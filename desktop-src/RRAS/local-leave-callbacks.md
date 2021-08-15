---
title: Rappels locaux de sortie
description: Une fois que le gestionnaire de groupe de multidiffusion a été notifié par IGMP qu’aucun autre destinataire n’est présent pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ \_ rappel de rappel local Leave PMGM \_ dans le protocole de routage sur cette interface, le cas échéant. Ce rappel avertit le protocole de routage de la modification.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4cd346ac3d84a5c763c7f8f866e21a1bffa2af533e5710c86ec8826ad7db45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790639"
---
# <a name="local-leave-callbacks"></a>Rappels locaux de sortie

Une fois que le gestionnaire de groupe de multidiffusion a été notifié par IGMP qu’aucun autre destinataire n’est présent pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ \_ \_ rappel local Leave PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) dans le protocole de routage sur cette interface, le cas échéant. Ce rappel avertit le protocole de routage de la modification.

Ce rappel et le rappel de [**\_ \_ \_ rappel de jointure locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) sont utilisés pour synchroniser le transfert entre les protocoles IGMP et de routage.

 

 




