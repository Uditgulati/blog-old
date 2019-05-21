---
layout: post
title:  "GSoC project introduction: Adding features to NMatrix core"
date:   2019-05-21
---

Google Summer of Code is an annual global program focused on bringing more student developers into open source software development. Students work with an open source organization on a 3 month programming project. 

I applied to the program under the SciRuby organization with the project titled "Improving NMatrix: Adding features to NMatrix core". I am thankful to ScriRuby for giving me the opportunity to work on this project during summer as part of GSoC. I am also thankful to my mentor Prasun Anand for guiding me so far and for helping me complete my proposal in time.

Detailed proposal can be found [here](https://docs.google.com/document/d/1MR01QZeX_8h7a16nmkOYlyrVt--osB1Yg9Vo0xXYtSw/). 

### Brief introduction to NMatrix

NMatrix is a fast numerical linear algebra library for Ruby, with dense and sparse matrices, written mostly in C and C++ (and with experimental JRuby support). It supports dense matrices as well as two types of sparse (linked-list-based and Yale/CSR). NMatrix currently relies on ATLAS/CBLAS/CLAPACK and standard LAPACK for several of its linear algebra operations.


### My project

NMatrix's backend is currently written in C and C++ with some parts of the backend in Ruby too. This has made NMatrix to be a bit slower for some operations and also some parts of code base are not much readable. The project is being re-implemented from scratch by ScriRuby contributors here at [https://github.com/prasunanand/nmatrix_reloaded](https://github.com/prasunanand/nmatrix_reloaded) with backend written completely in C. This will make the project more efficient and the code more uniform and readable.

Summary of my project outcomes:

+	Adding support for **sparse matrices** (COO, CSR, CSC, Dia).
+	Adding **N-dimensional matrix support** which includes indexing, iterating, slicing and blradcasting.
+	Adding **linear algebra support which** includes implementation of BLAS and LAPACK routines.
+	**Integration with iruby notebooks** which includes writting methods such as pretty_print and taking care of some use cases.

This is my first blog regarding my GSoC 2019 progress. I'll be writing more such posts on this blog in near future. A blog post will be written each week giving a brief overview of the work done during that week.