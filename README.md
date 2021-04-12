# DelayScheduling


### Required Software
* Python 3.7
```bash
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get update
sudo apt-get install python3.7
```
* OpenMPI 
```bash
sudo apt-get install openmpi-bin openmpi-doc libopenmpi-dev
```

* Virtualenv
```bash
sudo apt install python3.7-dev python3-pip
sudo pip3 install -U virtualenv
virtualenv --system-site-packages -p python3.7 ./venv
source ./venv/bin/activate  # sh, bash, ksh, or zsh
pip install --upgrade pip
```

### Copy and paste RLSkip source code
Unzip the source code package.

### Install Dependencies
```shell script
cd RLSkip
pip install -r requirements.txt
```
### Training
To train a RL model based on a job trace, run this command:
 
```bash
python rl-skip.py --workload "./data/some_data.swf" --exp_name your-exp-name
``` 

### Monitor Training 

After running Default Training, a folder named `logs/your-exp-name/` will be generated under `./data`. 

```bash
python spinningup/spinup/utils/plot.py ./data/logs/your-exp-name/
```

It will plot the training curve.
