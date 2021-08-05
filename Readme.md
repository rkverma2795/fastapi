# Setup instruction Task_builder

Clone the application on local 

`git clone `


## To Run and test application with Docker

### Docker setup and application run

    Install docker and docker-compose in system.
    
    docker-compose build
    docker compose up

### Test application with docker 
    
    Go To docker container:
    1) run "Docker ps" to get all the container running 
    2) Go to container bash by command 
        "docker exec -it task_builder_web_1 bash"
    3) Run test run "pytest"

    

### Setup postgres
`change username, password, host and name in src/database.py file`

### Create and activate virtual env with python3.9

`virtualenv venv -p python3.9` 

`source env/bin/activate`

### install the requirements
`cd src`

` pip install -r requirements.txt`

### Run main.py

`python main.py`

### To Run Test cases

`pytest`


## Api Details

    Get TODO List:
    URl: localhost:8000/
    Method: GET


    POST TODO:
    URl: localhost:8000/to-do/
    Method: POST
    Request Parameter: 
        {
            "title":<title>,
            "description":<description>
        }

    UPDATE TODO:
    URl: localhost:8000/to-do/
    Method: PUT
    Request Parameter: 
        {
            "id":<id>
            "title":<title>,
            "description":<description>
        }

    Get single TODO:
    URl: http://localhost:8000/to-do/{todo_id}
    Method: GET

    Delete TODO:
    URl: http://localhost:8000/to-do/{todo_id}
    Method: DELETE