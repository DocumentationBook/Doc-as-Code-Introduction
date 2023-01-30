.. _intro:

Introduction
############

Take a look at some top-level terminology the process as a whole.


Doc-as-code meaning
======================

First of all, the documentation is treated similar to programs in the following aspects:

*  Documentation source files are stored in a version control system.
*  The code is reviewed by various reviewers (managers, developers, analysts, technical writers, and others).
*  Documents are tested for accuracy and functionality. Especially it concerns code examples, links
   sequence of operations, and other practical parts.
*  Documentation artifacts are produced and published automatically.


Benefits
========

Doc-as-code is a partial implementation of the `literate programming <http://www.literateprogramming.com/>`_ paradigm,
which is based on close binding between documentation and program code.
This paradigm means that documentation goes first, and between the documentation
paragraphs goes the program code that implements the process described in the documentation.
For the program documentation, the main benefit of it is that it makes a program much more clear,
so that it is easier to maintain with all technical and commercial advantages this entails.

Very important is that literate programming involves developers into the documenting process,
because they can create and maintain the documentation in the same files where their code exists.

Program documentation is not the only type of documentation of course.
The main difference for other types of documentation is that the documentation source code is created separately
from the code. All other aspects are the same.


Documentation types
===================

*  Long term: concepts, FAQ, user's guides, getting started, and others
*  Reference: API, SDK, man pages, and others.


Documentation toolsets
======================

*  Generators of static documentation
*  Generators of documents from program source: pydoc, Javadoc, and others.
*  Generators of documents from configuration files and other metadata: Swagger toolset.



