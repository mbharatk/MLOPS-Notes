MLOps is a set of practices taht aim to deploy and maintain machine learning models in production reliably and efficiently.

MLOPS = Machine Learning + DevOps + Data Engineering 

#### Web server:

Client ------Request (GET, POST)------->Server
CLient <------Response (text, JSON ect)------Server

*   Client = Curl, Python/requests, Web browser
*   Server = EC2, Virtualbox, any remotely managed machine

List of Web Servers tools: 
*   Virtualbox, AWS EC2, GCP CLoud Compute
*   SSH
*   Python: Jupyter-lab, Pandas, Pytorch, Pickle, Requests, FLask, Poetry
*   CLI Commands: ls, cd, sudo, sudo apt*, curl, screen, ssh-keygen, chmod

#### hands-on:
    $python -m venv venv
    $source venv/bin/activate
    $pip3 install jupyterlab/jupyter
    $jupyter lab



### mlops code examples:

    $cd flask_examples_regression
    $vi flask_simple_regression_service.py and remove import pickle & save
    $python flask_simple_regression_service.py
    $flask not available, downloaded flask using pip3 install flask
    run the "python flask_simple_regression_service.py" again


#### use the following commands to check how the generated ip address works

    import requests

    #response = requests.get("hhtp://theja.org")
    for input_feature_vector in range(10):
        response = requests.get(f"http://127.0.0.1:5000/?x={input_feature_vector}")
        print(response.json())

    response

    response.json()

    response.text
