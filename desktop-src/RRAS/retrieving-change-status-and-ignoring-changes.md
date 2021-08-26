---
title: Récupération de l’état des modifications et ignorer les modifications
description: Le client peut interroger le gestionnaire de table de routage pour déterminer si une notification de modification apportée à une destination est en attente en appelant RtmGetChangeStatus. Cette fonction retourne la valeur TRUE jusqu’à ce que l’appelant récupère cette modification en appelant RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a117130ac939788a74aaa32092000e8f6f29aa6b34e697ca6066c9e13259b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028059"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Récupération de l’état des modifications et ignorer les modifications

Le client peut interroger le gestionnaire de table de routage pour déterminer si une notification de modification apportée à une destination est en attente en appelant [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus). Cette fonction retourne la **valeur true** jusqu’à ce que l’appelant récupère cette modification en appelant [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).

Un client peut utiliser cette requête pour éviter d’effectuer une action qui devrait être annulée après la réception et le traitement de la notification de modification. L’utilisation de cette fonctionnalité permet au client de travailler efficacement en reportant certaines opérations à un moment ultérieur.

Le client peut également ignorer une notification de modification en attente pour une destination en appelant [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests). Un appel ultérieur à [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) ne retourne pas cette destination, sauf si une autre modification survient après l’appel à [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).

 

 




