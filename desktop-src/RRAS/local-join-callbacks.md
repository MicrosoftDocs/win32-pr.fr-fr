---
title: Rappels de jointure locale
description: Une fois que le gestionnaire de groupe de multidiffusion est averti par IGMP que de nouveaux récepteurs sont présents pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ rappel de rappel de jointure locale PMGM \_ \_ au protocole de routage qui possède l’interface, le cas échéant.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b3464aa645a6ab110acef09f238ffca97f781a38cc6c2602a39e7c66316490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074069"
---
# <a name="local-join-callbacks"></a>Rappels de jointure locale

Une fois que le gestionnaire de groupe de multidiffusion est averti par IGMP que de nouveaux récepteurs sont présents pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ \_ \_ rappel de jointure locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) au protocole de routage qui possède l’interface, le cas échéant. Ce rappel avertit le protocole de routage de la modification.

Ce rappel et le rappel de rappel de la [**\_ \_ sortie \_ locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) sont utilisés pour synchroniser le transfert entre les protocoles IGMP et de routage.

 

 




