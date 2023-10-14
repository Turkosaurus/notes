---
SSH
---

# SSH

## Local Addresses
* Pi: `turkosaurus@192.168.1.219`
* Max: `user@192.168.1.129`

## Setting up public and private keys

### Generate key
`ssh-keygen -t -[encryption method]`

### Connect to Server
`ssh user@host`

---

## Common Commands
`chown` -- change owner \
`scp` -- OpenSSH secure file copy \
`sshd` -- ssh daemon process that monitors for connection requests

---

## Key Locations
* `/.ssh/id_[encryption method]`
* `/.ssh/id_[encryption method].pub`
* `.ssh/id_[encryption method]_[id]`.
* `.ssh/authorized_keys`*

*(encryption methods = [`rsa`, `ed25519`])*

> *Note: Save unique keys with id for each use case to facilidate revocation

---

## Setting up SSH
[github video](https://www.youtube.com/watch?v=8X4u9sca3Io)
[other overview](https://www.youtube.com/watch?v=v45p_kJV9i4)

1. Generate _public_ and private Keys on local machine
> `ssh-keygen` -t ed25519 -C example@email.com
- `-t` type of encryption
- `-C` comment

1. Startup `ssh-agent`
> `eval "$(ssh-agent -s)"`

1. Check for existing file in
> `~/.ssh/config`

1. Create new file if none exists
> `code ~/.ssh/config`

```
Host *
  AddKeysToAgent yes
  IdentityFile ~/.ssh/id_ed25519
```

1. Add key
> `ssh-add ~/.ssh/id_ed25519`

1. Pull public key
> `cat ~/.ssh/ided25519.pub`

1. Test connection
> `ssh -T git@github.com`

1. Share public key to connected machine
> `ssh-copy-id`

outdated: `scp [file] [location]`

Add public key to `.ssh/authorized_keys` on server
Connect to server
* say hello to server
* server creates challenge from public key
* requester uses private key to solve challenge
* requester sends hashed proof to server

**Congratulations! You may now utilize your SSH connection.**
