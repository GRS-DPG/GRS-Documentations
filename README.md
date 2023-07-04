# Welcome to the Grievance Redress System

- [Authors](#authors)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Developer Guide](#developer-guide)
- [Contributions and Support](#contributions-and-support)
- [License](#license)

## Authors

- [@Biplob](https://www.linkedin.com/in/ekramul-kabir-biplob/)
- [@Tappware Solutions Limited](https://tappware.com/)

## Features

- [Admin Features](https://github.com/GRS-DPG/GRS-Documentations/blob/master/3.2%20GRS%20Admin%20Manual.doc)
- [Complianant Features](https://github.com/GRS-DPG/GRS-Documentations/blob/master/3.1%20GRS-Complianant-Manual.doc)
- [GRO & Appeal Officer Features](https://github.com/GRS-DPG/GRS-Documentations/blob/master/3.3%20GRS%20GRO%20_%20Appeal%20Officer%20Manual.doc)


## Prerequisites

Before proceeding with the installation, make sure you have the following software installed on your system:

- Ubuntu Server
- Apache 2.4.52
- PHP (version 8.0 or higher)
- Composer
- Laravel 9.0
- MySQL 8.1.2
or
- MariaDB 10.4.22


## Installation

```sh
git clone this-url
```

```sh
cd project-root
```

##### Install [composer](https://getcomposer.org/) dependencies of this project by running

```sh
composer install
```

##### Copy `.env-example` to `.env` and configure your database and other connection.

##### Run this two command also

```shell
php artisan key:generate
php artisan storage:link 
```

##### Run this command for migration and seeder

```shell
php artisan migrate:fresh --seed
```

##### Run this command to seed menu permission

```shell
php artisan db:seed --class=TablePermissionKeySeeder
```

##### Run this command to seed menu permission for system admin, institute admin, branch admin, training center admin and triner

```shell
php artisan db:seed --class=RoleWisePermissionSeeder
```

##### Run this command to clear all type of cache

```shell
php artisan cache:clear
```

```shell
php artisan optimize:clear
```


##### Run this command to start application

```shell
php artisan serve
```



## Usage

Go to the link `http://127.0.0.1:5173/` for login and enter the system admin credentials below.

##### Demo complianant credentials

```shell
mobile no: 01756888319
password: 123456
```

##### Demo system admin credentials

```shell
user id: 200000000163
password: 02522016
```

##### Demo gro officer credentials

```shell
user id: 100000006843
password: 02522016
```

##### Demo appeal officer credentials

```shell
user id: 100000004769
password: 02522016
```


## Developer Guide

### Basic Instruction

- All model should extend BaseModel class.
- All controller should extend BaseController class.


## Contributions and Support

Thanks to [everyone](https://github.com/GRS-DPG/GRS-API/graphs/contributors)
who has contributed to this project!

Please see [CONTRIBUTING.md](CONTRIBUTING.md) to contribute.

If you found any bugs, Please report it using [Github](https://github.com/GRS-DPG/GRS-API/issues)

## License

Copyright 2023 @a2i, Bangladesh

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
