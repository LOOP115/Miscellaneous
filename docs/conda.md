## CLI for setup a new env in Anaconda

conda create --name [env name] python=[version]

conda activate [env name]


conda install -c anaconda ipykernel

python -m ipykernel install --user --name=[env name]

jupyter notebook