# handson_tutorial

This package holds the documentation of the moveit_handson package.

The source files of the tutorial, which are `.rst` files, locate in the `./doc` folder. The documentation is created with [rosdoc_lite](http://wiki.ros.org/rosdoc_lite) tool using [sphinx](http://www.sphinx-doc.org/en/master/index.html) engine.

In order to build and read the documents, the user need to install `rosdoc_lite` and `sphinx` at first.

Install `rosdoc_lite`:

```shell
apt-get install ros-{%ROSVERSION%}-rosdoc-lite
```

Install `Sphinx`:

```shell
sudo apt-get install python-sphinx
```

Build the document:

```shell
source path_to_your_ros_workspace/devel/setup.bash

roscd handson_tutorial

rosdoc_lite -o build .
```

If the document files were built successfully, open the file `./build/html/index.html` with a normal web browser, then the tutorial will be displayed.

###### *Any security issue should be reported using process at https://01.org/security*
