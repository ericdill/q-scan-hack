q-scan-hack
-----------

Basically this works by

#. find a peak
#. copy motor positions to spec computer
#. find another peak
#. copy motor positions to spec computer
#. do some other spec stuff
#. do an hkl scan in simulation mode via a for loop. Something like this ::

    def foo '
      for(kk=1; kk<10; kk++){
        hh = 1+kk/10
        ubr hh 0 0
        wh
      }
    '

#. parse the spec file and get motor positions
#. do a scan with bluesky from the parsed spec file
