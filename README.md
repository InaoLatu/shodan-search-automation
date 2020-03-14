# shodan-search-automation to .docx 
### Author: Inao Latourrette 
It builds an automatic search in Shodan (https://www.shodan.io/) and a exploits discovery search. 
The results obtained from the searches are represented in 2 .docx files and they are also printed by console.

## Requirements 

1. Install python3 and pip3: 
```
   sudo apt update
   sudo apt install python3-pip
   sudo apt-get install python3 
```

2. Install virtualenv:
``` pip3 install virtualenv ```

3. Create the virtualenv: 
``` virtualenv venv```

4. Activate virtualenv: ``` source venv/bin/activate```

5. Install requirements: 
``` pip install -r requirements.txt ```

## How to use the code 
In *main.py* you have to complete the code with your API_KEY and the searches you would like to make: 
``` 
SHODAN_API_KEY = ""  # Insert your SHODAN_API_KEY
api = shodan.Shodan(SHODAN_API_KEY)
query = 'webcam 7  -401 http.component:"mootools"'  # query for automatic_search()
exploits_query = 'webcam 7'  # for exploits_search()
```
After inserting the previous parameters the code is ready to use: 
``` python main.py ```
