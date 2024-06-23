# suBruteforce

<p align="center">
  <img src="https://github.com/D1se0/suBruteforce/assets/164921056/c1de1502-f825-472a-857e-4dca9e336377" alt="Directorybrute" width="400">
</p>

---

## Description

**`suBruteforce`** is a brute force tool designed to test user and password combinations on Unix systems using the `su` command. This tool is written in Python and provides a friendly and customizable interface for performing brute force attacks.

## Characteristics

- Brute force using lists of users and passwords.
- Support for multiple threads to speed up the process.
- Export results to a file.
- Continuation of brute force even after finding a valid password (optional).
- Check to make sure the script is not run as root.

## Install

### Requirements

- `Python 3`
- `pip` (python package manager)

### Installation Steps

1. Clone the repository:

    ```sh
    git clone https://github.com/D1se0/suBruteforce.git
    cd suBruteforce
    ```

2. Run the installation script:

    ```sh
    ./requeriments.sh
    ```

    This script will install all the necessary dependencies and copy the `suBruteforce.py` file to `/usr/bin/suBruteforce`.

## Use

### Basic Commands

- **Basic use with a single user and a password dictionary:**

    ```sh
    python3 suBruteforce.py -u <user> -w <password_file>
    ```

- **Use with a user list and password dictionary:**

    ```sh
    python3 suBruteforce.py -U <user_file> -w <password_file>
    ```

- **Specify a single password for a user:**

    ```sh
    python3 suBruteforce.py -u <user> -p <password>
    ```

- **Use multiple threads to speed up the process:**

    ```sh
    python3 suBruteforce.py -u <user> -w <password_file> -t <number_of_threads>
    ```

- **Export results to a file:**

    ```sh
    python3 suBruteforce.py -u <user> -w <password_file> -f <results_file>
    ```

- **Continue brute force even after finding a valid password:**

    ```sh
    python3 suBruteforce.py -U <user_file> -w <password_file> --success-continue
    ```

## Execution Example

```sh
python3 suBruteforce.py -u test -w passwords.txt -f credentials.txt
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

## Contributions

Contributions are welcome! If you would like to contribute, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
