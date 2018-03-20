# SKU
An inventory management and tracking system built with Ruby on Rails 5.


### Set Enviroment Variables
 You need to set 6 enviroment variables, for emails to be delivered (for ActionMailer, password reset, etc).


| Enviroment Variable Names| Are                  |
| ------------            |:---------------------:|
| EMAIL_DOMAIN            | Domain of your email server     |
| EMAIL_USERNAME          | Username for your email (most of the time name@domain.tld)|
| EMAIL_PASSWORD          | Password for your email          |
| SMTP_SERVER         	  | Address for your smtp server     |
| EMAIL_SEND_FROM         | Email address where email will go out from |
| ACTION_MAILER_SEND_TO   | Email address which will receive email notifications on order create, cancel, renew, return |

You may have to further configure the SMTP delivery options. If so, edit this file ```config/environments/development.rb```

### Run the server
* Run ```rails s``` to start the server
* Without stoping the server, open another terminal window and run ```rake jobs:work``` (needed in order for ActionMailer to work and deliver emails)
* Visit http://localhost:3000
* Use ```padma@demo.com```  ```test@123``` for the email and password. Change the password and email once you login. Create more users via the Console.
