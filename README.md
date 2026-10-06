# Android-ConfidentalDataCibersecurity

Android Confidential Data analysis for ethical security.

## PASOS

1. Hacemos un profile de la APK con Android Studio.
![Android Analyze APK](./doc/img/1.png)

2. Iniciamos la app en modo monitor con el botón específico para ello (véase la documentación oficial para desarrolladores de Android).
![Android Analyze APK 2](./doc/img/2.png)

3. Iniciamos sesión con las credenciales por defecto (user: jack, password: Jack@123$).
![Android Analyze APK 3](./doc/img/3.png)

4. Hemos iniciado sesión.
![Android Analyze APK 4](./doc/img/4.png)

5. Usamos adb (la interfaz de debuggeo de Android) para ver los dispositivos contectados y entrar a su sistema de ficheros.
![Android Analyze APK 5](./doc/img/5.png)

6. Recuperamos las preferences con los datos de inicio de sesión con `adb pull data/data/com.android.insecurebankv2/shared_prefs/mySharedPreferences.xml`.
![Android Analyze APK 6](./doc/img/6.png)

7. Vemos los datos de inicio de sesión en shared_prefs.
![Android Analyze APK 7](./doc/img/7.png)

8. Antes de iniciar sesión, tenemos que arrancar el servidor de la app. Así recuperaremos los datos al iniciar sesión desde la consola.
![Android Analyze APK 8](./doc/img/8.png)

9. Desciframos los datos con ayuda del código fuente de la aplicación (aquí desciframos la contraseña con AES, ya que el nombre de usuario está codificado en Base64).
![Android Analyze APK 9](./doc/img/9.png)

* Este es el código fuente de la aplicación donde se hace login y se encripta los datos.
![Android Analyze APK Info](./doc/img/10.png)
