// map node:
http://localhost:8080/wmts/gm_layer/gm_grid/{level}/{x}/{y}.png


  
gps:


roslaunch '/home/rvl/guosheng/mapviz/src/nmea_navsat_driver/gpsnode.launch' 

rosrun nmea_navsat_driver nmea_serial_driver _port:=/dev/ttyUSB1 _baud:=9600

roslaunch '/home/rvl/guosheng/mapviz/src/gps_umd/gps_common/launch/fix_translator.launch' 



systemctl restart docker

1.
sudo docker run -p 8080:8080 -d -t -v ~/mapproxy:/mapproxy danielsnider/mapproxy


2.  
roslaunch mapviz mapviz.launch



sudo service docker restart







