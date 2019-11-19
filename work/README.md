# ZoKrates circuits

## Requirements
Install `cargo` by `curl https://sh.rustup.rs -sSf | sh`

## build
```
./do build
```

## example
```
cat examples/square.code > root.code
./do compile
./do setup
./do witness 3 9 
./do generate
```
