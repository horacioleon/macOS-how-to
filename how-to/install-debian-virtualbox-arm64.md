# 🧰 Instalação do VirtualBox e criação de máquina virtual Debian no MacBook M1/M2

Este guia explica como instalar o VirtualBox e configurar uma máquina virtual com o Debian 12.10 no seu MacBook com chip Apple Silicon (M1 ou M2).

---

## ✅ Pré-requisitos

- MacBook com chip **M1 ou M2** (Apple Silicon)
- Acesso à internet
- Permissões de administrador no macOS

---

## 📥 1. Baixar o VirtualBox para Apple Silicon

Baixe a versão do VirtualBox compatível com macOS ARM64 (Apple Silicon):

👉 [VirtualBox 7.1.6 para macOS ARM64](https://download.virtualbox.org/virtualbox/7.1.6/VirtualBox-7.1.6-167084-macOSArm64.dmg)

1. Após o download, abra o arquivo `.dmg`.
2. Clique duas vezes em `VirtualBox.pkg` para iniciar a instalação.
3. Siga os passos do instalador.
4. **Se aparecer um alerta de segurança**, vá em:
   - **Preferências do Sistema** > **Segurança e Privacidade** > **Geral**
   - Clique em **Permitir** para concluir a instalação.

> ℹ️ Importante: reinicie o sistema se for solicitado após a instalação.

---

## 📥 2. Baixar imagem ISO do Debian (ARM64)

Baixe a imagem de instalação do Debian para arquitetura ARM64:

👉 [Debian 12.10.0 ARM64 - DVD ISO](https://cdimage.debian.org/debian-cd/current/arm64/iso-dvd/debian-12.10.0-arm64-DVD-1.iso)

---

## 🖥️ 3. Criar uma máquina virtual Debian no VirtualBox

### 1. Abrir o VirtualBox

Abra o VirtualBox a partir da sua **pasta de Aplicativos** ou via **Spotlight**.

### 2. Criar nova máquina virtual

- Clique em **"Nova"**
- Nome: `Debian ARM64`
- Tipo: `Linux`
- Versão: `Debian (64-bit)` *(ou `Debian ARM64`, se disponível)*

### 3. Configurações básicas

- **Memória RAM**: pelo menos **2048 MB** (ou mais, se disponível)
- **Disco rígido virtual**: crie um novo disco VDI com **20 GB** ou mais

### 4. Configurar a ISO de instalação

- Com a VM selecionada, clique em **Configurações > Armazenamento**
- No controlador de disco, clique no ícone de disco e selecione:
  - **"Escolher um arquivo de disco"**
  - Selecione o arquivo ISO `debian-12.10.0-arm64-DVD-1.iso` baixado anteriormente

---

## 🚀 4. Iniciar a instalação do Debian

- Clique em **Iniciar** na VM
- O Debian carregará a partir da ISO
- Siga o processo de instalação (idioma, teclado, partição, etc.)
- Ao final, remova a ISO da unidade de CD virtual e reinicie a VM

---

## 🛠️ Dicas pós-instalação

- Instale pacotes básicos como:

```bash
sudo apt update && sudo apt install sudo curl git build-essential
