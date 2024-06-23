# suBruteforce

## Descripción

**suBruteforce** es una herramienta de fuerza bruta diseñada para probar combinaciones de usuarios y contraseñas en sistemas Unix utilizando el comando `su`. Esta herramienta está escrita en Python y proporciona una interfaz amigable y personalizable para realizar ataques de fuerza bruta.

## Características

- Fuerza bruta utilizando listas de usuarios y contraseñas.
- Soporte para múltiples hilos para acelerar el proceso.
- Exportación de resultados a un archivo.
- Continuación de la fuerza bruta incluso después de encontrar una contraseña válida (opcional).
- Verificación para asegurarse de que el script no se ejecute como root.

## Instalación

### Requisitos

- Python 3
- pip (gestor de paquetes de Python)

### Pasos de Instalación

1. Clona el repositorio:

    ```sh
    git clone https://github.com/tuusuario/suBruteforce.git
    cd suBruteforce
    ```

2. Ejecuta el script de instalación:

    ```sh
    ./requeriments.sh
    ```

    Este script instalará todas las dependencias necesarias y copiará el archivo `suBruteforce.py` a `/usr/bin/suBruteforce`.

## Uso

### Comandos Básicos

- **Uso básico con un solo usuario y un diccionario de contraseñas:**

    ```sh
    suBruteforce -u <usuario> -w <archivo_de_contraseñas>
    ```

- **Uso con una lista de usuarios y un diccionario de contraseñas:**

    ```sh
    suBruteforce -U <archivo_de_usuarios> -w <archivo_de_contraseñas>
    ```

- **Especificar una única contraseña para un usuario:**

    ```sh
    suBruteforce -u <usuario> -p <contraseña>
    ```

- **Usar múltiples hilos para acelerar el proceso:**

    ```sh
    suBruteforce -u <usuario> -w <archivo_de_contraseñas> -t <número_de_hilos>
    ```

- **Exportar los resultados a un archivo:**

    ```sh
    suBruteforce -u <usuario> -w <archivo_de_contraseñas> -f <archivo_de_resultados>
    ```

- **Continuar la fuerza bruta incluso después de encontrar una contraseña válida:**

    ```sh
    suBruteforce -U <archivo_de_usuarios> -w <archivo_de_contraseñas> --success-continue
    ```

## Ejemplo de Ejecución

```sh
suBruteforce -u test -w passwords.txt -f credentials.txt
 ____       _             ____       _             
/ ___|  ___| |_ _   _ ___|  _ \ ___ (_)_ __   __ _ 
\___ \ / _ \ __| | | / __| |_) / _ \| | '_ \ / _` |
 ___) |  __/ |_| |_| \__ \  __/ (_) | | | | | (_| |
|____/ \___|\__|\__,_|___/_|   \___/|_|_| |_|\__, |
                                            |___/ 

Bienvenido a suBruteforce - Herramienta de Fuerza Bruta para su

[+] Contraseña encontrada para 'test': test123
[+] Resultados exportados correctamente a 'credentials.txt'.
```

## Contribuciones

¡Las contribuciones son bienvenidas! Si deseas contribuir, por favor abre un issue o envía un pull request.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.
