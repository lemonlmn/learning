# learning

## virtual environment 

### start new project

- create new ennvironment   
```conda create --name learning```

- activate the environment  
```conda activate learning``` 

- install packages  
  - basic data wrangling python package 
  ```conda install pandas```
  
  - jupyter
  ```conda install -c conda-forge jupyterlab```
  
  - R
  ```conda install -c conda-forge r-base=4.1.1```
  ```conda install -c conda-forge r-irkernel=1.2```
  ```
  R
  IRkernel::installspec(user = TRUE)  # specify for this 
  ```

### terminal open tool

- open Rstudio  
```open -na Rstudio```


### udpate conda

```conda update -n base conda``` 

### search 

```conda search r-base```
```conda search -c conda-forge r-base```
