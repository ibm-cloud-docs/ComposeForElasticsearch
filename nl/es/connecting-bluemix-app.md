---

copyright:
  years: 2016,2017
lastupdated: "2017-06-16"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Conexión de una aplicación {{site.data.keyword.cloud_notm}}

Para conectar una aplicación {{site.data.keyword.cloud}} al servicio, utilice las credenciales de servicio que se crean cuando se suministra el servicio. La app de ejemplo muestra cómo utilizar Node.js para conectar a un servicio de {{site.data.keyword.composeForElasticsearch}} utilizando las credenciales y cómo crear una base de datos y leer y escribir en la base de datos.

## Conexión mediante la app de ejemplo 'Hello World'

La app de ejemplo [compose-elasticsearch-helloworld-nodejs](https://github.com/IBM-Bluemix/compose-elasticsearch-helloworld-nodejs) muestra cómo utilizar Node.js para conectar a un servicio de {{site.data.keyword.composeForElasticsearch}} utilizando las credenciales proporcionada. La aplicación crea, lee y escribe en un índice de Elasticsearch.

Descargue la app de ejemplo y siga las instrucciones del archivo readme. A continuación, en la página de detalles de la aplicación de {{site.data.keyword.cloud}}, pulse **Ver APP** para ver el contenido del índice de *ejemplos*.

Nombre de campo|Descripción
----------|-----------
`uri`|El URI que se utilizará al conectarse al servicio. Incluye el esquema (`https:`), el nombre de usuario y la contraseña del administrador, el nombre de host del servidor y el número de puerto al que se conecta.
`uri_direct_1`|Un URI alternativo que se puede utilizar al conectarse al servicio. Formateado en cuanto a `uri`.
`uri_health`|Un mandato `curl` que solicita el estado del clúster desde el primer haproxy.
`uri_health_1`|Un mandato `curl` que solicita el estado del clúster desde el segundo haproxy.
`ca_certificate_base64`|Un certificado firmado automáticamente que se utiliza para confirmar que una aplicación se está conectando al servidor apropiado. Está codificado como base64. Debe decodificar la clave antes de utilizarla, como se muestra en la aplicación de ejemplo.
`deployment_id`|Un identificador interno para el servicio, tal como se ha creado en Compose.
`db_type`|El tipo de base de datos que ofrece el servicio; en este caso, `elastic_search`.
`name`|El nombre del despliegue de la base de datos.
{: caption="Tabla 1. Credenciales de Compose for Elasticsearch" caption-side="top"}

**Nota:** Dos portales `haproxy` proporcionan acceso al clúster Elasticsearch. Tanto `uri` como `uri_direct_1` pueden utilizarse para conectarse al clúster. En las aplicaciones, conmute entre `uri` y `uri_direct_1` para gestionar respuestas a fallos de conexión.