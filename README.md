# mysql-max-connections-script
**An assignment given to me during my internship**
What's This Script For?

This simple Bash script helps you increase the maximum number of connections in MySQL to 50,000. It waits 30 seconds before running to make sure MySQL has fully started, then applies the new setting.

What You Need Before Running It

Make sure MySQL is installed and running.

Run the script with a user that has permission to change MySQL settings.

How to Use It

Save the script as set_max_connections.sh.

Give it permission to run:

**chmod +x set_max_connections.sh**

Run it:

**./set_max_connections.sh**

How It Works

sleep 30: Pauses for 30 seconds so MySQL has time to start.

mysql -u root -p -e "SET GLOBAL max_connections = 50000;": Logs into MySQL as root and increases the connection limit.

exit 0: Ensures the script exits smoothly.

Things to Keep in Mind

Make sure MySQL is actually running before executing this script.

The root user needs the right permissions to change MySQL settings.

If you're running this script without interaction, you might need to modify it to include the MySQL password.

Troubleshooting

Permission issues? Try running it with sudo:

sudo ./set_max_connections.sh

MySQL isn't starting? Try increasing the sleep time.

Still not working? Check your MySQL config file (my.cnf) to see if max_connections is restricted.

This should help you smoothly increase your MySQL connection limit. Let me know if you run into any issues!


