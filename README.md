# Server Architecture

# Version 1.0.0

           
        Master -------------------------> write/read  ---------------> |-----------|
              |                                                        |           |
              |---- Slave                                              |    DB     |
              |                                                        |           |
              |---- Slave                                              |    HA     |
              |                                                        |           |         
              |---- Slave                                              |-----------|         
                                                                              |
        API -------------------------> write/read ---------------> -----------|   
