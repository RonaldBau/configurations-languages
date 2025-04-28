# Configuración en Visual Studio Code en Windows

Dentro de las aplicaciones instaladas en Windows, abra la opción `MYSYS2 UCRT64` 

![alt-img][image1]

Luego en la terminal abierta, ingrese los siguientes comandos:
 
1. **Actualiza e instala los paquetes necesarios de `MYSYS2`** 

    ```bash
    pacman -Syu --noconfirm
    ```

2. **Instala herramientas para que windows pueda reconocer y ejecutar comandos para `c++`**
    ```bash
    pacman -S mingw-w64-x86_64-gcc --noconfirm
    ```

3. **Asegurece de cambiar la variable de entorno del `Path` en Windows:**
    ```bash
    C:\msys64\mingw64\bin
    ```

4. **Verifique que pueda ejecutar el comando `g++` o `gcc` en su terminal, con el siguiente comando:**
    ```bash
    g++ --version
    ```

Deberia ver la siguiente salida:

![alt-img][image2]

Esto significa que ha podido configurar de manera correcta y que ya puede ejecutar y compilar desde su terminal de Windows.

### Verificar en la terminal de Visual Studio Code

Para ello dentro del editor de Visual Studio Code abra una nueva terminal, dirigase a la pestaña **Terminal > New Terminal**

Verifique que ya pueda compilar y ejecutar archivos `.cpp` en Visual Studio Code, como se muestra a continuación:

![alt-img][image4]

## Posibles errores en el archivos `.cpp`
Si tras instalar las extensiones de Visual Studio Code de `C/C++ Extension Pack` observa un error en la primera linea de un archivo `.cpp` como el siguiente archivo:

![alt-img][image5]

Este es un error de configuración de Visual Studio Code el cual no pudo realizarse automaticamente, usted debe elegir la condiguracion realizando la siguiente:

1. En Visual Estudio Code acceda al atajo: `Ctrl+Shift+P` cual abre una ventana y busque la opción de ***C/C++: Select IntelliSense Configuration...***

    ![alt-img][image6]

2. Seleccione la opcion Use `g++.exe` preferentemente que esten dentro de la ruta `C:/msys64/mingw64/bin`
    
    ![alt-img][image7]

    > Las opciones `g++.exe` o `gcc.exe` son ejecutables que realizan la misma operacion de compilar y ejecutar archivos c++. De preferencia eliga `g++` por esta vez.

3. Con ello, desaparecerá el error que aparecia anteriormente.

    ![alt-img][image8]

<!-- References -->
[image1]: /c++/img/01.PNG "Logo Title Text 2"
[image2]: /c++/img/03.PNG "Logo Title Text 2"
[image4]: /c++/img/04.PNG "Logo Title Text 2"
[image5]: /c++/img/05.PNG "Logo Title Text 2"
[image6]: /c++/img/06.PNG "Logo Title Text 2"
[image7]: /c++/img/07.PNG "Logo Title Text 2"
[image8]: /c++/img/08.PNG "Logo Title Text 2"
