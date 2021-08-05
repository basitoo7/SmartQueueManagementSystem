# SmartQueueManagementSystem
smart queue management system is developed in python flask rest API base user friedly system

### Features:

- Support for POS USB printers on major operating systems.
- Customize-able interfaces.
- Supports text-to-speech announcement.

### Setup:

#### - With executable:

You can find an executable that's suitable to your OS from :

- [FQMS](https://fqms.github.io/#download)
- [Github Release](https://github.com/mrf345/FQM/releases/)
- [Sourceforge](https://sourceforge.net/projects/free-queue-manager/)

#### - From the source:

- Make sure to install and use **Python 3.7** or **3.8**
- Execute the following commands in a terminal window:

1. `git clone https://github.com/mrf345/FQM.git`
2. `cd FQM`
3. `python -m pip install -r requirements/deploy.txt`
4. `python run.py --cli`

- To checkout the supported command-line options `python run.py --help`:

```bash
Usage: run.py [OPTIONS]

  FQM command-line interface (CLI):

  * If `--cli` is not used, initializing GUI will be attempted.

  * If no `ip` is passed it will default to `127.0.0.1`.

  * If no `port` is passed it will default to a random port.

Options:
  --cli        To use commandline interface instead of GUI.
  --quiet      To silence web server logs.
  --reset      Reset admin default password.
  --ip TEXT    IP address to stream the service on.
  --port TEXT  Port to stream the service through.
  --help       Show this message and exit.
```

#### - For development on Linux\MacOS:

- Make sure to install and use **Python 3.7**
- Execute the following commands in a terminal window:

1. `chmod +x installer.sh`
2. `./installer.sh --install`
3. `./installer.sh --run`

- To checkout the supported command-line options `./installer.sh --help`:

```bash
./installer.sh --help: Examples

    ./installer.sh --install        to install packages required
    ./installer.sh --uninstall      to remove packages installed
    ./installer.sh --run            to run FQM
    ./installer.sh --test           to run FQM tests
    ./installer.sh --migration      to run FQM migration
    ./installer.sh --help           to print out this message
```

#### - Database migration:

Since the `0.7` release we're able to migrate the data generated in previous releases to the new ones.

- You'll have to copy the `data.sqlite` file from the main project folder to the new release project folder.
- If you've uploaded any `Multimedia` files to your previous setup, make sure to copy them over to the new project folder manually from and to `FQM/static/multimedia/` folder.

**Make sure the migration steps are performed prior to running the new release of the system**.

### Documentation:

- [How do i add support for my language ?](docs/localization.md)
- [How do i add additional settings and customizations ?](docs/settings.md)
