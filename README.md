apt-cacher-box
==============

What do it do?
------------------

This is a teensy standalone vagrant box that acts as a central cache for all your hits to the ubuntu apt servers. It makes iterating fast on Vagrantfiles a fair bit less painful if you're using ubuntu.

For now, you've got to be able to figure out what network adaptor you should bridge to, and you have to copypasta the resulting IP address into the config for whatever other boxes you want to point at this. Yeah, this sucks. Looks like there's no way around that yet, but I hope to find one eventually.
