# Fitxa tècnica: Configuració d'una connexió SSH en Ubuntu Server

## Objectiu

L'objectiu d'aquesta pràctica és configurar i comprovar el servei SSH en Ubuntu Server per poder accedir remotament al servidor des d'un altre ordinador de la xarxa.

## Materials

- Un ordinador amb Visual Studio Code.
- Una màquina virtual amb Ubuntu Server.
- Un ordinador amb Windows Terminal.
- Connexió de xarxa entre els dos equips.

## Procediment

1. Iniciar la màquina virtual amb Ubuntu Server.
2. Comprovar l'adreça IP del servidor amb la comanda `ip a`.
3. Comprovar si el servei SSH està instal·lat.
4. Instal·lar el servei SSH si és necessari.
5. Comprovar que el servei SSH està actiu.
6. Obrir Windows Terminal a l'ordinador client.
7. Connectar-se al servidor mitjançant la comanda SSH.
8. Comprovar que podem executar comandes remotament al servidor.

## Comprovacions

- [ ] Comprovar l'adreça IP del servidor amb `ip a`.
- [ ] Comprovar que el servei SSH està actiu.
- [ ] Comprovar que l'ordinador client té connexió amb el servidor.
- [ ] Comprovar que la connexió SSH funciona correctament.

## Incidències i solucions

| Incidència | Solució |
|---|---|
| El servei SSH no està instal·lat | Instal·lar-lo amb `sudo apt install ssh`. |
| El servei SSH no està actiu | Iniciar-lo amb `sudo systemctl start ssh`. |
| No es pot establir la connexió | Comprovar l'adreça IP i la connexió de xarxa. |
| La contrasenya no és correcta | Comprovar les credencials de l'usuari del servidor. |

## Recursos

- [Documentació d'Ubuntu Server](https://ubuntu.com/server/docs)
- [Documentació d'OpenSSH](https://ubuntu.com/server/docs/how-to/security/openssh-server)

![Captura de la connexió SSH](img/captura-ssh.png)

## Comanda de comprovació

```bash
ip a
sudo systemctl status ssh
ssh usuari@adreça_ip
