## file to keep track of the docker runs of the same image: captest-pipreq2

the branch 'container' has all the files for the initial docker containerization of the model apps.  it got so far as to work with the all-in-prediction that directly takes an input through the call, but not a user input.

renamed the other all-in-prediction-user-input to clearly indicate that includes a prompt for an input (not currently working)

docker run -d -i --name capcont-pipreq2i  -p 8000:8000 captest-pipreq2
docker run -d -i -t --name capcont-pipreq2it  -p 8000:8000 captest-pipreq2 #with this run i get the swagger interface to 'wait' for an input, but i do not know where to enter it...  after i close the run it shows that it was expecting the entry but it never came

uvicorn main:app --reload --workers 1 --host 0.0.0.0 --port 8000

