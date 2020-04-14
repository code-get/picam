# picam
An interface to control the Raspberry Pi Cameras

## How to configure the SD Card for a PiCAM

From the control machine run the following to configure the SD Card

```
ansible-playbook -i '127.0.0.1,' playbooks/sdcard.yml
```

## How to Generate Encrypted Password

```
python -c 'import crypt; print crypt.crypt("This is my Password", "$1$SomeSalt$")'
```


