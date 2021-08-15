---
title: Gestion des handles
description: Le gestionnaire de table de routage conserve un décompte de références pour toutes les informations qu’il gère.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c701dbe8469baab54c427d42f9d603a976402ebb5693d1799989aeff74b65945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790602"
---
# <a name="managing-handles"></a>Gestion des handles

Le gestionnaire de table de routage conserve un décompte de références pour toutes les informations qu’il gère. Cela empêche le gestionnaire de table de routage de retourner à un client tous les descripteurs de la mémoire qui a été libérée. Chaque fois qu’un handle est retourné à l’appelant, en tant que handle explicite ou en tant que partie d’une structure d’informations, comme les [**\_ \_ informations de dest RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info), le nombre de références pour l’objet qui correspond au descripteur est incrémenté. Lorsque le handle ou la structure d’informations est libéré, le décompte de références approprié est décrémenté. Lorsque le nombre de références est égal à zéro, l’objet est libéré.

Les fonctions [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) et [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) retournent des structures d’informations. Ces fonctions correspondent respectivement aux fonctions [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) et [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

> [!Note]  
> La fonction [**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) doit être utilisée pour libérer des handles qui ont été retournés par un appel à [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests). N’utilisez pas [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) pour les structures de destination modifiées.

 

Si un client doit conserver un handle spécifique dans une structure d’information tout en libérant le reste, le client peut appeler [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) avec ce handle avant de libérer la structure d’informations. Le descripteur peut ensuite être libéré par un appel aux fonctions [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) et [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

 

 




