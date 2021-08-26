---
title: Rappels d’alerte d’interface incorrects
description: Une fois que le redirecteur de noyau a reçu des données de multidiffusion d’une source spécifique sur une interface incorrecte, il notifie le gestionnaire de groupe de multidiffusion.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3354b1355cbcb1654b41a61ab046e74ec41b8dc716de6d50f7d9d52b18d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024649"
---
# <a name="wrong-interface-alert-callbacks"></a>Rappels d’alerte d’interface incorrects

Une fois que le redirecteur de noyau a reçu des données de multidiffusion d’une source spécifique sur une interface incorrecte, il notifie le gestionnaire de groupe de multidiffusion. Le gestionnaire de groupe de multidiffusion appelle alors le [**PMGM \_ incorrect \_ si \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) le rappel de rappel au protocole de routage qui est propriétaire de l’interface sur laquelle les données arrivent incorrectement.

> [!Note]  
> Ce rappel n’est actuellement pas implémenté dans cette version de l’API MGM.

 

 

 




