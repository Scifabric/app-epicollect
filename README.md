PyBossa and EpiCollect project for Air Quality
==================================================

This is a demo project that can be used to analyze and categorize data
points from an EpiCollect project.

This project shows how you can integrate in a PyBossa server: *volunteer
sensing* and *volunteer computing* in one project.

The EpiCollect tool is a project that can be installed in an Android
device. Then, you can load a project and take geotagged pictures as well as
answer several questions, if the project has a form.

Then, the uploaded data via the volunteers, it can be analyzed in a PyBossa
server. In this case, the volunteers will help also in measuring the area of
the submitted lichen pictures.

This procedure will allow to estimate teh quality of the air for a given area,
based on the size of the reported and validated lichens.

![](http://i.imgur.com/AQYEwDZ.png)

Testing the project
=======================

You need to install pybossa-pbs. If you don't have a virtual environment,
we recommend you to create one, and activate it:

```bash
    $ virtualenv env
    $ source env/bin/activate
```

Then, you can install pybossa-pbs:

```bash
    $ pip install pybossa-pbs
```

Or if you prefer:

```bash
    $ pip install -r requirements.txt
```

## Creating an account in a PyBossa server

Now that you've all the requirements installed in your system, you need
a PyBossa account:

*  Create an account in your PyBossa server (use [Crowdcrafting](http://crowdcrafting.org) if you want).
*  Copy your API-KEY (you can find it in your profile page).

## Configure pybossa-pbs command line

PyBossa-pbs command line tool can be configured with a config file in order to
avoid typing the API-KEY and the server every time you want to take an action
on your project. For this reason, we recommend you to actually create the
config file. For creating the file, follow the next steps:

```bash
    $ cd ~
    $ editorofyourchoice .pybossa.cfg
```

That will create a file. Now paste the following:

```ini
[default]
server: http://yourpybossaserver.com
apikey: yourapikey
```

Save the file, and you are done! From now on, pybossa-pbs will always use the
default section to run your commands.

## Create the project

Now that we've everything in place, creating the project is as simple as
running this command:

```bash
    $ pbs create_project
```

## Add the task presenter, tutorial and long description

Now let's add to our project the required templates to show a better description
of our project, to present the tasks to our users, and a small tutorial for the volunteers:

```bash
    $ pbs update_project
```

## Add the tasks from an Epicollect project

First, go to your recently created project page. You should find it on
http://yourpybossaserver/project/your-project-short-name. From there, you should
be able to import the tasks from the EpiCollect Project: lichens (form Lichen).

For more information about how to import tasks from an Epicollect project, please
check the [documentation](http://docs.pybossa.com/en/latest/user/overview.html?highlight=epicollect#importing-the-tasks-from-an-epicollect-plus-public-project).

Done!

**NOTE**: we provide templates also for Bootstrap v2 in case your PyBossa
server is using Bootstrap2 instead of Bootstrap3. See the rest of the files.

Documentation
=============

We recommend that you read the section: [Build with PyBossa](http://docs.pybossa.com/en/latest/build_with_pybossa.html) and follow the [step by step tutorial](http://docs.pybossa.com/en/latest/user/tutorial.html).

**NOTE**: This project uses the [pybossa-pbs](https://pypi.python.org/pypi/pybossa-pbs) library in order to simplify the development of the project and its usage. Check the [documentation](https://github.com/PyBossa/pbs).

LICENSE
=======

Please, see the COPYING file.


Acknowledgments
===============

The thumbnail has been created using a [(http://www.flickr.com/photos/benetd/134314157/)photo] from benet2006 (license CC BY 2.0).
