# MQTT Sample Server for c++17 based on mqtt_cpp library with Boost.Asio

## Requirements

Library depends on [Boost](https://www.boost.org/) > 1.67 and [mqtt_cpp](https://github.com/redboltz/mqtt_cpp)

To install boost libraries on ubuntu:
```
sudo apt install libboost1.67-dev
```

## Compilation

Clone the repository with submodules
```
$ git clone --recursive git@github.com:frozen-eye/mqtt_srv.git
```

Build and install mqtt_cpp library

```
$ cd mqtt_srv/libs/mqtt_cpp
$ mkdir build && cd build && cmake ..
$ make && sudo make install
```

To build the project:
```
$ cd mqtt_srv && mkdir build
$ cd build && cmake .. && make
```

Run the server listen on port 9999:
```
cd mqtt_srv/build && mqtt_srv 9999
```
