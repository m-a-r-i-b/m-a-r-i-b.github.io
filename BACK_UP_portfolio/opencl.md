---
title: "High Performance Computing with OpenCL"
excerpt: "OpenCL, C/C++, CMake"
header:
  teaser: /assets/images/opencl_01.jpg
date: "2019-12-31" 
---

## Introduction

This project explores the use of OpenCL in high performance computing for heterogenous platforms (i.e., CPU/GPU). We present updated C/C++ code adhering to OpenCL 2.0 standard for the exercises in the "OpenCL in Action" book by Matthew Scarpino. Read the [book](https://www.manning.com/books/opencl-in-action). It is a good comprehensive book, suitable for beginners, which teaches OpenCL beginning from the basics.

The following tools will be used in this project:
+ C/C++
+ OpenCL
+ CMake
+ Intel CPU - we can test our OpenCL code on a CPU without the need to have a GPU

## Code
Find the source code in the [repository](https://github.com/Adaickalavan/opencl).

## Learning Outcome
At the end of this project, we should be able to:
+ Use OpenCL in C/C++ for high performance computing. 
+ Build C/C++ code with CMake.

## Project Structure

The project structure is as follows:

```text
opencl                                 # Repository root
├── apps                               # Source code
|   ├── Ch1
|   |   ├── matvec.c                   # C source file
|   |   └── matvec.cl                  # Cl source file
|   ├── Ch2
|   |   ├── context_count.c            # C source file
|   |   ├── device_ext_test.c
|   |   ...
|   .
|   .
|   .
|   ├── Ch8
|   |   ├── buffer_test.cl             # Cl source file
|   |   ├── buffer_test.cpp            # C++ source file
|   |   ...
|   └── CMakeLists.txt                 # CMake build file
├── assets                             # Reference materials 
|   ├── libpng-1.4.0-manual.pdf      
|   ├── OpenCL device model.jpg      
|   ├── OpenCL operators.jpg
|   ├── OpenCL scalar data types.jpg
|   └── OpenCL vector data types.jpg
├── bin                                # Executables
|   ├── ...                              
|   ...
├── libs                               # Local libraries
│   └── util                     
|       ├── CMakeLists.txt             # Library-level CMake build file
|       ├── util.c                     
|       ├── util.cpp                   
|       ├── util.h                     
|       └── util.hpp                   
├── .dockerignore
├── .gitignore
├── CMakeLists.txt                     # Top-level CMake build file
└── README.md                                 
```

## Steps to get started with OpenCL
1. Install OpenCL SDK 
  + For Intel processors: [website](https://software.intel.com/en-us/opencl-sdk/choose-download)

1. Install and run `clinfo` to show complete information of OpenCL platforms and devices.
```bash
$ sudo apt install clinfo
$ clinfo
```

## Exercise list
For easy reference, the solution code is organised by chapter and named according to the exercise. 

Build the C/C++ code using:
```bash
$ cd /path/to/repository/root/opencl
$ cmake -E make_directory build
$ cmake -E chdir ./build cmake -DCMAKE_BUILD_TYPE=Release ..
$ cmake --build ./build
```

Run the desired code as follows. Assuming the desired code is `callback_8_6`, then run:
```bash
$ cd /path/to/repository/root/opencl
$ ./bin/callback_8_6
```

The complete code listing is given in the table below.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;border-color:#aaa;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:#aaa;color:#333;background-color:#fff;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:#aaa;color:#fff;background-color:#f38630;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-lboi{border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-1fpb{background-color:#fcfbe3;text-align:center;vertical-align:top}
.tg .tg-baqh{text-align:center;vertical-align:top}
.tg .tg-g30d{background-color:#FCFBE3;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-quxf{background-color:#ffffff;text-align:center;vertical-align:top}
.tg .tg-pnt8{background-color:#FCFBE3;text-align:center;vertical-align:middle}
.tg .tg-z9fv{background-color:#FCFBE3;border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
.tg .tg-hb2y{background-color:#FCFBE3;text-align:left;vertical-align:middle}
.tg .tg-yq6s{background-color:#FCFBE3;text-align:center;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 455px">
<colgroup>
<col style="width: 152px">
<col style="width: 152px">
<col style="width: 151px">
</colgroup>
  <tr>
    <th class="tg-c3ow">Chapter</th>
    <th class="tg-baqh">Exercise</th>
    <th class="tg-c3ow">Name</th>
  </tr>
  <tr>
    <td class="tg-g30d">1<br>Introducing OpenCL</td>
    <td class="tg-pnt8">1.1</td>
    <td class="tg-z9fv">matvec</td>
  </tr>
  <tr>
    <td class="tg-c3ow" rowspan="3">2<br>Host programming: fundamental data structures</td>
    <td class="tg-nrix">2.1</td>
    <td class="tg-lboi">platform_ext_test</td>
  </tr>
  <tr>
    <td class="tg-pnt8">2.2</td>
    <td class="tg-hb2y">device_ext_test</td>
  </tr>
  <tr>
    <td class="tg-nrix">2.3</td>
    <td class="tg-cly1">context_count</td>
  </tr>
  <tr>
    <td class="tg-g30d" rowspan="2">3<br>Host programming: data transfer and partitioning<br></td>
    <td class="tg-pnt8">3.2</td>
    <td class="tg-z9fv">buffer_test</td>
  </tr>
  <tr>
    <td class="tg-nrix">3.3</td>
    <td class="tg-cly1">map_copy</td>
  </tr>
  <tr>
    <td class="tg-quxf" rowspan="5">4<br>Kernel programming: data types and device memory</td>
    <td class="tg-pnt8">4.1</td>
    <td class="tg-hb2y">hello_kernel</td>
  </tr>
  <tr>
    <td class="tg-nrix">4.2</td>
    <td class="tg-cly1">double_test</td>
  </tr>
  <tr>
    <td class="tg-pnt8">4.3</td>
    <td class="tg-hb2y">float_config</td>
  </tr>
  <tr>
    <td class="tg-nrix">4.4</td>
    <td class="tg-cly1">vector_widths</td>
  </tr>
  <tr>
    <td class="tg-pnt8">4.5</td>
    <td class="tg-hb2y">vector_bytes</td>
  </tr>
  <tr>
    <td class="tg-1fpb" rowspan="7">5<br>Kernel programming: operators and functions</td>
    <td class="tg-nrix">5.1</td>
    <td class="tg-cly1">op_test</td>
  </tr>
  <tr>
    <td class="tg-pnt8">5.2</td>
    <td class="tg-hb2y">id_check</td>
  </tr>
  <tr>
    <td class="tg-nrix">5.3</td>
    <td class="tg-cly1">mod_round</td>
  </tr>
  <tr>
    <td class="tg-pnt8">5.4</td>
    <td class="tg-hb2y">polar_rect</td>
  </tr>
  <tr>
    <td class="tg-nrix">5.5</td>
    <td class="tg-cly1">mad_test</td>
  </tr>
  <tr>
    <td class="tg-pnt8">5.6</td>
    <td class="tg-hb2y">shuffle_test</td>
  </tr>
  <tr>
    <td class="tg-nrix">5.7</td>
    <td class="tg-cly1">select_test</td>
  </tr>
  <tr>
    <td class="tg-quxf" rowspan="6">7<br>Events, profiling, and synchronization</td>
    <td class="tg-pnt8">7.2</td>
    <td class="tg-hb2y">callback</td>
  </tr>
  <tr>
    <td class="tg-nrix">7.3</td>
    <td class="tg-cly1">user_event</td>
  </tr>
  <tr>
    <td class="tg-pnt8">7.6</td>
    <td class="tg-hb2y">profile_read</td>
  </tr>
  <tr>
    <td class="tg-nrix">7.7</td>
    <td class="tg-cly1">profile_items</td>
  </tr>
  <tr>
    <td class="tg-pnt8">7.8</td>
    <td class="tg-hb2y">atomic</td>
  </tr>
  <tr>
    <td class="tg-nrix">7.9</td>
    <td class="tg-cly1">mutex</td>
  </tr>
  <tr>
    <td class="tg-yq6s" rowspan="7">8<br>Development with C++</td>
    <td class="tg-pnt8">8.1</td>
    <td class="tg-hb2y">full_context_8_1</td>
  </tr>
  <tr>
    <td class="tg-nrix">8.2</td>
    <td class="tg-cly1">create_kernels_8_2</td>
  </tr>
  <tr>
    <td class="tg-pnt8">8.4</td>
    <td class="tg-hb2y">buffer_test_8_4</td>
  </tr>
  <tr>
    <td class="tg-nrix">8.5</td>
    <td class="tg-cly1">map_copy_8_5</td>
  </tr>
  <tr>
    <td class="tg-pnt8">8.6</td>
    <td class="tg-hb2y">callback_8_6</td>
  </tr>
  <tr>
    <td class="tg-nrix">8.7</td>
    <td class="tg-cly1">user_event_8_7</td>
  </tr>
  <tr>
    <td class="tg-pnt8">8.8</td>
    <td class="tg-hb2y">profile_8_8</td>
  </tr>
</table>