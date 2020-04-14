# picam
An interface to control the Raspberry Pi Cameras

## How to Generate Encrypted Password

```
python -c 'import crypt; print crypt.crypt("This is my Password", "$1$SomeSalt$")'
```
