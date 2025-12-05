# Steps to access from shell

✅ From now on, the workflow is:

git pull origin main (to get the latest updates)

Make edits locally

git add .

git commit -m "message"

git push origin main



# Access cluster from Shell

Step 1:
ssh -J misla093@wolf.cs.fiu.edu misla093@asterix.cs.fiu.edu
SSH pearl.cs.fiu.edu
Step 2: 
Password: 
Step 3:
set prompt = “%”;

# See list of existing environments
conda env list

Step 3: Create environment
conda create --name openAI_env python=3.8 numpy pandas
Step 4:
conda activate env_name

# To active jupyter notebook in cluster
nohup jupyter notebook --no-browser --port=9954 --ip=0.0.0.0
