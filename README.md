# Daily progress tracker API
 
django based api that can be run with docker

simple api with token based authentication


purpose:
I want to be able to log and view the answers to the following questions everyday
I want to make sure I answer these questions everyday as it is a good habit to do this.

It is a good habit to do this because it will help me make less mistakes and improve tomorrow what went bad today 

I will help me be greatful for all the things that went well today and help me see my past successes.

It will help me in reviewing after a few days months or years like james clear does it at 

I will try to make this open source so other people can also use this api and track their progress - they will need to setup a server though so I might in furture make this into more of a service delivered via an app for ios and android and the web but for now it is a basic API with basic email, password auth and generates a token.

Then they can simply store their data in the following models:


class ProgressLog(model.Models):
    good = models.TextField(blank=True)
    bad = models.TextField(blank=True)
    learning = models.TextField(blank=True)
    time = models.DateTimeField(auto = True)



with this we can add logs as they happen so dont have to wait for the day to be over to add a log - just add logs as they happen.

django admin can be used to delete logs.


user data will be stored in an sqlite db and should be easily backupable and restoreable - user may download a backup file and upload the same to restore their data.

POST
/api/add-good


/api/add-bad

/api/add-learn

GET
/api/get-all/{days}



