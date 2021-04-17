---
title: Informations de référence sur l’API Services Bureau à distance AudioEndpoint
description: Prend en charge les interfaces pour l’inscription du point de terminaison audio et le transport des données.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, informations de référence sur l’API AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380192"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Informations de référence sur l’API Services Bureau à distance AudioEndpoint

Un *point de terminaison audio* représente un périphérique audio, une API audio, ou toute autre source ou récepteur audio, et permet d’envoyer des données à ou de consommer des données à partir du moteur audio. Un point de terminaison audio doit être connecté au moteur audio via une *connexion*, et chaque connexion ne peut être connectée qu’à un seul point de terminaison. Une fois qu’un point de terminaison est inscrit, le moteur audio joint le point de terminaison à la connexion.

Chaque objet de point de terminaison doit implémenter les interfaces suivantes :

-   [**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) pour permettre au moteur audio d’obtenir des informations sur le point de terminaison.
-   [**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) pour obtenir des informations sur la mémoire tampon de données avant d’effectuer un passage de traitement et de notifier le point de terminaison lorsque la passe est terminée.
-   L’interface [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) ou [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , selon que l’objet de point de terminaison capture ou restitue l’audio.
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

Le moteur audio utilise ces interfaces pour obtenir des informations sur les points de terminaison attachés au moteur. L’implémentation du point de terminaison doit fournir le mécanisme permettant de fournir des données à ou de consommer des données du moteur comme spécifié par ces interfaces.

L’API Services Bureau à distance AudioEndpoint prend en charge les types d’énumération, les interfaces et les structures.

## <a name="in-this-section"></a>Dans cette section

-   [Types d’énumération AudioEndpoint Services Bureau à distance](terminal-services-audioendpoint-enumeration-types.md)
-   [Services Bureau à distance les fonctions AudioEndpoint](remote-desktop-services-audioendpoint-functions.md)
-   [Services Bureau à distance les interfaces AudioEndpoint](terminal-services-audioendpoint-interfaces.md)
-   [Structures AudioEndpoint Services Bureau à distance](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Notes

L’API Services Bureau à distance AudioEndpoint est destinée à être utilisée dans Bureau à distance scénarios ; ce n’est pas le cas pour les applications clientes.

 

 




