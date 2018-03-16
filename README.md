# Setup Spark Environment on Mac

Download Spark from the offical [website](https://spark.apache.org/downloads.html). I am using Spark release 2.0.2, Pre-built for Apache Hadoop 2.7 and later.

Using the Terminal, move the tar-ball from Downloads to your home directory

```
cd Downloads/

mv spark-2.0.2-bin-hadoop2.7.tar ~

```

Extract the tar-ball in home directory:
```
cd ~

tar xzf spark-2.0.2-bin-hadoop2.7.tar
```
Create softlink to spark shell:
```
ln -s spark-2.0.2-bin-hadoop2.7 spark
```
In case you update your spark version to a later one, you may just change this.

Set bash_profile environment:

```
sudo vim ~/.bash_profile
```

Update with the following in the .bash_profile:

```
#SPARK

export SPARK_HOME="/Users/YOUR_USER_NAME/spark"
export PATH="$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin"
```
Source your bash_profile
```
source ~/.bash_profile
```
Ensure you have Java [runtime](https://www.java.com/en/download/mac_download.jsp) and [development kit](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) installed on the system.
# Verify Installation:

```
spark-shell
```
<kbd>
  <img src="/spark_shell_verify.png">
</kbd>

```
pyspark
```
<kbd>
  <img src="/pyspark_verify.png">
</kbd>

Download Zeppelin from the official [website](https://zeppelin.apache.org/download.html). I am using zeppelin release 0.7.3, the binary for all technologies.

Using the Terminal, move the tar-ball from Downloads to your home directory

```
cd Downloads/

mv zeppelin-0.7.3-bin-all.tar ~

```

Extract the tar-ball in home directory:
```
cd ~

tar xzf zeppelin-0.7.3-bin-all.tar
```
Create softlink to spark shell:
```
ln -s zeppelin-0.7.3-bin-all zeppelin
```
In case you update your spark version to a later one, you may just change this.

Set bash_profile environment:

```
sudo vim ~/.bash_profile
```

Update with the following in the .bash_profile:

```
#ZEPPELIN
export ZEPPELIN_HOME="/Users/YOUR_USER_NAME/zeppelin"
alias zeppelin_start="$ZEPPELIN_HOME/bin/zeppelin-daemon.sh start"
alias zeppelin_stop="$ZEPPELIN_HOME/bin/zeppelin-daemon.sh stop"
```
Source your bash_profile
```
source ~/.bash_profile
```
