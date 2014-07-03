Code block R
------------

.. container:: context-run-executable

  .. code-block:: r

    # this is a test
    install.packages("ff")
    library("ff")
    print("Hello World!")


Code block bash (default)

.. code-block:: bash

  # this is a test
  ls ok
  cat ok

Code block bash (with run-executable context)

.. container:: context-run-executable

  .. code-block:: bash

    # this is a test
    ls ok
    cat ok

Code block python
    
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
