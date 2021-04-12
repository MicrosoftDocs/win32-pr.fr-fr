---
title: Rappels de jointure locale
description: Une fois que le gestionnaire de groupe de multidiffusion est averti par IGMP que de nouveaux récepteurs sont présents pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ rappel de rappel de jointure locale PMGM \_ \_ au protocole de routage qui possède l’interface, le cas échéant.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462362"
---
# <a name="local-join-callbacks"></a>Rappels de jointure locale

Une fois que le gestionnaire de groupe de multidiffusion est averti par IGMP que de nouveaux récepteurs sont présents pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ \_ \_ rappel de jointure locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) au protocole de routage qui possède l’interface, le cas échéant. Ce rappel avertit le protocole de routage de la modification.

Ce rappel et le rappel de rappel de la [**\_ \_ sortie \_ locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) sont utilisés pour synchroniser le transfert entre les protocoles IGMP et de routage.

 

 




