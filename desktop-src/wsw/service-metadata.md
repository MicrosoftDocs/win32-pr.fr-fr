---
title: Métadonnées du service
description: L’hôte de service WWSAPI prend en charge WS-MetadataExchange pour ses points de terminaison.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Métadonnées de service natives-services Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295150"
---
# <a name="service-metadata"></a>Métadonnées du service

L’hôte de service WWSAPI prend en charge WS-MetadataExchange pour ses points de terminaison. Vous activez ce type d’échange de métadonnées sur l’hôte de service en procédant comme suit :

-   Spécifiez les documents de métadonnées dans la propriété de [**\_ \_ métadonnées WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) sur l' [ \_ \_ hôte WS service](ws-service-host.md).
-   Spécifiez le nom du service dans la propriété de [**\_ \_ métadonnées WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) sur l' [ \_ \_ hôte du service WS](ws-service-host.md).
-   Spécifiez le port pour les points de terminaison individuels à l’aide de la propriété de [**\_ \_ \_ \_ métadonnées de propriété de point**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) de terminaison de service WS sur le point de [**\_ \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).
-   Activez une ou plusieurs structures de [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) pour traiter les demandes de WS-MetadataExchange.
-   Si vous le souhaitez, spécifiez le **\_ \_ \_ \_ \_ \_ \_ suffixe de l’URL d’échange de métadonnées du point de terminaison WS service** dans l’énumération de l' [**\_ \_ \_ \_ ID de propriété du point de terminaison de service Web**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) pour traiter Ws-MetadataExchange demandes sur une adresse spécifique.


Spécification de documents de métadonnées/nom de service sur l’hôte de service

La première étape consiste à spécifier les documents de métadonnées sur l’hôte de service. Pour ce faire, rassemblez les documents individuels sous la forme d’un tableau de la \_ chaîne WS XML \_ \* . Ces chaînes peuvent être des documents de schéma XML, WSDL ou WS-Policy. Cela est spécifié par le biais de la propriété de [**\_ \_ \_ métadonnées de propriété de service Web**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .

Éventuellement, une application peut également spécifier le nom du service et l’espace de noms dans le cadre des [**\_ \_ métadonnées du service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata). Si le document de métadonnées ne spécifie pas l’élément de service pour le nom de service donné, le modèle de service génère un élément de service avec les ports WSDL correspondants pour le service.

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

Notez qu’aucune vérification des documents de métadonnées individuels n’est effectuée sur les documents. Il incombe à l’application de valider le contenu des documents et de s’assurer que tous les chemins d’importation sont spécifiés de façon relative.

L’espace de noms spécifié est utilisé pour localiser le document dans lequel l’élément de service sera ajouté par l’hôte de service.

Ajout d’un élément de service au document WSDL

L’hôte de service fournit à l’application la possibilité d’ajouter un élément de service en son nom, si aucune n’est déjà spécifiée. Pour activer ce comportement, une application doit spécifier des champs serivceName et serviceNs sur la structure de [**\_ \_ métadonnées WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) . Si serviceName et serviceNs sont tous deux **null** , aucun élément de service n’est ajouté au document WSDL. Ils sont tous deux utilisés pour identifier le document dans lequel le serviceElement va être ajouté.

Si la propriété de [**\_ \_ \_ métadonnées de propriété WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) n’est pas spécifiée, aucune métadonnée n’a lieu sur l’hôte de service.

Spécification du port sur le point de terminaison du \_ service WS \_

Pour qu' [**un \_ point de \_ terminaison de service Web**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) soit disponible en tant que port à l’intérieur de l’élément de service dans le document WSDL, l’application doit spécifier la propriété de [**\_ \_ \_ \_ métadonnées de la propriété de point de terminaison de service WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

Il est supposé que la référence au nom de liaison et à l’espace de noms existe dans les documents spécifiés sur l’hôte de service dans le cadre des \_ \_ métadonnées de propriété WS service \_ . Le runtime ne vérifie pas cela au nom de l’application.

Activer la maintenance de WS-MetadataExchange sur le point de terminaison de \_ service WS \_

Pour pouvoir traiter les demandes de WS-MetadataExchange, l’hôte de service doit avoir au moins un point de terminaison activé pour la maintenance des demandes de WS-MetadataExchange. Pour ce faire, définissez la version appropriée pour WS-MetadataExchange sur le [**\_ point de \_ terminaison du service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Activer la maintenance HTTP sur le point de terminaison de \_ service WS \_

Pour serviceHTTP les demandes d’accès, l’hôte de service doit avoir au moins un point de terminaison activé pour la maintenance des demandes de WS-MetadataExchange. Pour ce faire, définissez la version appropriée pour WS-MetadataExchange sur le [**\_ point de \_ terminaison du service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Spécification du suffixe d’URL pour les demandes Ws-MetadataExchange

Une application peut éventuellement activer l’acceptation des demandes uniquement pour WS-MetadataExchange sur un chemin d’accès spécifique. Pour ce faire, vous spécifiez un suffixe pour le point de terminaison du service WS donné \_ \_ . Ce suffixe est concaténé tel quel à l’URL réelle du point de \_ terminaison du service WS \_ . La chaîne concaténée est utilisée comme URL correspondante à l’en-tête « to » reçu.

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

Les éléments d’API suivants sont liés au service métadonnées.

| Énumération                                                       | Description                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_type d’échange de métadonnées WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | Active ou désactive la maintenance de WS-MetadataExchange et HTTP sur le point de terminaison. |



 



| Structure                                                               | Description                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_ \_ métadonnées du point de terminaison de service WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | Représente l’élément de port pour le point de terminaison.                         |
| [**\_ \_ métadonnées WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | Spécifie le tableau de documents de métadonnées du service.                       |
| [**\_document de \_ métadonnées WS service \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | Spécifie les documents individuels qui composent les métadonnées du service. |



 

 

 




