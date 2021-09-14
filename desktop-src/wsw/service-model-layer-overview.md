---
title: Vue d’ensemble de la couche de modèle de service
description: L’API du modèle de service WWSAPI modélise la communication entre un client et un service en tant qu’appels de méthode, plutôt qu’en tant que messages de données.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Vue d’ensemble de la couche de modèle de service services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295147"
---
# <a name="service-model-layer-overview"></a>Vue d’ensemble de la couche de modèle de service

L’API du modèle de service WWSAPI modélise la communication entre un client et un service en tant qu’appels de méthode, plutôt qu’en tant que messages de données. Contrairement à la [couche de canal](channel-layer-overview.md), qui prend en charge des échanges de [messages](message.md) plus traditionnels entre le client et le service, le modèle de service gère automatiquement la communication au moyen d’un proxy de service sur le client et d’un hôte de service sur le service. Cela signifie que le client appelle des fonctions générées et que le serveur implémente les rappels.


Par exemple, imaginez un service de calculatrice qui effectue l’addition et la soustraction sur deux nombres. L’addition et la soustraction sont des opérations naturellement représentées naturellement comme appels de méthode.

![Diagramme montrant comment un service de calculatrice communique avec un client à l’aide d’appels de méthode pour l’addition et la soustraction.](images/servicemodelintro.png)

Le modèle de service représente la communication entre le client et le service en tant qu’appels de méthode déclarés, et masque donc les détails de communication de la couche de canal sous-jacente de l’application, ce qui rend le service plus facile à implémenter.

## <a name="specifying-a-service"></a>Spécification d’un service

Un service doit être spécifié en termes de modèles d’échange de messages, ainsi que sa représentation de données réseau. Pour les services, cette spécification est généralement fournie sous forme de documents de schéma WSDL et XML.

Le document WSDL est un document XML qui contient la liaison de canal et les modèles d’échange de messages du service, tandis que le document de schéma XML est un document XML qui définit la représentation des messages individuels.

Pour le service de calculatrice et ses opérations d’addition et de soustraction, le document WSDL peut se présenter comme dans l’exemple suivant :

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

De même, son schéma XML peut être défini comme suit :

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a>Conversion de métadonnées en code

Le modèle de service fournit le [WsUtil.exe](web-service-compiler-tool.md) en tant qu’outil pour traiter ces documents de métadonnées, en convertissant un fichier WSDL en en-tête C et en fichiers sources.

![Diagramme montrant comment WsUtil.exe convertit un fichier WSDL en en-tête C et en fichiers sources.](images/doctotool.png)

Le [WsUtil.exe](web-service-compiler-tool.md) génère l’en-tête et les sources pour l’implémentation de service, ainsi que les opérations de service côté client pour le client.

## <a name="calling-the-calculator-service-from-a-client"></a>Appel du service de calculatrice à partir d’un client

Comme pour l’implémentation du service, le client doit inclure l’en-tête ou les en-têtes générés.

``` syntax
#include "CalculatorProxyStub.h"
```

À présent, l’application cliente peut créer et ouvrir un proxy de service pour commencer à communiquer avec le service de calculatrice.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

L’application peut appeler l’opération Add sur le service Calculator avec le code suivant :

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Reportez-vous à l’exemple de code sur [HttpCalculatorClientExample](httpcalculatorclientexample.md) pour une implémentation complète du service de calculatrice.

## <a name="service-model-components"></a>Composants du modèle de service

L’interaction des composants individuels du modèle de service WWSAPI dans l’exemple de calculatrice est la suivante :

-   Le client crée un [proxy de service](service-proxy.md) et l’ouvre.
-   Le client appelle la fonction Add du service et passe le proxy de service.
-   Le message est sérialisé selon les métadonnées de sérialisation dans l’en-tête et les fichiers sources générés par l’outil de métadonnées ([WsUtil.exe](web-service-compiler-tool.md)).
-   Le message est écrit sur le canal et transmis sur le réseau au service.
-   Côté serveur, le service est hébergé à l’intérieur d’un hôte de service et possède un point de terminaison qui écoute le contrat ICalculator.
-   À l’aide des métadonnées du modèle de service dans le stub, le service désérialise le message à partir du client et le distribue au stub.
-   Le service côté serveur appelle la méthode Add, en lui transmettant le contexte d’opération. Ce contexte d’opération contient la référence au message entrant.

![Diagramme montrant l’interaction des composants individuels du modèle de service WWSAPI.](images/servicemodellayout.png)

Composants

-   [Hôte de service](service-host.md): héberge un service.
-   [Proxy de service](service-proxy.md): définit la manière dont un client communique avec un service.
-   [Context](context.md): jeu de propriétés pour rendre les informations spécifiques à l’état disponibles pour une opération de service.
-   [Contrat](contract.md): définition d’interface d’un service. Par exemple, ICalculator représente un contrat pour le service Calculator dans notre exemple de code.
-   [WsUtil.exe](web-service-compiler-tool.md): l’outil de métadonnées de modèle de service pour générer des proxies et des stubs.

 

 




