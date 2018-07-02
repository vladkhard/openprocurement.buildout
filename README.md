# openprocurement.buildout
Development Buildout of OpenProcurement

Follow the instructions:

  1. Bootstrap the buildout with bash:

     ```
     $ sh bootstrap.sh
     ```

  3. Activate virtualenv:

     ```
     $ source bin/activate
     ```

  2. Build the buildout:

     ```
     $ pip install -r requirements.txt && bin/buildout -N
     ```

System requirements (fedora 27):

     ```
     $ dnf install python bash-completion bind-utils couchdb file gcc git zeromq zeromq-devel libevent-devel libffi-devel libselinux-python libsodium libsodium-devel make openssl-devel policycoreutils-python python-devel python-virtualenv redhat-rpm-config redis sqlite-devel systemd-devel systemd-python
     ```

To start environment services:

     ```
     bin/circusd --daemon
     ```

To debug problems (if any) see `var/log/circus.log` and other `var/log/*.log` log files.

To to run openprocurement.api instance:

     ```
     bin/chaussette paste:etc/openprocurement.api.ini
     ```
