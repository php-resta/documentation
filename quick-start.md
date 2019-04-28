# Resta Quick Start

If you want to have a quick start to resta.
Just take a look at this short document.
You will need to install it first, as with any framework or package.
We need a composer installer to install the resta api.
If you don't have a composer installer, please [composer](https://getcomposer.org/download)
Check out this link.

## How to install the resta?

```bash
$ composer create-project php-resta/skeleton company_name dev-master
```
> **company_name:** The directory to which you will install the resta api is generally a group name that is valid for your company name or projects.Thus, your api projects will be in this general directory.

Your resta skeleton structure is now ready.

```bash
$ cd company_name
```
You can pass to the home directory of your project using the terminal command.

## Create your first project.

Now it's time to create our project.Your project will be created in the src / app directory.Let's create a project named demo with the command below.

```bash
$ php api project create demo
```

If you get a response similar to the following, Oh! Excellent. You now have a new project called demo.

```bash
$  > Application called as "Demo" has been successfully created in the /path/company_name/src/app/Demo/
```

Your project is located in the directory called src / app / Demo. Below you can see the structure of your project.

```code
Demo/
|
|- Api/
|  |- V1/
|     |- Config/
|     |- Middleware/
|     |- ServiceAnnotationsManager.php
|     |- ServiceEventDispatcherManager.php
|     |- ServiceLogManager.php
|     |- ServiceMiddlewareManager.php  
|
|- Kernel/
|  |- Node/
|     |- index.html
|  |- Providers/
|     |- AppServiceProvider.php
|     |- ConsoleEventServiceProvider.php
|     |- RouteServiceProvider.php
|  |- Stub/
|     |- index.html
|  |- Kernel.php
|  |- Version.php
|
|- Storage/
|  |- Language
|  |- Log
|  |- Resource
|  |- index.html
|
|- Tests/
|  |- index.html
|
|- Webservice/
|  |- index.html
|
|- .gitignore
|- composer.json
|- README.md

```

This project structure is created by default with each project command.Find out how to customize this structure in documents.
Since this section is a quick start, we won't write here what these directory structures do.
We'll just show you how to quickly reach your endpoints.

## Access your endpoints with the browser.

```code
http://localhost/company_name/public/demo
```

Now open your browser and enter the above address via localhost or ip.
As mentioned earlier, the directory where you create the resta skeleton repository structure will be your company_name name.


```code
{
"meta": {
"success": false,
"status": 401,
"illuminator": null
},
"resource": {
"errorMessage": "No Endpoint"
}
}
```

Congratulations! You took the first exception output :). Don't worry, you haven't done anything yet.

## Create your first controller structure.

```bash
$ php api controller create demo controller:users
```
Then let's create our first endpoint.Try creating your first controller with the command above.

```bash
$  > Controller called as "Users" has been successfully created in the /path/company_name/src/app/Demo/Api/V1/Controllers

```

Great! Your first controller has been successfully created. Now you'll see a controller directory created by looking into the V1 directory.
We will not describe the structure in this directory in this section. You will already find detailed information in our documents.


```code
http://localhost/company_name/public/demo/users
http://localhost/company_name/public/demo/v1/users //the same as the above request.

```

Now open your browser again and change the URL string that you specified with the demo to demo/users and request the request.

```code
{
"meta": {
"success": true,
"status": 200,
"illuminator": null
},
"resource": {
"endpoint": "Users"
}
}
```

This is great! We now have the first http 200 output.By default the system produces you json.You can find in our documentation how to change it.
This output is called as endpoint "users" and has a class as UsersController in the "Users" directory.


```code
<?php

namespace App\Demo\Api\V1\Controllers\Users;

class UsersController extends App
{
    /**
     * #define: get Users
     *
     * @return mixed|array
     */
    public function index()
    {
        return [
            'endpoint'=>'Users'
        ];
    }
}
```

Did you like it? in that case,continue reading our documents.We want you to have a nice the restfull api.
As you read the resta documents, we can say from now that you will say perfect for resta.Because the resta has wonderful facilities.



