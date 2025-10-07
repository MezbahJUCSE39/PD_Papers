# LLM Environment in Cluster

## Initial Steps
     setenv ENV_PREFIX $HOME/conda-envs/llms
     mkdir -p $HOME/conda-envs

## See list of environments
     $ conda env list

## Create environment in conda
     conda create -n <env_name> python=<version>
     conda create -n torch110 python=3.9 -y
     conda activate torch110


## To activate this environment, use

     $ conda activate /aul/homes/misla093/conda-envs/llms

## Run Jupyter notebook with continuous run
     $ nohup jupyter notebook --no-browser --port=8888 > jupyter.log 2>&1 &

     Explanation:
          nohup → keeps the process alive even after you disconnect.
          --no-browser → avoids opening a browser on the remote machine.
          --port=8888 → use any free port (e.g., 8888, 8890, 9000, etc.).
          > jupyter.log 2>&1 & → redirect logs to jupyter.log and run in background.

## To deactivate an active environment, use

     $ conda deactivate
## OPEN AI
https://platform.openai.com/docs/overview
