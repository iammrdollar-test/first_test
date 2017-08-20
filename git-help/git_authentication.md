# You can also use existing SSH key for all purposes

# Generate 4096 bit ssh key with a comment
$ ssh-keygen -t rsa -b 4096 -C "youremail@server.com"

# Give a passphrase and custom name (optional) to your ssh key

# Add private SSH key
$ ssh-add ~/.ssh/id_rsa

# Copy the SSH .pub key and paste it into your Github account SSH & GPS settings section
$ pbcopy < ~/.ssh/id_rsa.pub

# Confirm using your password

# Test Your SSH Connection
$ ssh -T git@github.com

# Hi username! You've successfully authenticated, but GitHub does not
# provide shell access.

# If you have any repo and it gives HTTP Error, remote add the repo again
$ git remote set-url origin git@github.com:iammrdollar-test/first_test.git
