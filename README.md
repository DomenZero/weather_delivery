# Weather delivery

#### Start Ansible yml
```bash
# sudo ansible-playbook ansible-docker_weather.yml --extra-vars "API_KEY=111 CITY_NAME=Honolulu"
```
#### Docker Start
```bash
# docker build -t weather_delivery:dev .
# docker run --rm weather_delivery:dev --api_key 111 --city_name Honolulu
Source: openweathermap
City: Honolulu
Description: few clouds
Temperature: 300.68
Humidity: 58
Pressure: 1016
```
#### Test on CentOS7 (without Docker)
```bash
# sudo yum install python3-pip
# sudo pip3 install requests
# python3 weather_delivery.py --api_key 1111 --city_name Honolulu
Source: openweathermap
City: Honolulu
Description: few clouds
Temperature: 299.09
Humidity: 51
Pressure: 1019
```
#### Delete all images
```bash
docker rmi $(docker images -q) -f
```
