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

 
                                Internet
                                
                                    |
                                    
                                  Modem （數據機）
                                  
                                    |
                                    
                                SW layer 2 （交換機第二層）
                                
                                    |
                                    
                                SW layer 1 （交換機第一層）
                                 
                                    |
                                    
                                 DMZ Port
                                 
                                    |
                                    
                              Virtual Network (虛擬網段)

# DMZ 邊界網路/對外網路

條件：無法存取內部網路。



   
