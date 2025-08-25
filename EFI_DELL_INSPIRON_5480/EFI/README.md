# Hackintosh EFI para Dell Inspiron 5480

Esta pasta contém a EFI para a instalação do macOS no **Dell Inspiron 5480**.

![Foto da sua máquina rodando macOS](link_para_a_imagem.jpg) 

## Especificações do Hardware

| Componente       | Modelo Específico                              |
| ---------------- | -----------------------------------------------|
| **CPU**          | i7-8565U (Whiskey Lake)                        |
| **GPU**          | Intel HD Graphics 620                          |
| **GPU Dedicada** | NVIDIA GeForce MX150 (Desativada)              |
| **RAM**          | 8GB DDR4 2400MHz                               |
| **SSD**          | Sk Hynix SSD M.2 Nvme 256gb                    |
| **Wi-Fi/BT**     | Intel Wireless-AC 9560                         |
| **Áudio**        | Realtek ALC295 (Layout ID: 13)                 |
| **Tela**         | 14" Full HD (1920x1080)                        |

## Versões de Software

* **macOS:** macOS Big Sur 11
* **OpenCore:** 0.9.7

## O que Funciona e o que Não Funciona

### Funcional ✅

* [✅] Aceleração gráfica (QE/CI) da Intel HD Graphics 620
* [✅] Áudio (alto-falantes internos, fone de ouvido e microfone)
* [✅] Wi-Fi e Bluetooth
* [✅] Portas USB-A e USB-C
* [✅] Gerenciamento de energia e suspensão (Sleep)
* [✅] Webcam
* [✅] Teclado e Trackpad (com gestos)
* [✅] Indicador de bateria

### Não Funcional ❌ ou com Problemas ⚠️

* [❌] Leitor de cartão SD (não é suportado)
* [❌] HDMI (somente via USB-C DP)


## Instruções de Instalação

1.  **Criação do Pen Drive de Instalação:** Siga o [Guia de Instalação do OpenCore](https://dortania.github.io/OpenCore-Install-Guide/) para criar seu pen drive de instalação do macOS.
2.  **Copiar a EFI:** Após criar o instalador, monte a partição EFI do seu pen drive e copie a pasta `EFI` deste diretório para dentro dela.
3.  **Gerar SMBIOS:** **MUITO IMPORTANTE!** Você **DEVE** gerar um novo SMBIOS (SystemSerialNumber, UUID e MLB) para o seu sistema. Use o [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) para gerar os dados para o modelo `MacBookPro14,1`.
4.  **Configurações da BIOS/UEFI:**
    * **SATA Mode:** AHCI
    * **Secure Boot:** Disabled
    * **VT-d:** Disabled
    * **CSM:** Disabled
    

5.  **Instalação:** Dê o boot pelo pen drive e proceda com a instalação padrão do macOS.
6.  **Pós-instalação:** Após a instalação, monte a partição EFI do seu SSD e copie a pasta `EFI` do pen drive para lá.
