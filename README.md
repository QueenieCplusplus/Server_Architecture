# Server Architecture

# Version 1.0.0 範例伺服器架構圖

           
                                         (fetch data)
        Master ---------> ------------> write/read  --------------->   |-----------|
                       |                                               |           |
                       |---- Slave                                     |    DB     |
                       |                                               |           |
                       |---- Slave                                     |    HA     |
                       |                                               |           |         
                       |---- Slave                                     |-----------|         
                                                                              |
        API ------------> ------------> write/read ---------------> --------->|   
                                      (fetch data)
                                      
                                      
# High Availability 熱備援


