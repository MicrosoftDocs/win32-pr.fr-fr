---
title: Énumération des groupes (RRAS)
description: Le tableau suivant résume une série d’étapes dans une interaction entre un protocole de routage et le gestionnaire de groupe de multidiffusion.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df3731e8370a213636ea12ad2a9b072903908888eba6983909c01201c655ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101839"
---
# <a name="enumerating-groups"></a>Énumération des groupes

Le tableau suivant résume une série d’étapes dans une interaction entre un protocole de routage et le gestionnaire de groupe de multidiffusion. La première colonne décrit les actions effectuées par le protocole de routage et les réponses du protocole de routage au gestionnaire de groupe de multidiffusion. La deuxième colonne décrit les réponses du gestionnaire de groupe de multidiffusion au protocole de routage. La troisième colonne présente des informations supplémentaires.

Chaque ligne de la table représente une étape.



| Action de protocole de routage                                                                                                                                                    | Action du gestionnaire de groupe de multidiffusion                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtenez un handle vers une énumération à l’aide de la fonction [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) .                                                         | Retourne un handle.                                                                                                                                                                                                                                                                                             |
| Obtenez un ou plusieurs groupes à l’aide de la fonction [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) .                                                             | Retourner autant de groupes que possible dans la mémoire tampon fournie par le client. Si aucun groupe ne peut être retourné dans la mémoire tampon fournie, la mémoire tampon de l’erreur \_ de retour est insuffisante \_ et la taille de la mémoire tampon nécessaire pour retourner un groupe.<br/> Renvoyer l’erreur plus \_ aucun \_ \_ élément lorsqu’il n’y a plus de groupes.<br/> |
| Si \_ une erreur \_ de mémoire tampon insuffisante est reçue, appelez à nouveau la fonction [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) à l’aide d’une mémoire tampon de la taille indiquée. |                                                                                                                                                                                                                                                                                                              |
| Continuez à appeler la fonction [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) jusqu’à ce qu’il \_ n’y \_ ait plus d' \_ éléments reçus.                                   |                                                                                                                                                                                                                                                                                                              |
| Terminez le processus d’énumération à l’aide de la fonction [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) .                                                                   | Détruisez le handle.                                                                                                                                                                                                                                                                                          |



 

 

 





