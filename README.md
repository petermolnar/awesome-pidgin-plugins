# awesome-pidgin-plugins

A list of Pidgin plugins to support modern networks and features

## Protocols and protocols extensions

### XMPP

#### [XEP-313](https://xmpp.org/extensions/xep-0313.html) Message Archive Management.

The XMPP support in Pidgin is extremely dated. There is a patched Pidgin source tree maintained at https://github.com/CkNoSFeRaTU/pidgin - you'll need to compile this for XEP-313 support. There is no plugin version.

#### [XEP-0280](https://xmpp.org/extensions/xep-0280.html) Message Carbons

Use https://github.com/gkdr/carbons

#### [XEP-0316](https://xmpp.org/extensions/xep-0316.html) MUC Eventing Protocol

Use https://github.com/danielkraic/Pidgin-XEP-0136-plugin

#### [XEP-0363](https://xmpp.org/extensions/xep-0363.html) HTTP File Upload

Use https://github.com/Junker/purple-xmpp-http-upload

#### [XEP-0384](https://xmpp.org/extensions/xep-0384.html) OMEMO Encryption

OMEMO is a multi-device 2e2 encryption protocol.
Use https://github.com/gkdr/lurch

#### [XEP-0184](https://xmpp.org/extensions/xep-0184.html) Message Delivery Receipts

Use https://github.com/noonien-d/pidgin-xmpp-receipts

### WhatsApp

https://github.com/hoehermann/purple-gowhatsapp is a new plugin that, unlike other Pidgin WhatsApp plugins, connects to the web interface of WhatsApp, so the possibility if immediately getting block is reduced.

### Telegram

 https://github.com/majn/telegram-purple 

### Matrix

https://github.com/matrix-org/purple-matrix/

Basic features only.

### Skype (web)

https://github.com/EionRobb/Skype4pidgin

Via the web interface. Might break soon due to the coming redesign (again....) of skype.

### Discord

https://github.com/EionRobb/purple-discord

### Pushbullet

 https://github.com/EionRobb/pidgin-pushbullet

### Mattermost

 https://github.com/EionRobb/purple-mattermost

### Instagram

 https://github.com/EionRobb/purple-instagram

Makes an actual login on login - notification noise might hapen -, and it is a bit messy on contact list terms, but seems to be working.

### Facebook

https://github.com/dequis/purple-facebook/

You'll need to compile it for normal Facebook, no special tricks. 

##### Facebook for Work (aka Workplace)

1. Download, compile and install:

        git clone https://github.com/dequis/purple-facebook.git
        git checkout wip-work-chat
        ./autogen.sh # you'll probably need to install additional packages...  
        sudo make install

2. Restart pidgin
3. Accounts → Manage Accounts → Add
    * Protocol: Facebook
    * Username: your email address
    * Password: wharrgarbl (it doesn't matter)
    * Remember password: yes
    * Advanced → Login as a Workplace account: yes
    * Save, Ok

In case you get [SSL/TLS errors on connect](https://github.com/dequis/purple-facebook/issues/408#issuecomment-374275285):

- Try Tools → Plugins → NSS Preferences → Maximum Version → TLS 1.2
- restart Pidgin

If that doesn't work, and you're on Linux, you can try recompile Pidgin without GnuTLS. If you do so, I suggest using https://github.com/CkNoSFeRaTU/pidgin - this is a Pidgin patched with XEP-0313, should that be ever needed - it's useful.

```
./configure --prefix=/usr --disable-perl --disable-nm --with-dynamic-prpls=jabber,irc --enable-gnutls=no
```

### ICQ (as 2019 ICQ)

https://github.com/EionRobb/icyque

Because ICQ started to abandon the old protocol.



## Other useful plugins

- https://github.com/EionRobb/pidgin-ignore-nickchange
- https://github.com/kgraefe/pidgin-znc-helper