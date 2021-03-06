[![django](https://user-images.githubusercontent.com/39559256/58042289-f3cf0700-7b42-11e9-972a-0535fbe404af.jpg)](https://www.skysilk.com/blog/2017/how-to-make-a-blog-with-django/)

This repository is specifically meant to those who are looking into using Django, since this gives a good amount of information about Django and it's capabilities.

**Disclaimer**: I have also included a [bootstrap boilerplate](https://github.com/endormi/django/tree/master/boilerplate) for this project.

Since newer versions of Python are often faster, have more features, and are better supported, the latest version of Python 3 is recommended.

### Table of contents:

- [What is Django](#what-is-django-)
- [Building Web Applications](#building-web-applications-)
    - [Scalability](#scalability)
    - [Validation](#validation)
- [Security](#security-)
- [Packages](#packages-)
- [Documentation](#documentation-)
- [Open Source Community](#open-source-community-)
- [Installing Django](#installing-django-)
- [Articles](#articles)
- [Thanks](#thanks)

## What is Django 🐍

Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. Built by experienced developers, it takes care of much of the hassle of web development, so you can focus on writing your app without needing to reinvent the wheel. It’s free and open source.

To give you an idea what the capabilities of Django are, here is a list of big companies that use Django:

- [Disqus](https://disqus.com/)
- [Instagram](https://www.instagram.com/)
- [Spotify](https://www.spotify.com/)
- [YouTube](https://www.youtube.com/)
- [The Washington Post](https://www.washingtonpost.com/)
- [Dropbox](https://www.dropbox.com/)
- [BitBucket](https://bitbucket.org/)
- [Mozilla](https://www.mozilla.org/)
- [National Geographic](https://www.nationalgeographic.com/)
- [Pinterest](https://www.pinterest.com/)

**Django's Architecture**

[![django](https://user-images.githubusercontent.com/39559256/54877175-9d379c00-4e23-11e9-9a8e-08477fdb0a19.png)](https://subscription.packtpub.com/book/web_development/9781788831345/1/ch01lvl1sec12/how-does-django-work)

## Building web applications ⛏

Django has adopted Python’s `"batteries included"` approach, the framework has everything necessary to create a fully developed application without needing to install any packages.
You can start building a simple application instantly without needing to customize it since all of the essentials are already available.

Django's structure mainly consists of:

1. The Model Layer
2. The Views Layer
3. The Template Layer
4. The Development Process
5. Security
6. The Admin
7. Forms

### Scalability

Django, at it's core is just a series of components of Python, wired up and ready to go. Components are not dependent on each other, since they are separate entities. You can choose, pick, unplug and replace them when your app requires for that to be done. Meaning you can build up to whatever level of performance you need, without compromising the functionality of your app.

### Validation

Django follows the `DRY principle`. You have a Model and it has some fields with restrictions and rules e.g. `integer field`, `string field` with length constraint etc. You are going to take input from the users and want to save it in the Model and therefore need to validate the user inputs. You don’t have to write same fields and rules again. You just need to create a `ModelForm` class and it’ll use the field and rules from the Model class.

## Security 🔒

By default, Django prevents most common security mistakes:

* [XSS (cross-site scripting) protection](https://docs.djangoproject.com/en/3.0/topics/security/#cross-site-scripting-xss-protection) - Django template system by default escapes variables, unless they are explicitly marked as safe.

* [CSRF (cross site request forgery) protection](https://docs.djangoproject.com/en/3.0/topics/security/#cross-site-request-forgery-csrf-protection) - Django has built-in protection against most types of CSRF attacks, providing you have [enabled and used it](https://docs.djangoproject.com/en/3.0/ref/csrf/#using-csrf) where appropriate.

* [SQL injection protection](https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection) - Django uses built-in ORM, thus there is no risk of SQL injection (raw queries are possible, but by no means something that a beginner would need to use).

* [PBKDF2 password hashing](https://docs.djangoproject.com/en/3.0/topics/auth/passwords/#how-django-stores-passwords) - Django uses the PBKDF2 algorithm with a SHA256 hash, a password stretching mechanism recommended by NIST. It’s quite secure, requiring massive amounts of computing time to break. Depending on your requirements, you may choose a different algorithm, or even use a custom algorithm to match your specific security situation.

More on [django security](https://docs.djangoproject.com/en/3.0/topics/security/).

## Packages 📦

If you happen to need more than Django offers, searching for `"django"` on `PyPI` finds lots of available for use.

A list of awesome Django packages (not in a specific order):

- [django-allauth](https://pypi.org/project/django-allauth/)
- [django-channels](https://channels.readthedocs.io/en/latest/)
- [django-contact-form](https://pypi.org/project/django-contact-form/)
- [django-compressor](https://django-compressor.readthedocs.io/en/stable/)
- [django-crispy-forms](https://django-crispy-forms.readthedocs.io/en/latest/)
- [django-filter](https://pypi.org/project/django-filter/)
- [django-rest-framework](https://www.django-rest-framework.org/)
- [django-tables2](https://pypi.org/project/django-tables2/)
- [django-taggit](https://django-taggit.readthedocs.io/en/latest/)
- [django-sorting-field](https://pypi.org/project/django-sorting-field/)
- [django-environ](https://django-environ.readthedocs.io/en/latest/)
- [django-fsm](https://github.com/viewflow/django-fsm)
- [django-registration](https://django-registration.readthedocs.io/en/3.0/)
- [django-two-factor-auth](https://django-two-factor-auth.readthedocs.io/en/stable/)
- [django-favorite](https://pypi.org/project/django-favorite/)
- [django-debug-toolbar](https://django-debug-toolbar.readthedocs.io/en/latest/index.html)
- [django-redis](http://niwinz.github.io/django-redis/latest/)
- [django-model-utils](https://django-model-utils.readthedocs.io/en/latest/)
- [django-extensions](https://django-extensions.readthedocs.io/en/latest/)
- [django-cors-headers](https://pypi.org/project/django-cors-headers/)
- [django-sendsms](https://pypi.org/project/django-sendsms/)
- [django-csp](https://pypi.org/project/django-csp/)

## Documentation 📑

Django’s [official documentation](https://docs.djangoproject.com/en/3.0/) is more than enough. On top of that, **Stack Overflow** is well-stocked with questions & answers related to Django.

## Open Source Community 🗃

Being open source and insanely popular, Django has created a helpful community.

Django has created a lot of libraries of its own, but not any for testing. It doesn’t mean that Django doesn’t support testing, it most certainly does. They have a complete section dedicated to [testing](https://docs.djangoproject.com/en/3.0/topics/testing/). Python itself provides a great testing library for Django, so it wouldn't be very practical to develop a testing library.

## Installing Django 🌩

1. Install pip. The easiest is to use the standalone pip installer.

2. Take a look at virtualenv and virtualenvwrapper. These tools provide isolated Python environments, which are more practical than installing packages systemwide.

3. After you’ve created and activated a virtual environment (you do not need a virtual environment, but it is highly suggested).

Enter the command:

```sh
pip install django
```

> You can also download it from GitHub directly

```sh
git clone https://github.com/django/django.git
```

## Articles

- [Django vs. Flask in 2019: Which Framework to Choose](https://testdriven.io/blog/django-vs-flask/)
- [Uses of Django](https://www.educba.com/uses-of-django/)
- [When to choose Django](https://www.netguru.com/blog/when-to-choose-django)
- [Django Interview Questions](https://career.guru99.com/top-16-django-interview-questions/)
- [Top 10 Django mistakes](https://www.toptal.com/django/django-top-10-mistakes)
- [Creating custom template tags in Django](https://www.pythoncircle.com/post/42/creating-custom-template-tags-in-django/)
- [How to host Django app on Pythonanywhere for Free](https://www.pythoncircle.com/post/18/how-to-host-django-app-on-pythonanywhere-for-free/)
- [How to make a blog with Django](https://www.skysilk.com/blog/2017/how-to-make-a-blog-with-django/)

## Thanks

Thanks to these awesome [contributors](https://github.com/endormi/awesome-dj/blob/master/AUTHORS.md#contributors) for helping with this repository.
