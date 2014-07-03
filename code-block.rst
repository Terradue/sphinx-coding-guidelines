Code block R
------------

.. container:: context-run-executable

  .. code-block:: r

    # this is a test
    install.packages("ff")
    library("ff")
    print("Hello World!")
    
.. container:: context-run-executable

  .. code-block:: r

    #!/usr/bin/Rscript --vanilla --slave
    #Norbert Billet - IRD
    #2013/08/30: Norbert - Initial edit
    #Atlas_i1_SpeciesByOcean : build a graph of catches by ocean and by year
    
    #52North WPS annotations
    # wps.des: id = Atlas_i1_SpeciesByOcean, title = IRD tuna atlas indicator i1, abstract = Graph of species catches by ocean;
    # wps.in: id = WFS_URL, type = string, title = WFS URL, abstract = WFS URL;
    # wps.in: id = WFS_layer, type = string, title = WFS layer name, abstract = WFS layer name;
    # wps.in: id = OGC_filter, type = string, title = XML OGC Filter, abstract = XML OGC Filter;
    # wps.out: id = file_path, type = string, title = Output file, abstract = Path to the graph picture in png format;
    
    #norbert
    #personal comments
    WFS_URL <- "http://mdst-macroes.ird.fr:8080/constellation/WS/wfs/tuna_atlas"
    WFS_layer <- "ns11:i1i2_mv"
    OGC_filter <- "%3Cogc%3AFilter%20xmlns%3Aogc%3D%22http%3A%2F%2Fwww.opengis.net%2Fogc%22%20%0Axmlns%3Agml%3D%22http%3A%2F%2Fwww.opengis.net%2Fgml%22%3E%0A%20%20%20%20%20%3Cogc%3APropertyIsEqualTo%3E%0A%20%20%20%20%20%20%20%20%3Cogc%3APropertyName%3Especies%3C%2Fogc%3APropertyName%3E%0A%20%20%20%20%20%20%20%20%3Cogc%3ALiteral%3EYFT%3C%2Fogc%3ALiteral%3E%0A%20%20%20%20%20%3C%2Fogc%3APropertyIsEqualTo%3E%0A%3C%2Fogc%3AFilter%3E"
    
    if(! require(IRDTunaAtlas))
    {
    	stop("Missing IRDTunaAtlas library")
    }
    
    gml_file_path <- WFS2GMLFile(WFS_URL, WFS_layer, OGC_filter)
    
    file_path <- Atlas_i1_SpeciesByOcean(gml_file_path)

Code block bash

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
