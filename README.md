# Pytorch Example

This project is a playground for my first tests with Pytorch. Its purpose is mainly to provide a setup doc and sample code for myself. 

## Setup

As Platform Win10 is used

Guide:
https://pytorch.org/get-started/locally/

Package Manager:
https://chocolatey.org/

### Python3

I'm not sure if this is necessary because conda also installs its own python. 

```
choco install python
```

### Conda & Pytorch

Command line package and environment manager

1. Install Conda

    ```
    choco install anaconda3
    ```

2. Get a conda prompt 

    In ``C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Anaconda3 (64-bit)`` are the shortcuts to the conda prompts
    
    ``` 
    %windir%\System32\WindowsPowerShell\v1.0\powershell.exe -ExecutionPolicy ByPass -NoExit -Command "& 'C:\tools\Anaconda3\shell\condabin\conda-hook.ps1' ; conda activate 'C:\tools\Anaconda3' "
    %windir%\System32\cmd.exe "/K" C:\tools\Anaconda3\Scripts\activate.bat C:\tools\Anaconda3
    ```
    
    In the conda prompt you can use all commands to configure your enviroment. https://conda.io/projects/conda/en/latest/user-guide/cheatsheet.html

3.  Create an enviroment for pytorch

    ```
    conda info
    conda create --name pytorch python=3.8
    conda activate pytorch
    conda install pytorch torchvision cpuonly -c pytorch
    ``` 

    Use https://pytorch.org/get-started/locally/ to generate your script

4. Test installation

    Open python console for the environment
          `C:\tools\Anaconda3\python.exe`
    
    ```
    from __future__ import print_function
    import torch
    x = torch.rand(5, 3)
    print(x) 
    ```
    ```
    import torch
    torch.cuda.is_available()
    ```

Windows Terminal configs

```
{
      "guid": "{dc604a02-f778-415b-91bf-c05105efcfdb}",
      "hidden": false,
      "name": "Conda Powershell",
      "commandline": "C:\\tools\\Anaconda3\\startPowershell.bat"
    },
    {
      "guid": "{840f8468-2c6f-4239-ba65-b349ecf4f7f4}",
      "hidden": false,
      "name": "Conda Python",
      "commandline": "C:\\tools\\Anaconda3\\python.exe"
    }
```

startPowershell.bat: `powershell.exe -ExecutionPolicy ByPass -NoExit -Command "& 'C:\tools\Anaconda3\shell\condabin\conda-hook.ps1' ; conda activate 'C:\tools\Anaconda3' "`


### PyCharm

1. new Python Project
2. Project Intepreter C:\tools\Anaconda3\envs\pytorch\python.exe




