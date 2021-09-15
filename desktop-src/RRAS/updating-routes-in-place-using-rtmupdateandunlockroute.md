---
title: Mise à jour des itinéraires sur place à l’aide de RtmUpdateAndUnlockRoute
description: La mise à jour sur place est généralement plus efficace que la mise à jour de la table de routage avec une méthode indirecte telle que celle utilisée par la fonction RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311593"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Mise à jour des itinéraires sur place à l’aide de RtmUpdateAndUnlockRoute

La mise à jour sur place est généralement plus efficace que la mise à jour de la table de routage avec une méthode indirecte telle que celle utilisée par la fonction [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) . Cette méthode est plus efficace, car le client n’est pas obligé d’obtenir un descripteur, ni de passer la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) à et à partir du gestionnaire de tables de routage. Cette méthode prend également moins de temps. Toutefois, la mise à jour directe de la table de routage peut être risquée, étant donné que le gestionnaire de tables de routage ne fonctionne pas comme intermédiaire.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [mettre à jour un itinéraire sur place à l’aide de RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).

 

 




