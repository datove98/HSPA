# Preparación de Desarrollador Full Stack

Instalar y configurar lo siguiente para poder iniciar el trabajo de desarrollo

## Software a Instalar

- [KeepassXC](https://keepassxc.org)
- Algún 2FA OTP Manager para Móvil (Android / iOS)
    - Como [Aegis](https://getaegis.app/), [Raivo OTP](https://raivo-otp.com/), Microsoft authenticator, Google Authenticator, etc.
- [Microsoft Teams](https://teams.microsoft.com) para Desktop (PC / Mac)
- [Session](https://getsession.org/) para Desktop (PC / Mac)
- [Visual Studio Community](https://visualstudio.microsoft.com/) (Windows)
    - Addon web con net core 2.2, 3.1 y 6.0
- [Visual Studio Code](https://code.visualstudio.com/)
    - Addon net core, flutter y dart
- [Azure Storage Explorer](https://azure.microsoft.com/en-us/features/storage-explorer/)
- SQL Server Manager
    - como [SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16) (Windows), [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver16) o [DbGate](https://dbgate.org/)
- Cliente MongoDB
    - Como [Compass](https://www.mongodb.com/products/compass), [Studio 3T](https://robomongo.org/), o alguna extension de [VSCode](https://www.mongodb.com/products/vs-code)
- SQLite Browser
    - como [DB Browser](https://sqlitebrowser.org/) o [DbGate](https://dbgate.org/)
- [Flutter](https://docs.flutter.dev/get-started/install)
    - poder intercalar entre 1.2 y 2.1 (con git o con FVM)
    - conectar dispositivo android / ios y usar flutter doctor
- [Android Studio](https://developer.android.com/studio) y Android SDK
    - addon flutter y dart
    - Usamos mínimo SDK para Android 5, 8 y 11
- [Xcode](https://apps.apple.com/us/app/xcode/id497799835?mt=12) (MacOS)
- [GIT](https://git-scm.com/)
    - opcionalmente un GUI como [TortoiseGIT](https://tortoisegit.org/) (Win) o [SmartGIT](https://www.syntevo.com/smartgit/)
- Agente de SSH
    - nativo en todas las nuevas versiones de [Windows](https://docs.microsoft.com/en-us/azure/devops/repos/git/use-ssh-keys-to-authenticate?view=azure-devops), MacOS y Linux
    - En windows anteriores usar [Putty](https://www.ssh.com/academy/ssh/putty/download)
- API Platform
    - como [insomnia.rest](https://insomnia.rest/) o [postman](https://www.postman.com/)
    - Opcionalmente instalar [CURL](https://curl.se/) en Windows, es nativo en macOS y Linux
- [scrcpy](https://github.com/Genymobile/scrcpy) en Android
- [TestFlight](https://testflight.apple.com/) en iPhone
- Configurar dispositivo Android como [developer](https://developer.android.com/studio/debug/dev-options)
    - Permitir Side Loading de APKs

## Configuración de Área de Trabajo

### Plan de Contraseñas

> Objetivo: Tener una administración y metodología responsable de contraseñas seguras

Una contraseña segura es:

- **Única**: Una por sistema, si es comprometida solo ese sistema es afectado.
- **Fuerte**: Larga, compleja e impredecible, esto se mide con `entropia` en bits.
- **Inaccesible**: Almacenada en un contenedor encriptado, en un lugar físico seguro, o en nuestra mente.

Hay 2 tipos de contraseñas:

- **Memorables**: Diseñadas para ser recordadas por cualquier persona, fáciles de leer y escribir. Típicamente son palabras de un diccionario, como [EFF_wordlist](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases) y [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki).
    - Una contraseña memorable fuerte es mayor a 75 bits de entropia, es decir de 8 palabras o mas

> Ej. "muestra-año-acceso-camello-torso-trompa-pierna-abrazo"

- **No memorables**: Diseñadas para NO ser recordadas ni fáciles de leer o escribir, son cadenas de caracteres con letras, números y símbolos.
    - Recomendamos maxima seguridad con contraseñas no memorables, con mas de 100 bits de entropia, es decir 24 letras, símbolos, y números o mas

> Ej. "TnJlMd$g=b^r+x)p}u,q@kFsOhYm6w\\i"

Hacer lo siguiente:

1.  Solo necesitas recordar una sola contraseña, crea una contraseña memorable maestra
    
    - **OJO**: queda estrictamente prohibido almacenar contraseñas de cualquier tipo en texto plano (Excel, notepad, word, google docs, apps de notas, etc )
    - Tiene que ser **fuerte**, con una entropia mayor a 75 bits, **es decir de 8 o más palabras***.
    - Puedes usar el generador de KeepassXC (solo contraseñas en ingles), o [diceware](https://wintelguy.com/diceware-passphrase-generator.pl), [BIP39](https://www.bip39.net/#spanish) (multi idioma)
        - Si lo prefieres, KeepasXC te permite agregar un diccionario de palabras, puedes descargar uno en español [aquí](https://github.com/bitcoin/bips/blob/master/bip-0039/spanish.txt) y agregarlo.
    - No importa idioma, separador de palabras, símbolos especiales, acentos, mayusculas o minúsculas, lo que importa es que sea memorable y fácil de escribir.
2.  Memoriza la contraseña y anota con un recordatorio temporal
    
    - Anota tu contraseña o un recordatorio en una hoja de papel con pluma o lápiz, y ponla en un lugar seguro, esto sera temporal.
    - Aprende tu contraseña maestra, la puedes teclear en algo como notepad muchas veces, pero no almacenes el archivo en el disco duro, solo es para practicar.
    - Usaras esta contraseña consistentemente, así que **después de unas semanas que ya la memorizaste, destruye la hoja de papel con tu contraseña o recordatorio**.
3.  Crea una base de datos de KeepassXC
    
    - Usa tu contraseña maestra que memorizaste
    - Puedes guardar el archivo en cualquier parte, y si gustas puedes usar un folder en la nube para respaldarlo (Dropbox, OneDrive, Google Drive, iCloud, etc)

Usaras KeepassXC para almacenar todas las cuentas, llaves, contraseñas, certificados, etc. o cualquier información privada que se te proporcione o que tu creas.

**OJO:** Todas las contraseñas nuevas que tu creas tienen que tener mas de 100 bits de entropia (usualmente mas de 24 caracteres)

### Cuenta de trabajo de Microsoft
> Objetivo:  Establecer seguridad de cuenta y comunicacion con el equipo de desarrollo.

Se te dará un nombre de usuario y contraseña temporal para tu cuenta de Microsoft. Esta cuenta proporciona acceso a lo siguiente:

- Correo Electrónico ([outlook.office.com](https://outlook.office.com/mail/))
- Microsoft Teams
- Microsoft Office ([office.com](/Applications/Joplin.app/Contents/Resources/app.asar/www.office.com "www.office.com"))
- DevOps ([dev.azure.com](https://dev.azure.com/))
- Y mas... (sql server, active directory, azure data, etc.)

Es importante que cuides y protejas esta cuenta. Haz lo siguiente:

1.  Crea una entrada nueva en KeepassXC, con el correo como nombre de usuario y algún titulo de tu preferencia.
2.  Genera una nueva contraseña **NO memorable** de 100 bits de entropia y guarda tu entrada.
3.  En tu cuenta de Microsoft:
    - Cambia tu contraseña con la nueva contraseña que generaste
    - Agrega 2FA (autenticación de 2 factores) usando la app de tu preferencia.

Configura tu cuentas de trabajo:
1\. Ahora puedes iniciar sesión en Microsoft Teams para chatear con todo el equipo de desarrollo.
2\. Sube una foto de perfil en tu cuenta de Teams, puede ser una foto casual pero seria (sin fiestas, fachas, familiares, pareja, etc).
3\. Puedes configurar el cliente de outlook si lo deseas.
4\. Puedes configurar tu OneDrive si gustas, tienes 1 TB de almacenamiento.

Usamos Teams y Outlook para planear juntas, tienes que estar atento a los mensajes y correos que recibas.

### Llaves SSH para GIT
> Objetivo: Establecer comunicación segura con el repositorio de GIT

Accederás a repositorios de código usando GIT, entre otros servicios (como VMs de linux). Para autenticar tu acceso, necesitas crear un par de llaves de SSH.

- Windows requiere mas preparación, sigue la siguiente guía de [Windows](https://docs.microsoft.com/en-us/azure/devops/repos/git/use-ssh-keys-to-authenticate?view=azure-devops)
- MacOS y Linux usualmente ya lo tienen instalado, si no, hay muchas guías en internet.

Haz lo siguiente:

1.  Crea un registro de contraseña en KeepassXC, sugiero generar una contraseña no memorable de solo letras y números.
2.  Navega hacia [dev.azure.com](https://dev.azure.com/) e inicia sesión.
3.  Abre la terminal (CMD o Power Shell en Windows, Terminal en Macos y Linux)
4.  Navega al folder de .ssh en la terminal con `cd`, usualmente en `~/.ssh/`
5.  Crea tu par de llaves con el comando `ssh-keygen`, con valores por defecto, copia la contraseña generada en KeepassXC y pégala cuando lo solicite.
6.  Se generaran 2 llaves, una llamada `id_rsa` y otra llamada `id_rsa.pub`
7.  Abre en notepad el archivo de `id_rsa.pub` y copia el contenido. Esta es tu llave pública.
8.  Vuelve a [dev.azure.com](https://dev.azure.com/), navega hacia preferencias de usuario (el icono de peon en la parte superior derecha), y selecciona "llaves SSH publicas".
9.  Agrega tu llave pública.

Ahora cuando clones un repositorio de GIT, copia la URL que usa SSH, y usa esa para clonar tus proyectos. Al usar `git clone git@ssh.dev.azure.com:v3/proyecto_ejemplo` te pedirá tu contraseña de la llave SSH.

De igual manera, al iniciar sesión en un servidor de linux con el comando `ssh user@server.com`te pedirá la contraseña.

Opcionalmente, para no tener que usar contraseñas puedes investigar el comando `ssh-add` para que deje tu contraseña guardada en el agente de SSH. Alternativamente puedes usar la funcionalidad de [Agente SSH en KeepassXC](https://keepassxc.org/docs/#faq-ssh-agent-how)

### Configuración de GIT
> Objetivo: Mostrar una correcta identidad en los repositorios de GIT

Para poder mostrar tu perfil en el historial de cambios de GIT, tu correo configurado en GIT tiene que ser el de tu cuenta de Microsoft.

Git permite configurar tu correo de manera global, o por repositorio. Si tienes una configuración de GIT actual con tus proyectos personales usando tu correo personal, puedes hacer el cambio por repositorio, pero recomiendo que lo hagas global de ser posible.

Sigue la siguiente [guía para configurar tu nombre y correo en GIT](https://linuxize.com/post/how-to-configure-git-username-and-email/).

### Configuración de [Session](https://getsession.org/)
> Objetivo: Compartir información privada y secreta con otros miembros del equipo de desarrollo.

Utilizamos Session para compartir texto o mensajes que requieran alta seguridad, por ejemplo contraseñas, llaves, certificados, etc. Los mensajes desaparecen en un tiempo establecido por lo que hay que copiarlos para guardarlos en KeepassXC cuando sea necesario.

Para garantizar que no pierdas tu cuenta, por favor respalda tu `frase de recuperación` de session en KeepassXC.
