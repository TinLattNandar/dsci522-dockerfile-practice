# dsci522-dockerfile-practice

1. Create the environment.yml

```python
name: docker-practice
channels:
  - conda-forge
  - defaults
dependencies:
  - pandas=2.2.2
  - pandera=0.20.4
  - python=3.11
  - pip
  - pip:
    - deepchecks==0.18.1

```

3. Run the following command
```bash
conda-lock --kind explicit --file environment.yml -p linux-64
```
   
3. Create the Dockerfile and run this
```bash
docker build --platform=linux/amd64 --tag assignment2
```
4. Run the docker image
```bash
docker run --rm -it assignment2 /bin/bash
```
