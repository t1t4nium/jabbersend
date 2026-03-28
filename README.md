# jabbersend

jabbersend is a Ruby script to send XMPP (jabber) messages.

Original script by Harisankar P S (https://github.com/coderhs) at
https://github.com/xmpp4r/xmpp4r/blob/master/data/doc/xmpp4r/examples/basic/jabbersend.rb

## Setup

Prerequisites


- Ruby 2.5.8+
- RubyGems


Example, to install Ruby and RubyGems on FreeBSD:


    pkg inst devel/ruby-gems


Then, install `xmpp4r` gem:


    gem install --user-install xmpp4r


Install the script


    mkdir ~/bin
    git clone https://github.com/t1t4nium/jabbersend.git jabbersend
    cp jabbersend/jabbersend ~/bin/
    chmod 700 ~/bin/jabbersend


Settings

Edit `~/bin/jabbersend` and fill `myJID` and `myPassword`


    # settings
    myJID = 'user@example.com'
    myPassword = 'securepassword'
    ##########


Check if `$HOME/bin` is in your `$PATH`


    echo $PATH | grep $HOME/bin


If isn't the case, add it according to your shell. Example for Bash:


    PATH=$PATH:$HOME/bin; export PATH


## Usage

The script will send a jabber message to the specified JID by the `-t` option.
The subject can be specified using the `-s` option, and the body can be
specified using the `-b` option. If the body is omitted, it will be taken from
stdin on run.

Send a message


    jabbersend -t dest@example.com -s "This is a test" -b "Hello, how are you?"


or by this way


    echo "Today is a beautiful day!" | jabbersend -t dest@example.com -s "This is another test"


Help


    jabbersend -h



