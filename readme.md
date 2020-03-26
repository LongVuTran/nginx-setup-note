# move static folder -> share folder
sudo bindfs -u www-data -g www-data /root/downloads/boxes/ /usr/share/nginx/root_boxes

# log error
sudo tail -30 /var/log/nginx/error.log

# gunicorn restart
sudo service gunicorn restart

# ngix restart
sudo service ngix restart