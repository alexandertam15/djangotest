This command:
$ heroku config:set DISABLE_COLLECTSTATIC=1 
must be ran in the build for it to work, it was having a few difficulties inside heroku but when run manually through terminal with this command it works. Also, I was having difficulties using Jenkins on my laptop as it would not work for some reason so I integrated a python scripting code to test if the tests ran successfully by checking if " no issues " was in the output of os.popen('python3 ./manage.py test').read().  This allows for me to check if there were any failures in the test run and I printed to the user that there was an error and quit the program if there was any failures. This test code can be found inside ./git/hooks/pre-commit. ./git/hooks/pre-push also has a manual version of pushing to Heroku commented out as I integrated the deployment pushing into Heroku through the website. 
