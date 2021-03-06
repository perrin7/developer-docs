Enable SSH
==========

1.  Connect to your sphere using USB

.. code-block:: bash

	# OS X
	screen /dev/cu.usbmodem*
	# Linux
	screen /dev/ttyACM0


2.  Use default username and password
::

	username: ninja
	password: temppwd

3.  Change the default ninja password

Before enabling ssh, it is good practice to change the default password of the ninja account to something less well-known, so:
::

	sudo with-rw passwd ninja  # type the current password once and the new password twice

Don't forget the new password - if you do forget it, you will need to factory reset the sphere to reset it.

4.  Install ssh for easier access
::

	sudo with-rw bash -c "apt-get update -y && apt-get install -y openssh-server"