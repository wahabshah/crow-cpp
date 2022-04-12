
# Motivation

<a href="https://gitpod.io/#https://github.com/wahabshah/crow-cpp" rel="nofollow noopener noreferrer" target="_blank" class="after:hidden"><img src="https://gitpod.io/button/open-in-gitpod.svg" alt="Open in Gitpod"></a>

* This repository contains a server using [CROW C++ framework](https://crowcpp.org/)
* This framework is made by the company which made the famous Python Flask
* This framework uses Boost Asio in the background

## Build Echo Server Iteration1
```sh
rm -rf build && mkdir -p build && \
(cd build && cmake -DCMAKE_BUILD_TYPE=Debug .. && make clean all VERBOSE=1) && \
./build/crow-server
```

```sh
curl http://localhost:18080
Hello World
```

# Links

* https://github.com/ipkn/crow
* https://github.com/CrowCpp/Crow