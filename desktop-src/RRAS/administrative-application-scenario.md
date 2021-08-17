---
title: Scénario d’application administrative
description: Les applications administratives appellent un sous-ensemble de fonctions MGM liées à l’énumération des entrées de transfert de multidiffusion (MFEs) et des statistiques MFE.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c8574a0e6ab85fe4e826a224377fa0de5de3851b7e31264b4c68c3c2fce56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791914"
---
# <a name="administrative-application-scenario"></a>Scénario d’application administrative

Les applications administratives appellent un sous-ensemble de fonctions MGM liées à l’énumération des entrées de transfert de multidiffusion (MFEs) et des statistiques MFE. Une application n’a pas besoin de s’inscrire auprès du gestionnaire de groupe de multidiffusion pour utiliser ces fonctions (autrement dit, l’application n’a pas besoin d’un descripteur).

## <a name="enumerating-mfes"></a>Énumération de MFEs

Le tableau suivant résume une série d’étapes dans les interactions entre une application administrative et le gestionnaire de groupe de multidiffusion. La première colonne décrit les actions effectuées par l’application administrative et les réponses de l’application administrative au gestionnaire de groupe de multidiffusion. La deuxième colonne décrit les réponses du gestionnaire de groupe de multidiffusion à l’application administrative. La troisième colonne présente des informations supplémentaires.

Chaque ligne de la table représente une étape.



| Action de l’application administrative                                                                                                                                                                                      | Action du gestionnaire de groupe de multidiffusion                                                                                                                                                                                                                                                              | Remarques                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtenez un ou plusieurs MFEs à l’aide de la fonction [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) .                                                                                                                                   | Retourner autant de MFEs que possible dans la mémoire tampon fournie par le client. Si aucun MFEs ne peut être retourné dans la mémoire tampon fournie, la mémoire tampon de l’erreur de retour \_ est insuffisante \_ et la taille de la mémoire tampon nécessaire pour retourner un MFE.<br/>                                                              | Les clients peuvent également récupérer des statistiques MFE à l’aide des fonctions statistiques correspondantes, [**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) et [**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats). |
| Si \_ une erreur \_ de mémoire tampon insuffisante est reçue, appelez à nouveau la fonction [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) à l’aide d’une mémoire tampon de la taille indiquée.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Poursuivez l’appel de la fonction [**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) , en spécifiant comme l’un des paramètres le dernier MFE qui a été retourné par l’appel précédent à la fonction [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) . | Retourner autant de MFEs que possible dans la mémoire tampon fournie par le client. Si aucun MFEs ne peut être retourné dans la mémoire tampon fournie, la mémoire tampon de l’erreur de retour \_ est insuffisante \_ et la taille de la mémoire tampon nécessaire pour un MFE.<br/> Renvoyer l’erreur plus \_ aucun \_ \_ élément quand aucun MFEs n’est conservé.<br/> |                                                                                                                                                                                                 |
| Poursuivez l’énumération jusqu’à l’erreur \_ aucun \_ autre \_ élément n’est reçu.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Utilisez les fonctions [**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) et [**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) pour récupérer un ensemble spécifique de MFE ou un ensemble spécifique de statistiques MFE.

 

 

 





