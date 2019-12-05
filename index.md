Ouistiti - Small featured HTTP server
=====================================

# Ouistiti

Ouistiti _(ˈwistiti)_ is the french name of [Marmoset](https://en.wikipedia.org/wiki/Marmoset)
a little monkey of the New World.

Ouistiti is a small web server to manage and to configure small devices.
It allows to create an **unified Web interface** for **security** on
**Documents**, **Websocket**, **Rest API** and more.

Ouistiti is dedicated to be embedded on device for control from a web server.

With *Ouistiti*, all pages, websockets, scripts are protected by the same way.
It is useless to manage the authentication by your-self.
 
# Features

## Multi HTTP versions:
 
   * **HTTP/0.9** **HTTP/1.0** **HTTP/1.1** : *Ouistiti* is able to manage each version
    of the HTTP protocol from the requests or to accept only the requests of one version. 
   * **Keep Alive** connection: A client connection may be use for several requests.
   * **pipeline** requests: **Ouistiti** is able to receive request during the management
    of the previous one in the same connection.

## Secure HTTP - *HTTPS*:

   **TLS/SSL connection** is available as module with *mbedtls* or *openssl* library.

## Authentication: 

  The __authentication__ is available on *all client's connection*. The users'
  password may be encrypted for the storage. The following challenge
  are supported:

   * **Basic Authentication**: *Ouistiti* is able to check the users to the simplest way.
   * **Digest Authentication**: *Ouistiti* allows to create your connection page and check
    the rights.
   * **Bearer Authentication**: *Ouistiti* is able to create a token and all instances 
    of *Ouistiti* is able to check this token on the same network domain.
   * **OpenID Authentication**: Manage the users on a OpenID server (like Google) and
    *Ouistiti* checks the user's rights on it.
 
## Websocket:

   A module build a **Websocket bridge** between HTTP socket client and UNIX socket.
   It is able to manage the handshake and the transfer of data to your application.
   You develop a STREAM server on a UNIX socket, *Ouistiti* protects it on a HTTPS
   connection.

## HTTP streaming:

   Like the *Websocket*, *Ouistiti* is able to protect your __stream's server__. Your
   application should only send data on a STREAM socket, *Ouistiti* does the rest.

## Static documents:  

   Like any webserver, *Ouistiti* is able to send any kinds of files to your client.
   And in the same time it can manage them on your server:

   * **Rest API**: it allows to manage the document files with a **Rest API** to 
     upload, delete, rename the files directly on the server.
   * **Home directory**: each user can manage his own directory with his __private rights__.
   * **Range request**: file may be broken into many chunks for the download.

## CGI/1.1:

   **CGI scripts** may be call from the client.

## Connection filtering:

   The server may start with a __blacklist__ and a __whitelist__ of IP address.
 
## Mono threading or multi threading:

   *Ouistiti* may be build to manage client connections with only one process, to
   be the __fastest webserver__.  
   Or it may create a independants process for each client connection, to create
   a __sandbox__ around it.

