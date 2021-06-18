![Image](https://www.iniciasoluciones.es/wp-content/uploads/2019/04/Logo_Inicia_2018.png)

# Grafana Dashboards

Current dashboards are valid only for xcally version 2.5.2 and higher. It has been tested in some grafana community versions.

### Dependencies

This grafana dashboards needs next dependencies

* [Grafana Server](https://grafana.com/) : Open source for nice dashboards.
* [Grafana Plugins](https://grafana.com/grafana/plugins/): Some awesome plugins for this great open source.
* [XCALLY Software](https://www.xcally.com/): Omnichanel Contact Center Software

### Installation

Grafana Server must have access to XCALLY database (or replica) so you'll need to open firewall ports and configure Mysql to accept connections from grafana. You'll have to decided by yourself if you can install Grafana in your XCALLY server or you need another one based on your server load:

 - Install Grafana Server

Depends on your server, you must to select the installation for this software. [Here](https://grafana.com/grafana/download?pg=get&plcmt=selfmanaged-box1-cta1) you can find diferent intall options bsed on debian, red hat and much more.

 - Install MySQL Connector and create a user

You must install the Mysql grafana plugin as this [link](https://grafana.com/grafana/plugins/mysql/) shows, and once you have installed it you need to connect to xcally database and create a user for grafana 

```sh
mysql -uroot -p
CREATE USER grafana@'my-grafana-server' IDENTIFIED BY 'grafana-pass';
```

 - Configure Grafana Datasource

Configure your MySQL Datasource with those credentials in section "Configuration" -> "Data Sources". Name this Data Source as XCALLY

##### Note: All dashboards have been configured with datasource 'XCALLY' so if data source name is different dashboards will not work.

 - Install Additional graphs plugins

This plugins require 3 additional plugins that can be easily installed from bash with next commands:

```sh
	grafana-cli plugins install farski-blendstat-panel
	grafana-cli plugins install grafana-piechart-panel
	grafana-cli plugins install grafana-piechart-panel
	systemctl restart grafana-server
```

- Upload grafana dashboards

Last step is upload grafana dashboards from the folder.

### Under construction

This repository is currently under construction so, some documentation about dashboards is not currently available...soon woulb be.


License
-----------

The present software is owned and managed by INICIA SOLUCIONES DE VOZ S.L.

All contents, brands, designs, logos, icons, software, trade names, domain names, and any other signs or elements susceptible to protection for intellectual and industrial property rights that are part of the software are property of INICIA SOLUCIONES S.L.
Under no circumstances shall it be understood that any license or renunciation, transfer, total or partial assignment of said rights is granted, nor is any right granted, and in particular, of exploitation, reproduction, distribution, transformation or public communication on said contents without the prior written authorization of INICIA SOLUCIONES DE VOZ SL

The use of the software will be limited to the specifications that the license of use grants.

Violations of any of the intellectual or industrial property rights referred to in this section will be prosecuted through the criminal and civil actions contemplated in current legislation.

If you need support, training or anything else please contact in comercial@iniciasoluciones.es


### Don't forget to talk about us in your social networks!!!!