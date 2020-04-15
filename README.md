# picam
An interface to control the Raspberry Pi Cameras

## How to configure the SD Card for a PiCAM

From the control machine run the following to configure the SD Card

```
ansible-playbook -i '127.0.0.1,' playbooks/sdcard.yml --ask-vault-pass
```

## Bootstrap the PiCAMs

### How to Generate Encrypted Password

```
python -c 'import crypt; print crypt.crypt("This is my Password", "$1$SomeSalt$")'
```

### Setup the RSA Keys

```
ssh-copy-id pi@192.168.86.200
ssh-copy-id pi@192.168.86.201
```

### Run the Ping Test

```
ansible-playbook -i inventory playbooks/ping.yml
```

### Run the Bootstrap Playbook

```
ansible-playbook -i inventory playbooks/bootstrap.yml
```

### Run the initial Update

```
ansible-playbook -i inventory playbooks/update.yml
```
### Run a Reboot

```
ansible-playbook -i inventory playbooks/reboot.yml
```

## Install Motion and Enable Camera

```
ansible-playbook -i inventory playbooks/site.yml
```

