# Open edX Devstack Aliases
Useful bash aliases for the edX devstack. I mainly use them to run tests
and paver commands quickly without having to SSH into my devstack.

## Warning
The aliases are highly opinionated. If you don't like
something you're welcome to submit pull requests and/or fork it!

## Commands
- `openedx` goes to the directory `~/work/openedx/edx-platform`
- `edxapp`: Execute command as the `edxapp` user e.g `$ edxapp ls`
- `vagrant_init_ssh`: Allow direct SSH via the edxapp user
- `paver`: Executes a paver command as the `edxapp` user e.g `$ paver --help`
- `manage.py`: Executes a manage.py command as the `edxapp` user e.g `$ manage.py --help`
- `pylint`: Executes pylint
- `test_bokchoy_one`: Tests a single bokchoy test case (requires the --serveronly to be running)
- `test_system_one`: Tests a single lms/cms unit and integration test case  e.g. `$ test_system_one lms/djangoapps/appsembler_api/tests/test_views.py`
- `test_cov_system_one`: Like `test_system_one`, with coverage report, and usually slower.


**Note:** Auto documentation generated from the code using:
```
$ grep -o 'Doc:.*' -- edx-devstack-aliases | sed -e 's|^Doc: `|- `|'
```

## Installation
Clone this repo:
```
$ git clone https://github.com/OmarIthawi/edx-devstack-aliases.git
```

Add the following line to your `~/.bashrc` file:

```
source ~/edx-devstack-aliases/edx-devstack-aliases
```

Close your terminal and open it again!

This repo requires allowing SSH as `edxapp`. To enable that
SSH into vagrant and run the commands below.

```
$ vagrant_init_ssh
```

# Known Limitations
 - [ ] It's currently not possible to do `$ edxapp vi file.txt`, you'd get
       a garbled screen!
 - [ ] Exiting long running commands like `$ paver lms` doesn't work, so
       it keeps running in the background.

# Author
Omar Al-Ithawi (<i@omardo.com>)

## Credit
 - The original repo was made while working at [**@Edraak**](https://github.com/Edraak).
 - It has been continued while working at  [**@appsembler**](https://github.com/appsembler).
