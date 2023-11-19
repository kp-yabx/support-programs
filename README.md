# support-programs

### Installation

1. Clone the repository
2. Create a new directory - `/opt/oracle/`
3. Unzip the Instant client
````
cd /opt/oracle/
unzip /home/yabx/support-programs/linux/instantclient-basic-linux.x64-12.2.0.1.0.zip  
unzip /home/yabx/support-programs/linux/instantclient-sdk-linux.x64-12.2.0.1.0.zip 
unzip /home/yabx/support-programs/linux/instantclient-sqlplus-linux.x64-12.2.0.1.0.zip 
unzip /home/yabx/support-programs/linux/instantclient-tools-linux.x64-12.2.0.1.0.zip

# If /opt/oracle/instantclient12_2/libclntsh.so is not found, make a symbolic link to link the library
cd /opt/oracle/instantclient12_2
ln -s libclntsh.so.12.1 libclntsh.so
````
4. Export ENV variables
````
export ORACLE_HOME=/opt/oracle
export LD_LIBRARY_PATH=$ORACLE_HOME/instantclient_12_1
````
5. Add `gem 'ruby-oci8'` in Gemfile and bundle it

