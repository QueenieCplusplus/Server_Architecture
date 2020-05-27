# Server Architecture

# Version 1.0.0

           
                                         (fetch data)
        Master ---------> ------------> write/read  --------------->   |-----------|
                       |                                               |           |
                       |---- Slave                                     |    DB     |
                       |                                               |           |
                       |---- Slave                                     |    HA     |
                       |                                               |           |         
                       |---- Slave                                     |-----------|         
                                                                              |
        API ------------> ------------> write/read ---------------> ---------->|   
                                      (fetch data)
