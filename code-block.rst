Code block
-----

Code block R (default)
=====

.. code-block:: r

  # this is a test
  install.packages("ff")
  library("ff")
  print("Hello World!")

Code block R with run-executable context
=====

.. container:: context-run-executable

  .. code-block:: r

    # this is a test
    install.packages("ff")
    library("ff")
    print("Hello World!")


Code block bash (default)
=====

.. code-block:: bash

  # this is a test
  ls ok
  cat ok

Code block bash with run-executable context

.. container:: context-run-executable

  .. code-block:: bash

    # this is a test
    ls ok
    cat ok

Code block python (default)
    
.. code-block:: python

  print "Goodbye, World!"
    
Code block python with run-executable context
    
.. container:: context-run-executable

  .. code-block:: python

    print "Goodbye, World!"

Code custom

.. container:: context-custom
  
  This is a custom context

  .. code-block:: bash

    # this is a test
    ls ok
    cat ok
