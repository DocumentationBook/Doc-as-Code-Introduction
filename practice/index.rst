.. _practice:

Practice
########


Using Docker
============

Docker enables you to separate document processing tools from the document content. You can share a specific
container image with your team or make it public, so that any one can just run document processing with one Docker
command.


Docker commands
===============

If you have a Docker image in your repository at a URL <path>/<docker_image>,
use a ``docker`` command on your host to run the documentation processing inside a docker container similar to this::

   $ docker container -it --rm --name <container_name> --mount type=bind,source=$PWD/<src_dir>,target=/<dst_dir> \
      <path>/<docker_image> <doctool_command> <doctool_arguments>

This command does the following:

#. Downloads (if not exists locally) the specified image ``<docker_image>``.
#. Creates a new container named ``<container_name>``.
#. Runs the container.
#. Mounts the source working folder ``$PWD/<src_dir>`` to the container's working folder ``/<dst_dir>``.
   This example uses the ``$PWD`` environment variable to determine the absolute path to your current folder on the host.

   .. warning:: Ensure that you are in the correct working folder,
      as the documentation toolset is able to create or even modify
      and delete some files and folders depending on the command you requested.

#. The ``it`` option instructs Docker to allocate a pseudo-TTY connected to the container’s stdin.
   It starts an interactive bash shell in the container. So you will get to this shell console immediately after
   the container starts.
#. The ``rm`` option instructs Docker to remove the container when you exit it.
#. After the container is created, it starts your custom command. For example, you can run one of Sphinx commands
   using  the ``sphinx-build`` or ``make`` utility, such as::

      $ make clean
      $ make dirhtml
      $ make spelling
      $ make linkcheck

