# 🧼 Como desinstalar o VirtualBox no macOS (Intel ou Apple Silicon)

Este tutorial explica como remover o VirtualBox completamente do seu Mac — incluindo todas as dependências e arquivos ocultos.

✅ Compatível com chips Intel e Apple Silicon (M1, M2, M3)

---

## 1. Identifique a versão e arquitetura do VirtualBox

Antes de remover, vamos verificar qual versão está instalada:

VBoxManage --version

O resultado será algo como: 7.1.6r167084

Para saber a arquitetura (Intel ou ARM64), execute:

file /Applications/VirtualBox.app/Contents/MacOS/VirtualBox

Você verá:

- Para Intel: x86_64
- Para Apple Silicon: arm64

---

## 2. (Opcional) Baixar o .dmg correspondente

Se quiser usar o desinstalador oficial, baixe o .dmg da mesma versão:

1. https://download.virtualbox.org/virtualbox/
2. Escolha a versão identificada
3. Baixe o .dmg:
   - Apple Silicon: VirtualBox-<versão>-macOSArm64.dmg
   - Intel: VirtualBox-<versão>-macOS.dmg

Depois, execute:

sudo /Volumes/VirtualBox/VirtualBox_Uninstall.tool

---

## 3. Remoção manual (qualquer versão)

sudo rm -rf /Applications/VirtualBox.app  
sudo rm -rf /Library/Application\ Support/VirtualBox  
sudo rm -rf /Library/Extensions/VBox*.kext  
sudo rm -rf /Library/LaunchDaemons/org.virtualbox.startup.plist  
sudo rm -rf /Library/Receipts/org.virtualbox.pkg.*  
sudo rm -rf /private/var/db/receipts/org.virtualbox.pkg.*  
rm -rf ~/Library/VirtualBox

---

## 4. Reinicie seu Mac

---

## 5. Verificação

ps aux | grep -i virtualbox

---

## Alternativas ao VirtualBox

- UTM (https://mac.getutm.app/)
- Parallels Desktop (https://www.parallels.com/br/products/desktop/)
- Docker Desktop (https://www.docker.com/products/docker-desktop/)
