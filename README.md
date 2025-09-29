
# 🚀 Instalação e uso do pyenv-win com pipx no Windows

Este guia mostra como instalar o **pyenv-win** no Windows usando **pipx**, configurar uma versão global do Python e criar um ambiente virtual para projetos.

---

## Pré-requisitos

- Ter o **Python** já instalado no Windows (pode ser a versão do instalador oficial).
- Acesso ao **PowerShell**.

---

## Instalar Pyenv

O Pyenv é uma ferramenta que ajuda a instalar e gerenciar múltiplas versões do Python no mesmo sistema.

No PowerShell, execute:

```powershell
git clone https://github.com/pyenv-win/pyenv-win.git "%USERPROFILE%\.pyenv"
```
Adicionar à variável de ambiente PATH os diretórios pyenv-win\bin e pyenv-win\shims.
---
Confirme que o pyenv foi instalado corretamente:

```powershell
pyenv --version
pyenv install --list
```
---


## Instalar e configurar uma versão do Python
Exemplo: instalar o Python 3.11.5 e defini-lo como padrão global:

```powershell
pyenv install 3.11.5
pyenv global 3.11.5
```

---
Verifique se a versão está ativa:

```powershell
python --version
```
---

## Criar e ativar um ambiente virtual no projeto
Navegue até a pasta do seu projeto e crie o ambiente virtual:
```powershell
python -m venv venv
```
---

Ative o ambiente virtual:
```powershell
.venv\Scripts\Activate.ps1
```

## Comandos úteis do pyenv
- pyenv versions        # lista todas as versões instaladas
- pyenv global <versão> # define a versão global do Python
- pyenv local <versão>  # define a versão apenas para o diretório atual
- pyenv which python    # mostra o caminho do Python em uso
