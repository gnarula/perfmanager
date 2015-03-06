#perfmanager
Mozilla perfomance alerts manager
##Ubuntu 14.04 Development Build Instructions
    #retrieve latest apt-get list
    $sudo apt-get update

    #Install virtualenv and pip
    $sudo apt-get install python-pip python-virtualenv
    
    #Fork perfmanager
    http://github.com/<your_user_name>/perfmanager

    #Clone your forked repo
    $git clone https://github.com/<your_user_name>/perfmanager.git

    #Create and activate a virtualenv
    $virtualenv venv
    $source venv/bin/activate

    #Install the dependencies
    $cd perfmanager
    $pip install -r requirements.txt
    
    #Rename local_settings_sample.py to local_settings.py and update the details  

    #Instantiate database
    $python manage.py syncdb

    #Populate with dummy alerts data
    $python manage.py loaddata initial_data.json
    
    #Start the development server
    $python manage.py runserver



