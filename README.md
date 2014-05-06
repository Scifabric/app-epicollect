PyBossa and EpiCollect application for Air Quality
==================================================

This is a demo application that can be used to analyze and categorize data
points from an EpiCollect project.

This application shows how you can integrate in a PyBossa server: *volunteer
sensing* and *volunteer computing* in one application.

The EpiCollect tool is an application that can be installed in an Android
device. Then, you can load a project and take geotagged pictures as well as
answer several questions, if the project has a form.

Then, the uploaded data via the volunteers, it can be analyzed in a PyBossa
server. In this case, the volunteers will help also in measuring the area of
the submitted lichen pictures.

This procedure will allow to estimate the quality of the air for a given area,
based on the size of the reported and validated lichens.

![](http://i.imgur.com/AQYEwDZ.png)

Testing the application
=======================

You need to install the pybossa-client first (use a virtualenv):

```bash
    $ pip install -r requirements.txt
```
Then, you can follow the next steps:

*  Create an account in PyBossa (e.g. on http://crowdcrafting.org)
*  Change the name and short_name of the application in the app.json file to something new
*  Change all occurrences of 'airquality' in the template.html and tutorial.html file to your new short_name
*  Create the application by running: python createTasks.py -k API_KEY -s SERVER (e.g. http://crowdcrafting.org) -c
*  The command will give you a URL to import the tasks from your EpiCollect
   project
*  Import the tasks from the EpiCollect Project: lichens (form Lichen)
*  Open with your browser the Applications section and choose the epicollect app. This will open the presenter for this demo application.

Documentation
=============

We recommend that you read the section: [Build with PyBossa](http://docs.pybossa.com/en/latest/build_with_pybossa.html) and follow the [step by step tutorial](http://docs.pybossa.com/en/latest/user/tutorial.html).

**NOTE**: This application uses the [pybossa-client](https://pypi.python.org/pypi/pybossa-client) in order to simplify the development of the application and its usage. Check the [documentation](http://pythonhosted.org/pybossa-client/).


LICENSE
=======

Please, see the COPYING file.


Acknowledgments
===============

The thumbnail has been created using a [(http://www.flickr.com/photos/benetd/134314157/)photo] from benet2006 (license CC BY 2.0).

Note
====
The createTasks.py script can be used to update the templates of the
application, not for getting the tasks as you can do that directly in the
PyBossa server.
