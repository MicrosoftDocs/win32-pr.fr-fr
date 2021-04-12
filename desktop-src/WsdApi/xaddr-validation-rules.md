---
description: Les adresses de transport (XAddrs) incluses dans les messages messages ProbeMatches et ResolveMatches sont soumises à la validation de base avant que WSDAPI envoie un message HTTP, tel qu’une demande de métadonnées.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Règles de validation XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202141"
---
# <a name="xaddr-validation-rules"></a>Règles de validation XAddr

Les adresses de transport (XAddrs) incluses dans les messages [messages ProbeMatches](probematches-message.md) et [ResolveMatches](resolvematches-message.md) sont soumises à la validation de base avant que wsdapi envoie un message http, tel qu’une demande de métadonnées.

Cela permet de s’assurer que les XAddrs se trouvent sur le même sous-réseau que le client.

Le code XML suivant montre un exemple d’élément XAddrs. Le préfixe WSD fait référence à l’espace de noms `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Toutes les conditions suivantes doivent être satisfaites pour que le message HTTP soit envoyé sur le réseau.

-   XAddrs doit être une adresse HTTP ou HTTPs. Les XAddrs d’autres schémas sont ignorés.
-   Si des XAddrs HTTPs sont présents, tous les XAddrs doivent être HTTPs. Les sections XAddr qui incluent des adresses HTTP et HTTPs sont entièrement ignorées. En outre, l’adresse de point de terminaison de l’appareil doit correspondre exactement à l’XAddrs HTTPs.
-   XAddrs doit être une adresse IP ou des noms d’hôte pouvant être résolus via DNS. En règle générale, les adresses IP sont utilisées.
-   Au moins une adresse IP incluse dans le XAddrs (ou l’adresse IP résolue à partir d’un nom d’hôte inclus dans le XAddrs) doit se trouver sur le même sous-réseau que la carte sur laquelle le message [messages ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) a été reçu.
-   L’adresse et le port spécifiés dans le premier XAddr doivent être accessibles. WSDAPI tente de se connecter à cette adresse lors de l’établissement d’une connexion HTTP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Messages ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Modèles de message d’échange de métadonnées et de découverte](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



