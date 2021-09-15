---
title: Windows Exemples de services Web
description: les exemples suivants montrent comment utiliser Windows API de Services Web.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525060"
---
# <a name="windows-web-services-examples"></a>Windows Exemples de services Web

les exemples suivants montrent comment utiliser Windows API de Services Web.

-   [Exemples de modèle de service](service-model-examples.md)
-   [Exemples de couche de canal TCP](tcp-channel-layer-examples.md)
-   [Exemples de couche de canal HTTP](http-channel-layer-examples.md)
-   [Exemples de couche de canal UDP](udp-channel-layer-examples.md)
-   [Exemples de couche de canal nommé](named-pipes-channel-layer-examples.md)
-   [Exemples de message](message-examples.md)
-   [Exemples XML](xml-examples.md)
-   [Exemples de modèles asynchrones](async-model-examples.md)
-   [Exemples de couche de canal de sécurité](security-channel-layer-examples.md)
-   [Exemples de réplication de fichiers](file-replication-examples.md)

## <a name="service-model-examples"></a>Exemples de modèle de service

Service Calculator : client : [HttpCalculatorClientExample](httpcalculatorclientexample.md), serveur : [HttpCalculatorServiceExample](httpcalculatorserviceexample.md).

Service Calculator avec sécurité de transport SSL : client : [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md), serveur : [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md).

Service Calculator avec nom d’utilisateur sur la sécurité SSL en mode mixte : client : [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md), serveur : [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).

Service Calculator avec Kerberos sur la sécurité SSL en mode mixte : client : [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md), serveur : [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md).

Service de bon de commande : client : [HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md), serveur : [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md).

Service de bon de commande avec sécurité de transport SSL : client : [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md), serveur : [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md).

Service de bon de commande avec nom d’utilisateur sur la sécurité SSL en mode mixte : client : [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md), serveur : [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md).

Service de bon de commande avec Kerberos sur la sécurité SSL en mode mixte : client : [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md), serveur : [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md).

Service de bon de commande non typé : serveur : [UnTypedServiceExample](untypedserviceexample.md). Client : [UnTypedClientExample](untypedclientexample.md)

Calculatrice de session : serveur : [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Client :[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md).

Calculatrice à l’aide d’une implémentation de canal et d’écouteur personnalisée : serveur :[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md). Client :[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md).

Calculatrice utilisant un canal encodé : serveur :[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md). Client :[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md).

Service qui gère les requêtes HTTP brutes (non-SOAP) : client :[HttpRawClientExample](httprawclientexample.md). Serveur :[HttpRawServiceExample](httprawserviceexample.md).

Notification d’abandon de l’opération de service : serveur : [BlockingServiceExample](blockingserviceexample.md). Client :[ServiceCancellationExample](servicecancellationexample.md).

Appel d’annulation : serveur : [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Client :[CallAbandonExample](callabandonexample.md).

Créez manuellement une description de la stratégie et utilisez-la pour créer un proxy de service : [PolicyTemplateExample](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Exemples de couche de canal TCP

Exemple TCP qui envoie des messages à l’aide d’un modèle unidirectionnel : client : [OneWayTcpClientExample](onewaytcpclientexample.md), serveur : [OneWayTcpServerExample](onewaytcpserverexample.md)

Exemple TCP qui envoie des messages à l’aide d’un modèle demande-réponse : client : [RequestReplyTcpClientExample](requestreplytcpclientexample.md), serveur : [RequestReplyTcpServerExample](requestreplytcpserverexample.md)

Exemple de streaming TCP : client : [StreamingTcpClientExample](streamingtcpclientexample.md), serveur : [StreamingTcpServerExample](streamingtcpserverexample.md)

Exemple de streaming TCP Async : client : [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md), serveur : [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Exemples de couche de canal HTTP

Exemple HTTP : client : [HttpClientExample](httpclientexample.md), serveur : [HttpServerExample](httpserverexample.md)

Exemple HTTP qui utilise les API de diffusion en continu : client : [StreamingHttpClientExample](streaminghttpclientexample.md), serveur : [StreamingHttpServerExample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Exemples de couche de canal UDP

Exemple UDP qui envoie des messages à l’aide d’un modèle unidirectionnel : client : [OneWayUdpClientExample](onewayudpclientexample.md), serveur : [OneWayUdpServerExample](onewayudpserverexample.md)

Exemple UDP qui envoie des messages à l’aide d’un modèle de réponse à une demande de multidiffusion : client : [MulticastUdpClientExample](multicastudpclientexample.md), serveur : [MulticastUdpServerExample](multicastudpserverexample.md) Voici le même exemple, mais à l’aide de l’adressage IPv6 : client : [MulticastUdpClientExample6](multicastudpclientexample6.md), serveur : [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Exemples de couche de canaux nommés

Exemple de canaux nommés qui envoie des messages à l’aide d’un modèle demande-réponse : client : [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md), serveur : [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)

Exemple de canaux nommés en continu : client : [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md), serveur : [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Exemples de message

Exemple qui utilise des en-têtes de message personnalisés : [CustomHeaderExample](customheaderexample.md)

Exemple qui encode et décode un message : [MessageEncodingExample](messageencodingexample.md)

Exemple de transfert d’un message : [ForwardMessageExample](forwardmessageexample.md)

## <a name="xml-examples"></a>Exemples XML

Exemple qui écrit et lit du code XML à l’aide d’une mémoire tampon XML [ReadWriteXmlExample](readwritexmlexample.md)

Exemple d’écriture et de lecture de données binaires à l’aide de MTOM, WsWriteBytes, WsPushBytes et WsPullBytes [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)

Exemple qui navigue dans une mémoire tampon XML [NavigateXmlExample](navigatexmlexample.md)

Exemple qui lit un nœud de document XML par nœud [ReadXmlExample](readxmlexample.md)

Exemple de recherche et d’affichage d’un attribut XML [ReadAttributeExample](readattributeexample.md)

Exemple d’écriture et de lecture d’un tableau d’éléments [ReadWriteArrayExample](readwritearrayexample.md)

Exemple qui insère un élément dans une mémoire tampon XML [InsertElementExample](insertelementexample.md)

Exemple qui illustre l’utilisation de certaines fonctions d’assistance de tampon XML [XmlBufferExample](xmlbufferexample.md)

Exemple qui écrit et lit le type dérivé à l’aide des fonctions d’assistance générées par Wsutil [DerivedTypeExample](derivedtypeexample.md)

## <a name="async-model-examples"></a>Exemples de modèles asynchrones

Exemple qui illustre le modèle pour les fonctions asynchrones. [AsyncModelExample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Exemples de couche de canal de sécurité

Windows la sécurité du transport via TCP : Client : [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), serveur : [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows la sécurité de transport sur des canaux nommés : Client : [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), serveur : [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Sécurité de transport SSL : client : [HttpClientWithSslExample](httpclientwithsslexample.md), serveur : [HttpServerWithSslExample](httpserverwithsslexample.md).

Nom d’utilisateur sur la sécurité SSL en mode mixte : client : [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), serveur : [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nom d’utilisateur sur la sécurité SSL en mode mixte : client : [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), serveur : [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Exemple de métadonnées

Les exemples suivants montrent comment traiter des documents WSDL et de stratégie dans le but d’extraire des informations sur le protocole pris en charge par un point de terminaison.

Nom d’utilisateur sur la sécurité SSL en mode mixte : [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Jeton émis sur la sécurité SSL en mode mixte : [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificat x509 sur la sécurité SSL en mode mixte : [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>exemple de Exchange WS-Metadata

Les exemples suivants montrent comment activer WS-MetadataExchange sur l' [ \_ \_ hôte WS service](ws-service-host.md).

Service TCP avec WS-MetadataExchange activé : [MetadataExchangeSample](metadataexchangesample.md). Client moniker de service WCF qui appelle le service TCP avec WS-MetadataExchange activé : [ServiceMonikerSample](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>En-têtes personnalisés et modèle de service

Les exemples suivants montrent comment utiliser les en-têtes personnalisés avec le [ \_ \_ proxy WS service](ws-service-proxy.md) et l' [ \_ \_ hôte WS service](ws-service-host.md) , respectivement.

Client : [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md), serveur : [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Exemple de réplication de fichiers

Exemple complet qui montre comment implémenter un service de réplication de fichiers : Tool : [FileRepToolExample](filereptoolexample.md), service : [FileRepServiceExample](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Interopérabilité du service public WCF

un client de services Web Windows communique avec un client de service WCF : [WcfPublicServiceSample](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Proxy HTTP personnalisé

un client de Services Web Windows communique avec un service ASMX TerraService à l’aide du client proxy personnalisé : [AsmxTerraServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)

 

 




