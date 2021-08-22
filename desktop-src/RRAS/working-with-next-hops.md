---
title: Utilisation des tronçons suivants
description: L’API RTMv2 permet aux clients de travailler avec la liste des tronçons suivants associés aux itinéraires et aux destinations.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f629bb5f43298c2cada3759ea3ab9c7bb71f0ca47a3c4158028d923646662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024709"
---
# <a name="working-with-next-hops"></a>Utilisation des tronçons suivants

L’API RTMv2 permet aux clients de travailler avec la liste des tronçons suivants associés aux itinéraires et aux destinations. Les clients peuvent ajouter ou mettre à jour un tronçon suivant en appelant [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Les clients peuvent supprimer un tronçon suivant à l’aide de [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop). Les clients peuvent rechercher les tronçons suivants en appelant [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).

Les clients peuvent également mettre à jour le tronçon suivant directement. Pour ce faire, le client doit d’abord verrouiller le tronçon suivant avec la fonction [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) . Le client peut ensuite utiliser le pointeur direct vers la structure d' [**\_ \_ informations du tronçon RTM RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) du gestionnaire de tables de routage pour effectuer les modifications nécessaires. Enfin, le client peut déverrouiller le tronçon suivant.

> [!Note]  
> L’adresse de saut suivant et les champs d’index d’interface dans le tronçon suivant identifient de façon unique le tronçon suivant et ne doivent pas être modifiés.

 

 

 




