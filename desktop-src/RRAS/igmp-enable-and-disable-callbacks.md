---
title: Activer et désactiver les rappels IGMP
description: Le gestionnaire de groupe de multidiffusion utilise deux rappels à IGMP pour coordonner les modifications de la propriété de l’interface de IGMP à un protocole de routage et d’un protocole de routage à IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103a0f9abb4d2a78b2b87fde3cb5832b4e88eb2677851d9fe703e5162263642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791142"
---
# <a name="igmp-enable-and-disable-callbacks"></a>Activer et désactiver les rappels IGMP

Le gestionnaire de groupe de multidiffusion utilise deux rappels à IGMP pour coordonner les modifications de la propriété de l’interface de IGMP à un protocole de routage et d’un protocole de routage à IGMP. Les rappels permettent à IGMP de coexister sur une interface avec un autre protocole de routage, tel que DVMRP.

Une fois que la propriété d’une interface a changé, le gestionnaire de groupe de multidiffusion appelle d’abord le rappel de [**\_ \_ \_ rappel IGMP PMGM Disable**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . IGMP doit cesser d’ajouter et de supprimer des appartenances aux groupes sur l’interface spécifiée jusqu’à ce que le gestionnaire de groupe de multidiffusion appelle PMGM activer le rappel de [**\_ \_ \_ rappel IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .

Le gestionnaire de groupe de multidiffusion appelle l’PMGM activer le rappel de [**\_ \_ \_ rappel IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) lorsque la modification de la propriété de l’interface est terminée.

 

 