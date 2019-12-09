# Laravel-Gii visual code generation tool CRUD + GUI

[中文文档](https://github.com/sunshinev/laravel-gii/blob/master/README_zh_CN.md)

[![Packagist Version](https://img.shields.io/packagist/v/sunshinev/laravel-gii)](https://packagist.org/packages/sunshinev/laravel-gii)
[![Travis (.com)](https://img.shields.io/travis/com/sunshinev/laravel-gii)](https://travis-ci.com/sunshinev/laravel-gii/)
![GitHub last commit](https://img.shields.io/github/last-commit/sunshinev/laravel-gii)
![GitHub](https://img.shields.io/github/license/sunshinev/laravel-gii)
![GitHub repo size](https://img.shields.io/github/repo-size/sunshinev/laravel-gii)
![GitHub stars](https://img.shields.io/github/stars/sunshinev/laravel-gii?style=social)
![GitHub forks](https://img.shields.io/github/forks/sunshinev/laravel-gii?style=social)

Suitable for fast B-side background development

According to the MySQL table structure, the corresponding project files such as Model, Observer, Controller, View, and Route are generated, and the complete CRUD background can be automatically created by simply clicking the mouse.


![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/controller.png)

   * [laravel-gii](#laravel-gii)
      * [Need to know before installing](#need-to-know-before-installing)
      * [Installation](#installation)
         * [Installation package](#installation-package)
         * [Publishing files](#publishing-files)
         * [Then visit](#then-visit)
      * [Use](#use)
         * [Creating a Model Model](#creating-a-model-model)
            * [Form Description](#form-description)
         * [Create CRUD](#create-crud)
            * [Form Description](#form-description-1)
         * [File Difference Comparison](#file-difference-comparison)
         * [Final file content](#final-file-content)
      * [Create a post page](#create-a-post-page)
         * [List](#list)
         * [Delete   Batch Delete](#delete--batch-delete)
         * [Row preview](#row-preview)
         * [Edit page](#edit-page)
      * [related question](#related-question)


## Installation

### Installation package

```
Composer require sunshinev/laravel-gii -vvv
```


### Publishing files
> This operation will release the assets static file to the public directory

```
Php artisan vendor:publish
```
select
`Tag: laravel-gii`


### Then visit
`http:[domain]/gii/model`


## Use


### Creating a Model Model

#### Form Description
1. Table name (supports drop-down selection)
2. Model class name (want to create a model class, including the namespace)
3. The parent class of the model inheritance (if Mongo can inherit `Jenssegers\Mongodb\Eloquent\Model`, MySQL uses `Illuminate\Database\Eloquent\Model`)


A list of generated files, blue for new files, red for existing files but different, white for existing files.

![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/success.png)

### Create CRUD

CRUD creation depends on the model created before.

This operation will be generated at the same time:

- route
- controller
- views

#### Form Description

1. Controller name (including namespace)
2. The previously created model class

![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/controller.png)

### File Difference Comparison
![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/diff2.png)

### Final file content
![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/viewfile.png)


## Create a post page

### List
This page contains the ability:

- list
- Pagination
- Search
- delete + batch delete
- preview
- Details
- Edit

![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/bg/bg_list.png)
### Delete + Batch Delete
Cancel button to prevent accidental deletion

![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/bg/bg_delete.png)

### Row preview
![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/bg/bg_view.png)

### Edit page
![image](https://github.com/sunshinev/remote_pics/raw/master/laravel-gii/bg/bg_edit.png)

## related question

1. If the Model is generated, the default configuration will be used in env. If you need to adjust, please modify the Model file.

## Need to know

The template generated by the project creation needs to rely on the [github:laravel-fe-render] (https://github.com/sunshinev/laravel-fe-render) project as a template parsing.

The background page depends on the compiled app.js ["github:base-fe"] (https://github.com/sunshinev/base-fe)

[https://github.com/sunshinev/laravel-gii](https://github.com/sunshinev/laravel-gii)