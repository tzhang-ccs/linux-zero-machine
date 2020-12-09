# linux-zero-machine

- miniconda
- zsh
    - conda install zsh

    ```bash
    conda install -c conda-forge  zsh
    ```

    - set zsh as the default shell by adding the following commands in .bash_profile 
    ```bash 
    export SHELL=/home/tzhang/soft/zsh/bin/zsh
    exec /home/tzhang/soft/zsh/bin/zsh -l
    
    ```

    - oh-my-zsh

    ```bash
    sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```

- vim

    ```bash
    alias vi=vim

    vim
    PlugInstall
    ```

- install package
    - install jupyterlab and extension
    > reference of TOC: https://github.com/jupyterlab/jupyterlab-toc 

    ```bash
    #base

    conda install jupyterlab
    
    conda install -c conda-forge nodejs
    jupyter labextension install @jupyterlab/toc
    
    jupyter labextension install @jupyterlab/jupyterlab-spreadsheet
    jupyter labextension install @jupyterlab/git
    ```
    - install general libraries
    
    ``` bash 
    conda install  -c conda-forge netcdf4
    conda install  -c conda-forge   nco
    conda install  -c conda-forge  cdo
    conda install  -c conda-forge  ncview
    conda install  -c conda-forge  tmux
    ```
    
    - install CDAT
    > reference: https://github.com/CDAT/cdat/wiki/install
    
    - create a new environment called as luffy
    ``` bash 
    #luffy
    conda create -n luffy
    python -m ipykernel install --user --name  luffy
    conda install  -c conda-forge -c cdat/label/v8.2.1 cdat
    conda install numpy
    conda install  psutil
    conda install -c conda-forge   cartopy
    conda install -c conda-forge netcdf4
    conda install -c conda-forge cmocean
    conda install  scikit-learn
    conda install statsmodels
    ```

    - install R 
    
    ```R
    R
    install.packages("pcalg", lib = "~/soft/R", repos='http://cran.us.r-project.org')
    install.packages("BiocManager", lib = "~/soft/R", repos='http://cran.us.r-project.org')
    
    library(BiocManager,lib.loc="~/soft/R")
    BiocManager::install('ggm', lib = "~/soft/R")
    ```
