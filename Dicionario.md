# 📘 Dicionário de Comandos Git e GitHub

## Configuração Inicial
| Comando | Descrição |
|----------|------------|
| `git config --global user.name "Seu Nome"` | Define o nome do usuário usado nos commits. |
| `git config --global user.email "seuemail@exemplo.com"` | Define o e-mail associado aos commits. |
| `git config --list` | Exibe as configurações atuais do Git. |

---

## Criação e Inicialização
| Comando | Descrição |
|----------|------------|
| `git init` | Cria um novo repositório Git local. |
| `git clone <url>` | Clona um repositório remoto para sua máquina. |

---

## Controle de Arquivos
| Comando | Descrição |
|----------|------------|
| `git status` | Mostra o estado atual dos arquivos (modificados, rastreados, etc). |
| `git add <arquivo>` | Adiciona um arquivo específico à área de staging. |
| `git add .` | Adiciona **todos** os arquivos modificados à área de staging. |
| `git rm <arquivo>` | Remove um arquivo do repositório e do diretório de trabalho. |
| `git mv <antigo> <novo>` | Renomeia ou move arquivos rastreados pelo Git. |

---

## Commits
| Comando | Descrição |
|----------|------------|
| `git commit -m "mensagem"` | Cria um novo commit com uma mensagem descritiva. |
| `git commit --amend` | Edita o último commit (mensagem ou conteúdo). |
| `git log` | Exibe o histórico completo de commits. |
| `git log --oneline` | Mostra o histórico resumido (um commit por linha). |

---

## Branches
| Comando | Descrição |
|----------|------------|
| `git branch` | Lista todas as branches locais. |
| `git branch <nome>` | Cria uma nova branch. |
| `git checkout <branch>` | Alterna para a branch especificada. |
| `git checkout -b <nome>` | Cria e muda para uma nova branch ao mesmo tempo. |
| `git branch -d <branch>` | Deleta uma branch local. |
| `git branch -m <novo_nome>` | Renomeia a branch atual. |

---

## Merge e Rebase
| Comando | Descrição |
|----------|------------|
| `git merge <branch>` | Une a branch especificada à branch atual. |
| `git merge --abort` | Cancela um merge em andamento. |
| `git rebase <branch>` | Reaplica commits da branch atual sobre outra branch. |
| `git rebase --continue` | Continua um rebase após resolver conflitos. |

---

## Repositório Remoto (GitHub)
| Comando | Descrição |
|----------|------------|
| `git remote -v` | Lista os repositórios remotos. |
| `git remote add origin <url>` | Conecta o repositório local a um remoto. |
| `git remote remove origin` | Remove a conexão com o remoto. |
| `git push origin <branch>` | Envia commits para a branch remota. |
| `git pull origin <branch>` | Atualiza a branch local com alterações do remoto. |
| `git fetch` | Baixa dados do remoto sem mesclar. |

---

## Desfazer e Corrigir
| Comando | Descrição |
|----------|------------|
| `git checkout -- <arquivo>` | Reverte alterações em um arquivo para o último commit. |
| `git reset <arquivo>` | Remove um arquivo da área de staging. |
| `git reset --soft HEAD~1` | Desfaz o último commit, mantendo alterações no código. |
| `git reset --hard HEAD~1` | Desfaz o último commit e descarta alterações. |
| `git revert <hash>` | Cria um novo commit que desfaz as mudanças de um commit específico. |

---

## Visualização e Análise
| Comando | Descrição |
|----------|------------|
| `git diff` | Mostra as diferenças entre arquivos modificados e o último commit. |
| `git log --graph --oneline --decorate --all` | Exibe o histórico em forma de gráfico. |
| `git blame <arquivo>` | Mostra quem alterou cada linha de um arquivo. |

---

## Dicas Extras
| Comando | Descrição |
|----------|------------|
| `git stash` | Armazena temporariamente alterações não commitadas. |
| `git stash pop` | Restaura alterações guardadas com `stash`. |
| `git tag <nome>` | Marca um commit específico (geralmente usado em versões). |
| `git show <hash>` | Mostra detalhes de um commit específico. |

---

**Fluxo básico de trabalho:**
```bash
git clone <url>
git branch nova-feature
git checkout nova-feature
# faz alterações
git add .
git commit -m "descrição"
git push origin nova-feature
