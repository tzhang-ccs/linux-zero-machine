# linux-zero-machine

1. miniconda
2. zsh
    1. conda install zsh

    ```bash
    conda install -c conda-forge  zsh
    ```

    1. set zsh as the default shell

    ```bash
    export SHELL=/home/tzhang/soft/zsh/bin/zsh
    exec /home/tzhang/soft/zsh/bin/zsh -l

    in .bash_profile
    ```

    1. oh-my-zsh

    ```bash
    sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```

    1. vim

    ```bash
    alias vi=vim

    vim
    PlugInstall
    ```

3. install package

    ```bash
    #base

    conda install jupyterlab
    jupyter labextension install @jupyterlab/toc
    jupyter labextension install @jupyterlab/jupyterlab-spreadsheet
    jupyter labextension install @jupyterlab/git

    conda install  -c conda-forge netcdf4
    conda install -c conda-forge nodejs
    conda install  -c conda-forge   nco
    conda install  -c conda-forge  cdo
    conda install  -c conda-forge  ncview
    conda install  -c conda-forge  tmux

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

    ```R
    R
    install.packages("pcalg", lib = "~/soft/R", repos='http://cran.us.r-project.org')
    install.packages("BiocManager", lib = "~/soft/R", repos='http://cran.us.r-project.org')
    
    library(BiocManager,lib.loc="~/soft/R")
    BiocManager::install('ggm', lib = "~/soft/R")
    ```
