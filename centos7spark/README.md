# Learning Spark

You can clone the repository, get into this folder and follow below instructions to setup Virtual Machine and use it.

## Technologies Provided

Here are the technologies that are setup on this virtual machine.

* Python 2.7
* Python 3.6
* Hadoop 3.2.1
* Spark 2.4.5

## Usages

Here are some of the usages of the Virtual Machine.

* Learn Spark using Jupyter Lab environment.
* Prepare for CCA 175 Spark and Hadoop Developer Certification using Python or Scala.

In case you don't have enough resources to practice, you can sign up for our [labs](https://labs.itversity.com).

## Starting Virtual Machine

Here are the instructions to start Virtual Machine.

* Make sure you are inside the folder `centos7spark`.
* Run `vagrant up` to bring up the Virtual Machine.
* You can connect to Virtual Machine by saying `vagrant ssh`.
* By default you will be logged in as user `vagrant`.
* Most of the stuff in the virtual machine are owned by `vagrant`.
* `vagrant` can sudo as root and can perform any task in the virtual machine.

## Starting Services

Here are the instructions to start the services.

* HDFS - `start-dfs.sh`
* YARN - `start-yarn.sh`
* You can run `jps` to see all the relevant processes running.
* You can also run `hdfs dfs -ls /user/vagrant` to confirm HDFS is up and running.

## Stopping Virtual Machine

Here are the instructions to stop the virtual machine.

* You need to make sure that all the services are gracefully stopped.
  * HDFS - `stop-dfs.sh`
  * YARN - `stop-yarn.sh`
* You can validate by running `jps`, it should list any of the HDFS or YARN Components.
* You can come out of the virtual machine by running `exit` command.
* Once you are back to `centos7spark` folder, you can say `vagrant halt` to bring down the virtual machine.

## Using retail_db dataset

As part of the virtual machine the data is made available in local file system of Virtual Machine.

* Location: `/data/retail_db`.
* We can copy `/data/retail_db` into HDFS location `/public` by saying `hdfs dfs -put /data/retail_db /public`.
* You can validate by running `hdfs dfs -ls /public/retail_db`. You should start seeing the folders related to retail_db such as **orders**, **order_items** etc.

## Launching Jupyter Lab

Lab is setup with Jupter Lab with following Kernels.

* Python 3
* Pyspark 2
* Apache Toree - Scala (Spark)
* Apache Toree - SQL (Spark SQL)

Here are the instructions to run jupyter lab.

* Run `jupyter lab --ip 0.0.0.0`
* Go to the browser and enter - `http://localhost:8888`
* Copy the Token that is generated on the terminal in the login page and login.
* You will see bare minimum content to begin with.

## Using Content from GitHub

At ITVersity, we not only provide Virtual Machine, we also provide content to practice. Here are the details about using the content to practice Spark especialy for CCA 175.

* Click [here](https://github.com/dgadiraju/itversity-books/) to visit official repository for all ITVersity Notebooks.
* Visit appropriate folders and click on the Notebook.
* Once the Notebook is opened you can copy paste the code into the virtual machine or any other environment you want to practice.
* Keep in mind that you might have to make some adjustments such as using appropriate paths of your environment to access the data.

## Accessing Content Locally

On top of providing Virtual Machine we are also planning to open source our high quality content. Here are the instructions to clone it in the Virtual Machine.

* Make sure you are in the virtual machine under `/home/vagrant`.
* If you run `ls -ltr` you will see a folder by name `itversity-books`.
* You can get into the folder by running `cd itversity-books`.
* Run `git pull` to get latest content as of date. Keep in mind that it might replace existing books, if you made any changes.

## Spark - Getting Started

TBD
