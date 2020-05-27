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
                                      
                                      
# High Availability for Network 網路設備的熱備援

 
                                    Internet

                                        |

                                   Modem （數據機）

                                        |

                                SW layer 2 （交換機第二層）

                                        |
                                       / \
                                    
    SW layer 1 （交換機第一層）< master >     SW layer 1 （交換機第一層）< backup >      
                                 
                                       |
                                    
                                     DMZ Port

                                        |

                               Virtual Network (虛擬網段)
                               
# High Availability for Server 主機設備的熱備援


                                    App
                                 
                                     |
                                  
                                  Host 主機
                                 
                                      |
                                  
                               Virtual Disk 虛擬硬碟
                              
                                      |
                                  
                              Data (Tiers) 資料分層
                           
                                      ｜
                  ------------------------------------------
                   |            |             |             |
               
                 Flash           SAS          SATA         Cloud
            
        faster <-----------------------------------------------> Slower
     
    frequently <-----------------------------------------------> less frequently
            

                       

# DMZ 邊界網路/對外網路

條件：無法存取內部網路。

作法：在 DMZ 內的主機能與同處 DMZ內 的主機能和外部網路的主機通信，而同內部網路主機的通信會被受到限制。這使DMZ的主機能被內部網路和外部網路所存取，而內部網路又能避免外部網路所得知。

優勢：能抵抗外部入侵。

劣勢：不能抵抗內部破壞。



   
