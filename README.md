## About

This project utilizes the [pantheon-systems/travis-scripts](https://github.com/pantheon-systems/travis-scripts) project in order to achieve the following things:

* Specify the Drupal modules, themes and libraries you use in a composer.json file, and build them with Composer.
* Automatically build components via Travis every commit.
* Use Behat to run tests on your site from Travis.
* Automatically deploy your site to your Pantheon dev environment, or some other branch, every time the tests pass.

## Create a New Project

There are two ways to quickly create a new project for your Drupal site, using this project as a template.

#### Via GitHub

* [Fork this project in GitHub](https://github.com/pantheon-systems/example-drupal7-composer#fork-destination-box)
* Clone your fork locally
* `$ cd example-drupal7-composer`
* `$ ./bin/init-new-project`

#### Via Composer
```
$ composer create-project pantheon-systems/example-drupal7-composer project '1.*'
```

## Configuration

Once you have created a new project, you will need to customize some of the files created to suit your particular needs.  See the [travis-scripts README](https://github.com/pantheon-systems/travis-scripts) for instructions on how to do this.

## Testing Locally
```
$ ./bin/local-test
```

## Repository Management

If you followed the instructions  above to create your project, then a suitable .gitignore file will already have been created for you.  You may therefore simply add and commit the modified files to your repository.

#### Custom Modules and Themes

You may place your custom modules and themes in `drupal/sites/all/modules/custom` and `drupal/sites/all/themes/custom`, respectively, and commit them to the same repository that contains your composer.json file.

If you prefer, you may instead create a Composer project for them, and add them to your composer.json file.  See [Creating your very own Composer Package](https://knpuniversity.com/screencast/question-answer-day/create-composer-package) for details on how to do this.

