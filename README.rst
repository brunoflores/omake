======
omake
======

Example
-------

Input:

.. code::

    project hello
        executable [src/main.c]


Output:

.. code::

    ninja_required_version = 1.10

    cflags = -Wall

    rule cc
      command = gcc $cflags -o $out $in

    build hello: cc ../src/main.c
