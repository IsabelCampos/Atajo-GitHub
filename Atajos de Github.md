# 🚀 Guía de Referencia: Git & Terminal

Esta guía contiene los comandos esenciales para el manejo de repositorios, configuración de llaves SSH y flujo de trabajo en la terminal.

---

## 📂 Comandos de la Terminal
| Comando | Descripción (ES) | Description (EN) |
| :--- | :--- | :--- |
| `pwd` | Muestra el directorio actual | Print working directory |
| `ls -a` | Lista todos los archivos (incluyendo ocultos) | List all files |
| `cd [ruta]` | Cambia el directorio | Change directory |
| `mkdir [nombre]` | Crea una nueva carpeta | Make directory |
| `touch [archivo]` | Crea un archivo vacío | Create an empty file |
| `cat [archivo]` | Muestra el contenido de un archivo | Preview file content |
| `mv [origen] [destino]` | Mueve o renombra archivos/carpetas | Move or rename files |
| `rm [archivo]` | Elimina un archivo | Remove a file |
| `rm -rf [dir]` | Elimina una carpeta y su contenido | Remove a directory recursively |
| `clear` | Limpia la pantalla de la terminal | Clear terminal screen |
| `sudo` | Ejecuta comandos como administrador | Execute as superuser |

---

## ⚙️ Configuración de Git
| Comando | Descripción |
| :--- | :--- |
| `git config --global user.name "Nombre"` | Configura tu nombre de usuario |
| `git config --global user.email "correo@ejemplo.com"` | Configura tu correo electrónico |
| `git config --list` | Lista todas las configuraciones activas |
| `alias arbolito="git log --all --graph --decorate --oneline"` | Crea el alias para ver el historial gráfico |

---

## 🔑 Gestión de Llaves SSH
| Comando | Descripción |
| :--- | :--- |
| `ssh-keygen -t rsa -b 4096 -C "email@example.com"` | Generar credencial SSH |
| `eval $(ssh-agent -s)` | Verifica el servidor de credenciales |
| `ssh-add ~/.ssh/id_rsa` | Agrega la credencial al entorno |

---

## 🛠️ Flujo de Trabajo Básico (Snapshoting)
| Comando | Descripción |
| :--- | :--- |
| `git init` | Inicia un nuevo repositorio local |
| `git status` | Verifica el estado de los archivos |
| `git add .` | Agrega todos los cambios al área de preparación |
| `git commit -m "mensaje"` | Crea un punto de control con un mensaje |
| `git commit -am "mensaje"` | Agrega cambios y hace commit en un paso |
| `git commit --amend` | Corrige el último commit realizado |

---

## 🌿 Ramas y Fusión (Branching & Merging)
| Comando | Descripción |
| :--- | :--- |
| `git branch` | Lista las ramas locales |
| `git branch [nombre]` | Crea una nueva rama |
| `git checkout [nombre]` | Cambia a la rama especificada |
| `git checkout -b [nombre]` | Crea una rama y cambia a ella inmediatamente |
| `git merge [rama]` | Fusiona la rama especificada con la actual |
| `git branch -d [nombre]` | Elimina una rama local |
| `git stash` | Guarda temporalmente los cambios (limpia el workspace) |
| `git stash clear` | Elimina todos los elementos guardados en el stash |

---

## 🌐 Repositorios Remotos
| Comando | Descripción |
| :--- | :--- |
| `git remote add origin [URL]` | Vincula el repo local con uno remoto |
| `git remote -v` | Lista las conexiones remotas configuradas |
| `git remote set-url origin [URL]` | Cambia la URL del repositorio remoto |
| `git pull origin [rama]` | Trae los cambios remotos y los fusiona |
| `git push origin [rama]` | Sube tus cambios locales al servidor |
| `git clone [URL]` | Descarga una copia completa de un repositorio |

---

## 🏷️ Etiquetas (Tags) y Versiones
| Comando | Descripción |
| :--- | :--- |
| `git tag -a v0.1 -m "mensaje" [id_commit]` | Crea una etiqueta anotada |
| `git tag` | Lista todas las etiquetas creadas |
| `git show-ref --tags` | Muestra la referencia de los tags |
| `git push origin --tags` | Sube todas las etiquetas al servidor |
| `git tag -d [nombre]` | Elimina una etiqueta localmente |
| `git push origin :refs/tags/[nombre]` | Elimina una etiqueta de GitHub |

---

## 🔍 Inspección y Otros
| Comando | Descripción |
| :--- | :--- |
| `git log --oneline` | Muestra el historial simplificado |
| `git diff [rama1] [rama2]` | Compara cambios entre ramas |
| `git grep -n [palabra]` | Busca palabras dentro de todo el proyecto |
| `git cherry-pick [id]` | Trae un commit específico de otra rama |
| `gitk` | Abre la interfaz gráfica de Git |
