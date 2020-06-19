# easyappointments-mu

easyappointments-mu is a heavily modified fork of [alextselegidis/easyappointments](https://github.com/alextselegidis/easyappointments) with the goal of creating a multiuser version of the application.

```diff
- Warning: The application is still an early alpha version. Do not use in production unless you know what you are doing! -
```

## Installation

First clone this repository

```
git clone git@github.com:Kuvvu/easyappointments-mu.git
```

then install all php requirements

```
composer install
```

## Configuration

easyappointments-mu will be configured by .env files for each customer host it will serve.
For example if your url will be https://meet.kuvvu.ch your .env file will be .meet.kuvvu.ch and needs to
be located in /storage/mu/

So copy the .env.example to /storage/mu/.HOSTNAME and fill out the file accordingly
```
PREFIX = Your Preferred Table Prefix
BASE_URL = The Base Url according to the HOSTNAME (eg https://meet.kuvvu.ch)
LANGUAGE = Available Languages are :

'arabic',
'bulgarian',
'chinese',
'danish',
'dutch',
'english',
'finnish',
'french',
'german',
'greek',
'hindi',
'hungarian',
'italian',
'japanese',
'luxembourgish',
'polish',
'portuguese',
'romanian',
'russian',
'slovak',
'spanish',
'turkish'

MYSQL_SERVER = Server IP or Hostname of Mysql Server
MYSQL_DATABASE = Database Name
MYSQL_USER = Database User
MYSQL_PASSWORD = Password
MYSQL_PORT = Port

SMTP = SMTP Server
SMTP_USER = SMTP Username
SMTP_PASS = SMTP Password
```

The multiuser definition can be done in two ways by

1. Using one Database with different Table Prefixes for each hostname
2. Using a different Database with every hostname

After added the .env File simply point your Web Server Configuration to the easyappointments-mu /src directory.

More Information can be found within the original Project or in the source code.
