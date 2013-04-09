PyBossa and EpiCollect application for Air Quality
==================================================

This is a demo application that can be used to analyze and categorize data
points from an EpiCollect project.

The application shows a picture of a lichen and asks the user to classify it
according to several categories, as well as measure the size of the lichen to
extrapolate the quality of the air in a given area.

![](http://i.imgur.com/D2dj9Ng.png)

Testing the application
=======================

You need to install the pybossa-client first (use a virtualenv):

```bash
    $ pip install pybossa-client
```
Then, you can follow the next steps:

*  Create an account in PyBossa
*  Import the tasks from the EpiCollect Project: lichens (form Lichen)
*  Open with your browser the Applications section and choose the epicollect app. This will open the presenter for this demo application.

Please, check the full documentation here:

http://docs.pybossa.com/en/latest/user/create-application-tutorial.html

The thumbnail has been created using a photo from benet2006 (license CC
BY 2.0). 
Check the original photo [here](http://www.flickr.com/photos/benetd/134314157/)  

Note
====
The createTasks.py script can be used to update the templates of the
application, not for getting the tasks as you can do that directly in the
PyBossa server.
