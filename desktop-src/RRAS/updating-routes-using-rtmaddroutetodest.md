---
title: Mise à jour d’itinéraires à l’aide de RtmAddRouteToDest
description: Si le client n’a pas besoin d’efficacité lors de l’ajout d’un itinéraire, il doit utiliser la méthode de mise à jour des itinéraires suivante.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3212a74637fa4de51f3b05f80f84bace1c0c57ba570e5025adb796da933b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025329"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Mise à jour d’itinéraires à l’aide de RtmAddRouteToDest

Si le client n’a pas besoin d’efficacité lors de l’ajout d’un itinéraire, il doit utiliser la méthode de mise à jour des itinéraires suivante. Cette méthode est moins efficace car elle nécessite l’obtention d’un handle vers l’itinéraire et la transmission de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) vers et à partir du gestionnaire de tables de routage. Cette méthode prend également plus de temps. Étant donné que [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) ne manipule pas directement la table de routage, cette méthode vous aide à améliorer la simplicité.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




