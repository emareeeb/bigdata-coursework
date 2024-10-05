
# ⚡ Apache Spark Setup Script

This Bash script automates the process of setting up **Apache Spark 3.5.3** on your machine. It covers everything from cleaning up old installations to installing necessary dependencies and configuring Spark for seamless use! 🚀

## 📋 Features
- Automatically removes previous Spark installations.
- Installs **Scala** and **Git** (if not already installed).
- Downloads and configures **Apache Spark 3.5.3** with **Hadoop 3** support.
- Adds environment variables for easy Spark usage.
- Runs an example Spark job to verify installation.
- Includes handy commands to start and stop Spark services.

## 🚀 Installation Steps
1. **Update and upgrade** your system packages:
    ```bash
    sudo apt-get update -y
    sudo apt-get upgrade -y
    ```

2. **Download and run** the `spark.sh` script:
    ```bash
    wget [your-script-url] -O spark.sh
    chmod +x spark.sh
    ./spark.sh
    ```

3. **Configure environment** variables:
    The script automatically appends Spark-specific environment variables to your `.bashrc`:
    ```bash
    export SPARK_HOME=/opt/spark
    export PATH=$PATH:$SPARK_HOME/bin
    export PYSPARK_PYTHON=/usr/bin/python3
    ```

## 🛠 How It Works
- The script **cleans up any previous Spark installations** by searching for directories starting with `spark-` and removes them.
- It **installs Scala and Git** as these are necessary for running Spark.
- Downloads the Spark 3.5.3 tarball and **extracts** it into `/opt/spark`.
- Ensures that the Spark binaries (like `pyspark`, `spark-shell`, etc.) are executable.
- **Runs an example Spark job** (`SparkPi`) to test the installation and outputs the result.

## 📦 Commands to Manage Spark
- **Start Spark**:
    ```bash
    /opt/spark/sbin/start-all.sh
    ```

- **Stop Spark**:
    ```bash
    /opt/spark/sbin/stop-all.sh
    ```

## 📊 Verifying Installation
After running the script, if you see output similar to:
```bash
Master running at <URL>
Worker running at <URL>
```
🎉 **Congrats! Your Spark setup is complete!**

You can further verify by running:
```bash
jps
```
If you see the **Master** and **Worker** listed, everything is working as expected! ✅

---

Feel free to download and run the script to get started with Spark effortlessly! ✨
