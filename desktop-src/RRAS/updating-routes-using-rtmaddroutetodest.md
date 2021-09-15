---
title: Mise à jour d’itinéraires à l’aide de RtmAddRouteToDest
description: Si le client n’a pas besoin d’efficacité lors de l’ajout d’un itinéraire, il doit utiliser la méthode de mise à jour des itinéraires suivante.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311590"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Mise à jour d’itinéraires à l’aide de RtmAddRouteToDest

Si le client n’a pas besoin d’efficacité lors de l’ajout d’un itinéraire, il doit utiliser la méthode de mise à jour des itinéraires suivante. Cette méthode est moins efficace car elle nécessite l’obtention d’un handle vers l’itinéraire et la transmission de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) vers et à partir du gestionnaire de tables de routage. Cette méthode prend également plus de temps. Étant donné que [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) ne manipule pas directement la table de routage, cette méthode vous aide à améliorer la simplicité.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




