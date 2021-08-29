---
title: Arrêt d’un protocole de routage de multidiffusion
description: Le tableau suivant résume une série d’étapes dans une interaction d’arrêt entre le gestionnaire de groupe de multidiffusion et le protocole de routage lorsque le protocole de routage s’arrête.
ms.assetid: d868218d-7939-45d1-9e2f-3415c40f1a62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b1097b21c75788cd802b7316efe023bfb9b61bec3414fd5b35a344e97114c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080909"
---
# <a name="shutting-down-a-multicast-routing-protocol"></a>Arrêt d’un protocole de routage de multidiffusion

Le tableau suivant résume une série d’étapes dans une interaction d’arrêt entre le gestionnaire de groupe de multidiffusion et le protocole de routage lorsque le protocole de routage s’arrête. La première colonne décrit les actions effectuées par le protocole de routage et les réponses du protocole de routage au gestionnaire de groupe de multidiffusion. La deuxième colonne décrit les réponses du gestionnaire de groupe de multidiffusion au protocole de routage et toutes les actions effectuées par le gestionnaire de groupe de multidiffusion, telles que les rappels. La troisième colonne présente des informations supplémentaires.

Chaque ligne de la table représente une étape.



| Action de protocole de routage                                                                                                                                     | Action du gestionnaire de groupe de multidiffusion                                                                                                                                                                                                                                                                                                                                                                                                                                            | Notes                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Libération de la propriété de chaque interface dont le protocole de routage est propriétaire à l’aide de la fonction [**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership) . | Si IGMP s’exécute également sur l’interface qui vient d’être publiée par un protocole de routage, contactez IGMP en utilisant le rappel de [**\_ \_ \_ rappel IGMP PMGM Disable**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . Une fois que toutes les modifications apportées aux données de multidiffusion concernant la propriété de l’interface ont été effectuées, contactez à nouveau IGMP en utilisant PMGM activer le rappel de [**\_ \_ \_ rappel IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .<br/> Supprimez toutes les entrées de transfert associées à cette interface.<br/> |                                                                           |
| Annulez l’inscription auprès du gestionnaire de groupe de multidiffusion à l’aide de la fonction [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                    | Détruisez le descripteur retourné au protocole de routage par un appel précédent à la fonction [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                                                                                                                                                                                                                                                                                                 | Le protocole de routage ne peut plus utiliser ce handle pour appeler les fonctions MGM. |



 

 

