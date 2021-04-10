---
title: Rappels locaux de sortie
description: Une fois que le gestionnaire de groupe de multidiffusion a été notifié par IGMP qu’aucun autre destinataire n’est présent pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ \_ rappel de rappel local Leave PMGM \_ dans le protocole de routage sur cette interface, le cas échéant. Ce rappel avertit le protocole de routage de la modification.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98d32e041b048e15497bc7fe35d17628b9331d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029424"
---
# <a name="local-leave-callbacks"></a>Rappels locaux de sortie

Une fois que le gestionnaire de groupe de multidiffusion a été notifié par IGMP qu’aucun autre destinataire n’est présent pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ \_ \_ rappel local Leave PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) dans le protocole de routage sur cette interface, le cas échéant. Ce rappel avertit le protocole de routage de la modification.

Ce rappel et le rappel de [**\_ \_ \_ rappel de jointure locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) sont utilisés pour synchroniser le transfert entre les protocoles IGMP et de routage.

 

 




