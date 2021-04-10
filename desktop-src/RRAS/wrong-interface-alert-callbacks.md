---
title: Rappels d’alerte d’interface incorrects
description: Une fois que le redirecteur de noyau a reçu des données de multidiffusion d’une source spécifique sur une interface incorrecte, il notifie le gestionnaire de groupe de multidiffusion.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675474"
---
# <a name="wrong-interface-alert-callbacks"></a>Rappels d’alerte d’interface incorrects

Une fois que le redirecteur de noyau a reçu des données de multidiffusion d’une source spécifique sur une interface incorrecte, il notifie le gestionnaire de groupe de multidiffusion. Le gestionnaire de groupe de multidiffusion appelle alors le [**PMGM \_ incorrect \_ si \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) le rappel de rappel au protocole de routage qui est propriétaire de l’interface sur laquelle les données arrivent incorrectement.

> [!Note]  
> Ce rappel n’est actuellement pas implémenté dans cette version de l’API MGM.

 

 

 




