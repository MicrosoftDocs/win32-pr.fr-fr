---
title: Utilisation des tronçons suivants
description: L’API RTMv2 permet aux clients de travailler avec la liste des tronçons suivants associés aux itinéraires et aux destinations.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380312"
---
# <a name="working-with-next-hops"></a>Utilisation des tronçons suivants

L’API RTMv2 permet aux clients de travailler avec la liste des tronçons suivants associés aux itinéraires et aux destinations. Les clients peuvent ajouter ou mettre à jour un tronçon suivant en appelant [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Les clients peuvent supprimer un tronçon suivant à l’aide de [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop). Les clients peuvent rechercher les tronçons suivants en appelant [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).

Les clients peuvent également mettre à jour le tronçon suivant directement. Pour ce faire, le client doit d’abord verrouiller le tronçon suivant avec la fonction [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) . Le client peut ensuite utiliser le pointeur direct vers la structure d' [**\_ \_ informations du tronçon RTM RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) du gestionnaire de tables de routage pour effectuer les modifications nécessaires. Enfin, le client peut déverrouiller le tronçon suivant.

> [!Note]  
> L’adresse de saut suivant et les champs d’index d’interface dans le tronçon suivant identifient de façon unique le tronçon suivant et ne doivent pas être modifiés.

 

 

 




