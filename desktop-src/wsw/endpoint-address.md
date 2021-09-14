---
title: Adresse du point de terminaison
description: Une adresse de point de terminaison représente l’adresse d’un service sur le réseau.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Service Web adresse du point de terminaison pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230843"
---
# <a name="endpoint-address"></a>Adresse du point de terminaison

Une adresse de point de terminaison représente l’adresse d’un service sur le réseau. Lorsque vous ouvrez un [canal](channel.md), en appelant la fonction [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , vous devez fournir l’adresse du point de terminaison du service avec lequel vous communiquez, ainsi que la spécification du canal que vous souhaitez ouvrir.


Une adresse de point de terminaison se compose des éléments suivants :

-   une [URL](url.md)
-   un ensemble d’en-têtes (facultatif)
-   ensemble d’extensions (facultatif)
-   [identité](endpoint-identity.md) facultative représentant l’identité de sécurité du service.

Lorsqu’un message est adressé, l’URL devient l’en-tête « to » du message. Tous les en-têtes qui font partie de l’adresse du point de terminaison sont également ajoutés au message.

![Diagramme montrant les en-têtes d’adresse de point de terminaison ajoutés à un message.](images/endpointaddress.png)

Les canaux traitent automatiquement tous les messages envoyés à l’aide de la structure d' [**\_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) qui a été transmise à [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel). Vous pouvez également utiliser la fonction [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) pour remplacer ce comportement par défaut.

Lorsque [**l' \_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) est transmise en tant que paramètre, les fonctions [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) et [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) créent une copie du paramètre d' **\_ \_ adresse du point de terminaison WS** en mémoire et sa taille est limitée par 65536 octets. [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) n’a pas cette limitation, car il ne nécessite pas la création d’une copie du paramètre d' **\_ \_ adresse du point de terminaison WS** .

Les extensions spécifiées dans le champ **Extensions** de l' [**adresse de point de \_ terminaison \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) ne sont pas utilisées pour traiter le message, mais sont plutôt un mécanisme d’extensibilité qui peut être utilisé pour fournir des informations supplémentaires (par exemple, des métadonnées) sur le service. Les extensions communes peuvent être lues à l’aide de la fonction [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .

le champ d’identité facultatif de l’adresse du point de terminaison peut inclure, par exemple, le nom DNS de l’ordinateur sur lequel le service est en cours d’exécution, ou l’UPN du compte Windows sous lequel le service s’exécute. Le champ d’identité n’est pas utilisé pour traiter le message, mais peut être utilisé pour obtenir un jeton de sécurité pour le service (par exemple, pour obtenir un ticket Kerberos pour l’UPN cible) et pour vérifier l’identité des réponses du service (par exemple, une identité DNS utilisée pour les contrôles de nom sur le certificat de service renvoyé pendant le protocole SSL).

Les adresses de point de terminaison peuvent être lues et écrites à l’aide de la [sérialisation](serialization.md) avec la valeur d’énumération du type d’adresse du **point de \_ terminaison \_ \_ WS** du [**\_ type WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type). Remarque pour sérialiser une adresse de point de terminaison, vous devez connaître la version de la spécification utilisée pour les en-têtes d’adressage, comme spécifié dans l’énumération de la [**\_ \_ version de l’adressage WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

 

 




