# Vagrant File for Data Science Env based on python

I create a data science environment on vagrant for study and testing with Python.
With this vagrant, we make a virtualbox vm - Ubuntu 16.04.
The VM has some python based softwares that is the most popular python components.

I reference a article - [15 Python Libraries for Data Science](https://www.upwork.com/hiring/data/15-python-libraries-data-science/)


Installed softwares are following

- python (2.7)
- ipython (5.1.0)
- jupyter (1.0.0)
- jupyter-client (4.4.0)
- jupyter-console (5.0.0)
- numpy (1.11.2)
- Pillow (3.4.1)
- scikit-learn (0.18)
- scipy (0.18.1)
- Scrapy (1.2.0)
- seaborn (0.7.1)
- bokeh (0.12.3)
- matplotlib (1.5.3)
- networkx (1.11)
- nltk (3.2.1)
- notebook (4.2.3)
- pandas (0.19.0)
- Pattern (2.6)
- Pillow (3.4.1)
- pip (8.1.2)
- tensorflow (0.11.0rc0)
- virtualenv (15.0.3)


# commands for quickstart

- Precondition
  - git, Vagrant and Virtualbox should be installed in target host OS.

- Building Vagrant Box
  - Clone repository from github/taewanme
  - Build image of vagrant from Vagrantfile
    - build time: about 10minute

```bash
> git clone git@github.com:taewanme/vagrant4DS.git
> cd vagrant4DS
> vagrant up
```

- login into the vagrant box

```bash
> vagrant ssh
'''

- startup of jupyter in the vagrant box

```bash
ubuntu@ubuntu-xenial:~$ ./jupyter.sh
[I 10:22:20.197 NotebookApp] Writing notebook server cookie secret to /run/user/1000/jupyter/notebook_cookie_secret
[W 10:22:20.205 NotebookApp] WARNING: The notebook server is listening on all IP addresses and not using encryption. This is not recommended.
[W 10:22:20.205 NotebookApp] WARNING: The notebook server is listening on all IP addresses and not using authentication. This is highly insecure and not recommended.
[I 10:22:20.209 NotebookApp] Serving notebooks from local directory: /vagrant/ipythons
[I 10:22:20.209 NotebookApp] 0 active kernels
[I 10:22:20.209 NotebookApp] The Jupyter Notebook is running at: http://[all ip addresses on your system]:9999/
[I 10:22:20.210 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[I 10:22:45.187 NotebookApp] 302 GET / (192.168.33.1) 0.67ms
```
