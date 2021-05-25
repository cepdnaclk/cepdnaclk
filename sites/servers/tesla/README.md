# tesla.ce.pdn.ac.lk Server

This is a GPU server of the Department of Computer Engineering, University of Peradeniya. 

The administrator changes will be documented [here](https://github.com/cepdnaclk/server-documentation-public).

You can use this server using the LDAP login for ce.pdn.ac.lk undergraduates (which is used for CO top floor lab, aiken and tesla) without sudo access.

## FAQ

### How can I connect to this server?

You can use ssh login. [This](https://ce-pdn-ac-lk.com/cewiki/server_use:use_of_servers) is a good set of instructions on the matter. If it is not clear (or unaccessible), contact dhanushki.mapitigama[at]eng.pdn.ac.lk 

### What is the Hardware Configuration of this server?
* Intel(R) Core(TM) i7-6700K CPU @ 4.00GHz (8MB Cache, 8 threads)
* 32 GB Memory
* Tesla C2075 GPU (6GB DDR5 Memory, 448 CUDA Cores, Compute Capability 2.0)

###  What is the operating system of this server?

Ubuntu 14.04.5 LTS

### What software is in installed in this server?
* MySQL : Students can request login to use the MySQL server for their projects.
* Apache server: Students can request web server space for their projects.



### How can I run a Jupyter Notebook on the server and access it over the internet?

1. Create a conda environment with jupyter notebook package installed.
2. Activate that environment.
3. Run <code>jupyter notebook --generate-config</code>
4. It will say the configuration file for your account. Edit the configuration file and add the following two lines. (They are originally commented out as given below.)
```
# c.NotebookApp.allow_origin = ''
# c.NotebookApp.ip = 'localhost'
c.NotebookApp.allow_origin = '*'
c.NotebookApp.ip = '0.0.0.0'
```
5. Save the configuration file. You should still be in the conda environment.
6. Run the jupyter notebook. <code>jupyter-notebook --no-browser</code>
7. You will see a URL like this <code>http://SOMETHING:8888/tree?token=abc123def456</code>
8. Type the following address into your PC browser <code>http://tesla.ce.pdn.ac.lk:8888/tree?token=abc123def456</code>
9. Your browser (on your PC) will be showing the jupyter notebook running on the tesla server.

###  Can I install some software here?

Please request through any [CO staff member](http://www.ce.pdn.ac.lk/academic-staff/). Please note that the server admin has no authority to install something unless it is requested by a staff memeber.

### What can I do if my doubt is not listed here?

Ask the [admin](../admin/).

### What software is installed in this server?

### I am not an undergraduate of the Department of Computer Engineering, University of Peradeniya. Can I use this server?

Ask headce[at]eng.pdn.ac.lk.

### I broke something. What should I do?

Write an [email](../admin/) if this is not urgent. If not [call](../admin/).