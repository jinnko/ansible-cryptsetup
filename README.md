## [![DebOps](https://debops.org/images/debops-small.png)](https://debops.org) cryptsetup

<!-- This file was generated by Ansigenome. Do not edit this file directly but
     instead have a look at the files in the ./meta/ directory. -->

[![Travis CI](https://img.shields.io/travis/debops/ansible-cryptsetup.svg?style=flat)](https://travis-ci.org/debops/ansible-cryptsetup)
[![test-suite](https://img.shields.io/badge/test--suite-ansible--cryptsetup-blue.svg?style=flat)](https://github.com/debops/test-suite/tree/master/ansible-cryptsetup/)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-debops.cryptsetup-660198.svg?style=flat)](https://galaxy.ansible.com/debops/cryptsetup)


`debops.cryptsetup` allows you to configure encrypted filesystems on top of
any given block device using [dm-crypt][]/[cryptsetup][] and [LUKS][].  A random
keyfile generated on the Ansible controller will be used for the encryption by
default.  It is your responsibility that the keyfile is kept secure for this to
make sense.  For example by storing the keyfile on an already encrypted
filesystem (both on the Ansible controller and the remote system).

[LUKS]: https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup
[dm-crypt]: https://en.wikipedia.org/wiki/Dm-crypt
[cryptsetup]: https://gitlab.com/cryptsetup/cryptsetup

### Features

* Create a random keyfile or use an already existing keyfile.
* Manage `/etc/crypttab` and `/etc/fstab` and mount point directories.
* Create a LUKS header backup and store it on the Ansible controller.
* Decrypt and mount an encrypted filesystem and never store any key material on
  persistent storage on the remote system. You might need to take care of your
  Swap space yourself for this!
* Setup an encrypted swap space (with random key or with persistent key).
* Setup filesystems using a random key on boot.
* ``cryptsetup`` plain, LUKS, TrueCrypt and VeraCrypt mode.
* Multiple ciphers and corresponding keys chained to encrypt one filesystem.

### Installation

This role requires at least Ansible `v2.2.3`. To install it, run:

```Shell
ansible-galaxy install debops.cryptsetup
```

### Documentation

More information about `debops.cryptsetup` can be found in the
[official debops.cryptsetup documentation](https://docs.debops.org/en/latest/ansible/roles/ansible-cryptsetup/docs/).


### Role dependencies

- `debops.secret`

### Are you using this as a standalone role without DebOps?

You may need to include missing roles from the [DebOps common
playbook](https://github.com/debops/debops-playbooks/blob/master/playbooks/common.yml)
into your playbook.

[Try DebOps now](https://debops.org/) for a complete solution to run your Debian-based infrastructure.





### Authors and license

- [Robin Schneider](https://docs.debops.org/en/latest/debops-keyring/docs/entities.html#debops-keyring-entity-ypid) (maintainer) | [e-mail](mailto:ypid@riseup.net) | [GitHub](https://github.com/ypid)

License: [GPL-3.0](https://tldrlegal.com/license/gnu-general-public-license-v3-%28gpl-3%29)

***

This role is part of [DebOps](https://debops.org/). README generated by [ansigenome](https://github.com/nickjj/ansigenome/).
