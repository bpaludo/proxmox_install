# proxmox_install

Apagar particoes Pendrive:

Abrir Command Prompt em modo administrador

diskpart

list disk

select disk 2 (ou outro numero)

clean

Formatar pendrive em Exfat

Baixar ISO do Proxmox 8 e colocar no pendrive

Entrar na Bios do Mini PC

Configurar para ligar automaticamente quando é energizado

Alterar order do boot e colocar pendrive na frente

Salvar e sair

Ideal é instalar o Proxmox em 2 SSDs de mesmo tamanho em Mirror para ter redundancia e protecao a falha em um dos discos

Para isso, usar a configuração RAID1, ashift12, compress lz4, checksum sha256, copies 1.

Caso nao tenha dois HDs, pode instalar em ZFS ou EXT4

FQDN usar: nomedopc.lan

Após instalar, retirar o pendrive e rebootar. Entrar na Bios novamente e colocar o SSD principal no primeiro disco no boot order


