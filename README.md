# MySQL lab

In this example:

* MySQL standalone server is deployed

Tasks:

0. Adjust sandbox name `3nk45yqd6e` as necessary for your sandbox
1. Provision MySQL root password secret either manually,
   with `kubectl create secret generic -n sandbox-name-goes-here mysql-standalone-secrets --from-literal=rootPassword=$(cat /dev/urandom | base64 | head -c 30)`
   or using
   https://git.k-space.ee/k-space/generated-secret-operator
2. Using kubectl forward the router instance port to your local laptop and attempt
   to connect using MySQL command line utilities
3. Attempt to load `employees.sql` from https://github.com/datacharmer/test_db
   using the forwarded port
4. Verify using phpMyAdmin that the content got loaded into MySQL server
5. Deploy your favourite application that uses MySQL
