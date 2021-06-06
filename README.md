# Creating my own templates in portainer

## Resources
* [Deploy Portainer](https://portainer.readthedocs.io/en/latest/deployment.html)
* [Documentation](https://portainer.readthedocs.io)

## Ways to create your own templates
1. Create JSON file where you can describe your template: https://portainer.readthedocs.io/en/latest/templates.html
2. Upload this file in GitHub for example so that you can access it with URL
3. Example templares.json here: https://raw.githubusercontent.com/lhoangphuong/portainer-custom-template/main/templates.json

### Using the settings section in Portainer UI 
1. docker run -d -p 9000:9000 -p 8000:8000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
2. access Portainer by pointing your web browser at http://DOCKER_HOST:9000
3. in portainer UI you go in Settings and write URL with your templates
<p align="center">
  <img title="portainer" src='https://raw.githubusercontent.com/lhoangphuong/portainer-custom-template/main/CAPTURE.png' />
</p>

### Using --templates flag 
1. docker run -d -p 9000:9000 -p 8000:8000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer --templates http://my-host.my-domain/templates.json
2. On the place of  http://my-host.my-domain/templates.json you should write URL with your JSON file. 
This way of adding your templates in portainer works without going to settings in portainer UI.
Documentation about it you find here: https://portainer.readthedocs.io/en/latest/configuration.html#use-your-own-templates 
