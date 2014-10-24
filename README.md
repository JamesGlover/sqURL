sqURL - A Sequencescape Curl wrapper
------------------------------------

                 __
                  \ `-.
         __        )   \
      .-'  `-._.--'    |
     /               _/
    |    ___     __-'. .
    |   '   `---<___/|/|
    |     _          o  )
    |      \   /  ,     |
    \  `,   )  \  \-`-._|
     `-/   /---'>_/_\
     '-`-__`-. '"   "
           ""

Squirrel by Joshua Bell-
http://ascii.co.uk/art/squirrel

sqURL helps avoid the need to manually type all the cruft needed when talking to the Sequencescape API.
Usage:

    squrl (POST|GET) (local|production|staging_2|staging|next_release) <endpoint> ['<data>']

#Set-up

The first time you run sqURL it will create .squrl in your home directory. You must correctly
configure this file before you may use sqURL.

* *API_KEY* Your sequencescape api key
* *LOCAL_APP_KEY* This can mostly be left as is. Specifies the X_SEQUENCESCAPE_CLIENT_ID when connecting locally
* *PRODUCTION* Full url and port number for production environment
* *STAGING* Full url and port number for staging environment
* *STAGING_2* Full url and port number for staging_2 environment
* *NEXT_RELEASE* Full url and port number for next_release environment
* *TRAINING* Full url and port number for training environment
* *LOCAL* Can mostly be left as "http://localhost:3000", Full url and port number for local development environment
* *S2UAT* Full url and port number for s2_uat environment

#Finding your api key
- Log into Sequencescape
- Click your username in the top right hand corner
- Your API key will be present in the blue box towards the bottom of the screen

#Gotchas
Any json data will need to be enclosed in single quotes.
You will connect to the API with user-level privileges, unless you are connecting to a local instance of Sequencescape. This means many actions, such as creating state changes, will be forbidden.
