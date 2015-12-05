This package contains a base Testcase Class that can be used to run end-to-end tests against Selenium 2 (using its Selenium 1 backward compatible Api).

Installing
---

Use [Composer](https://getcomposer.org) and add inside your composer.json file:

```
    "require": {
        "phpunit/phpunit-selenium": "*",
    }
```

then run `composer update`.

Requirements
---

A feature branch containing all the commits you want to propose works best.

Please direct pull requests to [giorgiosironi/phpunit-selenium](https://github.com/giorgiosironi/phpunit-selenium) for automated testing upon merging.

Running the test suite
---

#### Via Vagrant

Just run the following Vagrant commands (a minimal version of `v1.7` is required) and everything will be set up for you. The first start will take some time which depends on the speed of your connection (and less - speed of your computer):

    vagrant up
    vagrant provision
    vagrant ssh

    cd /vagrant
    vendor/bin/phpunit Tests
 
and you must see the `phpunit` testing `phpunit-selenium` project.

##### IMPORTANT NOTE about `Vagrant` usage
After `vagrant` has initialized the VM it makes sense to change amount of memory (and number of CPUs) manually from 384Mb by default to something near 2Gb (and 2 CPUs accordingly). I didn't do that in `Vagrantfile` deliberately since not every configuration might afford allocating 2Gb and 2 CPUs. Otherwise VM will swap hardly and at least one test will crash due to Out Of Memory.

