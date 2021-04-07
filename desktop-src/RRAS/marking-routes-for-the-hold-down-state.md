---
title: Marquage des itinéraires pour l’État Hold-Down
description: Certains clients, tels que les protocoles de vecteur de distance tels que RIP et DVMRP, requièrent que les destinations soient publiées comme inaccessibles pendant un certain temps après la suppression du dernier itinéraire vers la destination.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940057"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Marquage des itinéraires pour l’État Hold-Down

Certains clients, tels que les protocoles de vecteur de distance tels que RIP et DVMRP, requièrent que les destinations soient publiées comme inaccessibles pendant un certain temps après la suppression du dernier itinéraire vers la destination. Le dernier itinéraire qui est supprimé doit être publié comme étant inaccessible, même si des itinéraires plus récents arrivent en attendant. Le dernier itinéraire supprimé est marqué comme étant dans un *État de blocage*. Le processus de blocage empêche la formation de boucles de routage. Les boucles de routage sont générées lorsqu’un protocole de routage publie des informations de routage obsolètes. Lorsque le délai d’attente expire, ces protocoles reprennent leur publication avec le nouvel itinéraire le plus approprié.

Un protocole qui implémente des États de blocage indique qu’une destination est dans un état de blocage à l’aide de la fonction [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) . Le client appelle cette fonction lorsqu’il publie le meilleur itinéraire vers cette destination. Si tous les itinéraires vers cette destination sont supprimés par la suite, le dernier itinéraire supprimé est conservé dans un état de blocage pendant la période spécifiée dans l’appel précédent à **RtmHoldDestination**.

Lorsqu’un protocole publie une destination, les informations d’itinéraire qui sont utilisées varient selon que le protocole utilise des États de blocage et si un itinéraire dans l’état de blocage existe pour la destination.

Les protocoles qui n’utilisent pas d’États de blocage peuvent ignorer les informations de routage relatives aux États de maintien d’une destination et publier toujours le meilleur itinéraire.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [utiliser l’état de Hold-Down d’itinéraire](use-the-route-hold-down-state.md).

 

 




