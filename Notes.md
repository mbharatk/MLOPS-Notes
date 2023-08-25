#### MLOps is a set of practices that aim to deploy and maintain machine learning models in production reliably and efficiently.

`MLOPS = Machine Learning + DevOps + Data Engineering`

Web server:
--------------

Client ------Request (GET, POST)------->Server
Client <------Response (text, JSON etc)------Server

*   Client = Curl, Python/requests, Web browser
*   Server = EC2, Virtualbox, any remotely managed machine

#### List of Web Servers tools: 
*   Virtualbox, AWS EC2, GCP CLoud Compute
*   SSH
*   Python: Jupyter-lab, Pandas, Pytorch, Pickle, Requests, FLask, Poetry
*   CLI Commands: ls, cd, sudo, sudo apt*, curl, screen, ssh-keygen, chmod


Setting up the required environment (Python, Jupyter):
---------------------------------------------------------------

 To begin with, install [python](https://www.python.org/) and create a virtual environment, activate it and then install [jupyter lab](https://jupyter.org/) by using the following commands

    $python -m venv 'yourpreferredvitualenvname'
    $source venv/bin/activate (for mac) | $yourpreferredvirtualevname\scripts\activate (for windows)
    $pip3 install jupyterlab
    $jupyter lab

After the jupyter lab is opened in a web browser, open a terminal in it and use the following example,

### [Using a sample code from mlops code examples repo](https://github.com/mbharatk/mlops-code-examples.git)

 In this example, we used the flask regression sample code

    $cd flask_examples_regression
    $vi flask_simple_regression_service.py and remove import pickle & save
    $python flask_simple_regression_service.py
    $flask not available, downloaded flask using pip3 install flask
    run the "python flask_simple_regression_service.py" again


#### use the following commands in jupyter-lab python notebook to check how the server responds to the requests

    import requests

    #response = requests.get("hhtp://theja.org")
    for input_feature_vector in range(10):
        response = requests.get(f"http://127.0.0.1:5000/?x={input_feature_vector}")
        print(response.json())

    response

    response.json()

    response.text

