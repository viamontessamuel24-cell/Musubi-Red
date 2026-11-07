<div align="center">

# 🟣 Musubi Red

**Comparte la VPN de tu Android con tu iPhone, con un solo toque.**

[![Build](https://github.com/viamontessamuel24-cell/Musubi-Red/actions/workflows/build.yml/badge.svg)](https://github.com/viamontessamuel24-cell/Musubi-Red/actions)
![Android](https://img.shields.io/badge/Android-8.0%2B-3DDC84?logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-1.9-7F52FF?logo=kotlin&logoColor=white)
![Licencia](https://img.shields.io/badge/Licencia-MIT-8A2BE2)

</div>

---

## ✨ ¿Qué es Musubi Red?

*Musubi* (結び) significa **nudo, unión**. Musubi Red conecta tu Android con otro móvil, sobre todo un **iPhone**, para que este navegue y descargue a través de la **VPN que ya tienes encendida en el Android**, sin instalar nada en el iPhone.

Está pensada para que cualquier persona lo haga fácil: una pantalla minimalista con estilo *liquid glass*, un solo botón y los datos que necesitas a la vista.

## 🚀 Características

- 🔘 Un solo botón **Musubi** para activar o desactivar el uso compartido.
- 🌐 Proxy HTTP/HTTPS integrado en el puerto **8080**.
- 📶 Crea su propio Wi-Fi (*LocalOnlyHotspot*) o usa la zona Wi-Fi del sistema.
- 🧭 Muestra la IP y los datos que debes poner en el iPhone.
- 🔔 Servicio en primer plano: sigue activo aunque cambies de app.
- 🎨 Interfaz *liquid glass* con animaciones fluidas estilo iOS.
- 🔒 Sin anuncios, sin cuentas y sin recolección de datos.

## 🧩 ¿Cómo funciona?

```
 iPhone ──Wi-Fi──▶ Android (Musubi Red · proxy :8080) ──▶ VPN activa ──▶ Internet
```

El proxy corre en tu Android y sus conexiones salen desde allí, por lo que usan la VPN que tengas encendida.

## 📲 Uso paso a paso

1. Enciende tu **VPN** en el Android.
2. Abre **Musubi Red**, acepta los permisos y toca **Musubi**.
3. Toca **Crear Wi-Fi** (o activa la **zona Wi-Fi** del sistema).
4. En el iPhone, conéctate a ese Wi-Fi con la clave que muestra la app.
5. En el iPhone: **Ajustes › Wi-Fi › (i) › Configurar proxy › Manual**.
6. **Servidor** = la IP que muestra la app · **Puerto** = `8080` · Guardar.
7. Comprueba tu IP en Safari: debe ser la de tu VPN.

> Es normal que el iPhone diga "Sin conexión a internet" en ese Wi-Fi. El tráfico sale por el proxy.

## ⬇️ Instalación

1. Ve a la pestaña **Actions**, abre la última ejecución en verde y descarga el artefacto **MusubiRed-apk**.
2. Extrae el `.zip` e instala el `.apk` (permite "instalar apps desconocidas").

## 🛠️ Compilar

**Con GitHub Actions (sin PC):** al subir cambios, el flujo `.github/workflows/build.yml` descomprime `MusubiRed.zip`, compila con Gradle 8.7 / JDK 17 y publica el APK.

**Con Android Studio:** abre la carpeta `MusubiRed` y ejecuta *Build › Build APK(s)*.

Requisitos: Android 8.0 (API 26) o superior · `compileSdk 34` · Kotlin 1.9.

## 📁 Estructura

```
MusubiRed/
├─ app/src/main/java/com/musubi/red/
│  ├─ MainActivity.kt    Interfaz, Wi-Fi y panel "Acerca de"
│  ├─ ProxyServer.kt     Proxy HTTP/HTTPS (CONNECT)
│  ├─ ProxyService.kt    Servicio en primer plano
│  ├─ MusubiButton.kt    Botón de cristal con ondas
│  ├─ Anim.kt            Animaciones tipo resorte
│  └─ Info.kt            Textos, enlaces y datos editables
└─ app/src/main/res/     Diseños, íconos y estilos
```

## 🔐 Seguridad y privacidad

- Musubi Red **no recopila ni envía datos** a ningún servidor.
- El proxy **no tiene contraseña**: cualquiera conectado a tu Wi-Fi compartido podría usarlo. Úsalo en tu propio Wi-Fi y **apágalo al terminar**.
- Úsala solo con tus propios dispositivos y con VPN que tengas derecho a usar.

## ⚠️ Limitaciones conocidas

- Algunas apps de iOS ignoran el proxy del Wi-Fi.
- En ciertos Android no se puede crear el Wi-Fi propio mientras usas Wi-Fi como internet; en ese caso usa la zona Wi-Fi del sistema.
- Wi-Fi Direct y Bluetooth no se incluyen porque el iPhone no los soporta para compartir internet.

## ❤️ Apoya el proyecto

Musubi Red es gratis. Si te sirvió, toca el botón ❤ dentro de la app para ver cómo apoyar (solo Cuba) o compártela con quien la necesite.

## 👤 Autor

**Samuel Viamontes Escobar** — creador de contenido, desarrollador web y de apps iOS, creador de TransferPay.

[YouTube](https://youtube.com/@bytebytecu) · [Instagram](https://www.instagram.com/byteabytecu) · [Facebook](https://www.facebook.com/share/17s1Y4jyar/) · [Web](https://bytebyteweb.wordpress.com/) · [Correo](mailto:samuelviamontes07@gmail.com)

## 📄 Licencia

Distribuido bajo la licencia **MIT**. Consulta el archivo [LICENSE](LICENSE).
