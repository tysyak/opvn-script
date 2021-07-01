# Configuración del VPN

## Dependencias

* Este script hace uso de YAD para crear dialogos.
  * Basadas en Debian: `sudo apt install yad`
  * Basadas en RedHat: `sudo yum install yad`
  * Basadas en ArchLinux: `sudo pacman -S yad`


En `vendor/YOUR-OPENVPN-CONFIG.opvn` sustituir por vuestra configuración 
openvpn, también añadir la siguiente línea para que el archivo de configuración 
lea las credenciales de acceso a su red VPN

`auth-user-pass $HOME/.local/scripts/vendor/pass.txt`

por supuesto en `vendor/pass.txt` poner dichas credenciales

NOTA: Sustituir la ruta a donde quiera almacenar el script, en este caso
se guardo dentro de `$HOME/.local/scripts`, donde `scripts/` es un
directorio creado(Se recomienda poner la ruta anterior en la variable
`$PATH`) 

En `ConnectVPN` cambiar el valor `$pass` por su cuenta de administrador
(también en `DisconnectVPN`) y la variable $CONFIG con la ruta de 
su configuración *.opvn como ruta absoluta para evitar futuros conflictos
`vendor/YOUR-OPENVPN-CONFIG.opvn`

