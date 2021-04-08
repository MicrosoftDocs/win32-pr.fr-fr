---
title: Nouveautés des API UPnP
description: Les API de™ UPnP ont de nouvelles fonctionnalités et une documentation mise à jour pour Windows XP SP2. Le tableau suivant identifie la nouvelle documentation.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675766"
---
# <a name="whats-new-in-the-upnp-apis"></a>Nouveautés des API UPnP

Les API de™ UPnP ont de nouvelles fonctionnalités et une documentation mise à jour pour Windows XP SP2. Le tableau suivant identifie la nouvelle documentation.



| Fonctionnalité                                                          | Description                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Cette nouvelle interface permet à un appareil hébergé d’obtenir des informations sur un demandeur (autrement dit, un point de contrôle) et la demande. Il inclut trois méthodes, chacune d’elles fournissant un type d’informations différent.                                                                                                                                                              |
| [Implémentation du comportement de l’appareil](implementing-device-behavior.md) | Cette rubrique comprend une nouvelle section qui explique comment obtenir des informations de point de terminaison à l’aide de la nouvelle interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .                                                                                                                                                                                                     |
| [Paramètres de configuration](configuration-settings.md)             | Cette nouvelle rubrique fournit des informations sur les paramètres du Registre qui affectent le comportement des API UPnP.                                                                                                                                                                                                                                                                    |
| [Codes d’erreur de l’appareil](device-error-codes.md)                     | Cette nouvelle rubrique explique comment un code d’erreur d’un appareil est converti en valeur HRESULT et vice versa. Une bonne compréhension de ce processus est nécessaire pour évaluer une valeur HRESULT retournée par les méthodes [**IUPnPService :: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) et [**IUPnPService :: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) . |



 

 

 




