---
description: L’action WriteEnvironmentStrings modifie les valeurs des variables d’environnement.
ms.assetid: a91c1ffe-1bdd-49bb-aa6a-71667a1ed812
title: Action WriteEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a9d64a1140fc883d94e8d3733608d29dc2d39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011804"
---
# <a name="writeenvironmentstrings-action"></a>Action WriteEnvironmentStrings

L’action WriteEnvironmentStrings modifie les valeurs des variables d’environnement.

Les variables d’environnement ne changent pas pour l’installation en cours lorsque l’action WriteEnvironmentStrings ou l' [action RemoveEnvironmentStrings](removeenvironmentstrings-action.md) est exécutée. sur Windows 2000, Windows Server 2003, Windows XP et Windows Vista, ces informations sont stockées dans le registre et un message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) est envoyé pour informer le système des modifications une fois l’installation terminée. Un autre processus peut recevoir la notification des modifications en gérant ces messages. Aucun message n’est envoyé si le redémarrage du système est en attente. Un package peut utiliser la propriété [**MsiSystemRebootPending**](msisystemrebootpending.md) pour vérifier si un redémarrage du système est en attente.

Le programme d’installation exécute l’action WriteEnvironmentStrings uniquement lors de l’installation ou de la réinstallation d’un composant, et exécute l' [action RemoveEnvironmentStrings](removeenvironmentstrings-action.md) uniquement pendant la suppression d’un composant.

Les valeurs sont écrites ou supprimées en fonction de la sélection d’actions et de modificateurs principaux. Celles-ci sont décrites dans la section messages ActionData suivants. Notez que, selon l’action spécifiée, WriteEnvironmentStrings peut supprimer des variables et RemoveEnvironmentStrings peut les ajouter en fonction de la création de la [table d’environnement](environment-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L' [action InstallValidate](installvalidate-action.md) doit être exécutée avant l’action RemoveEnvironmentStrings. Étant donné que les actions WriteEnvironmentStrings et RemoveEnvironmentStrings ne sont jamais appliquées au cours de l’installation ou de la suppression d’un composant, leur séquence relative n’est pas restreinte.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                                                                                                                                                                                                  |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | Nom de la variable d’environnement à modifier.                                                                                                                                                                                 |
| \[2\] | Valeur de la variable d’environnement.                                                                                                                                                                                             |
| \[3\] | Il s’agit d’un champ de bits indicateurs qui spécifie l’action à exécuter. N’incluez qu’un seul bit pour une action principale. Il peut y avoir plusieurs bits de modificateur inclus dans ce champ. Consultez les descriptions des indicateurs de bits suivantes. |



 



| Valeur de bit | Description des actions principales                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1       | Prêts ? Définit la valeur de la variable d’environnement dans tous les cas.<br/> Si ce bit est combiné avec un bit de modificateur d’ajout ou de préfixe, l’action ajoute la valeur à toute valeur existante dans la variable.<br/> |
| 0x2       | Prêts ? Définit la valeur si la variable est absente.<br/> Si ce bit est combiné avec un bit de modificateur d’ajout ou de préfixe, l’action ajoute la valeur à toute valeur existante dans la variable.<br/>                |
| 0x4       | Supprimer. Supprime la valeur de la variable.<br/> Si ce bit est combiné avec un bit de modificateur d’ajout ou de préfixe, la valeur est supprimée de la chaîne existante, si la valeur existe.<br/>               |



 



| Valeur de bit  | Description du modificateur                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x20000000 | Si ce bit est défini, les actions sont appliquées aux variables d’environnement de l’ordinateur.<br/> Si ce bit n’est pas défini, des actions sont appliquées aux variables d’environnement de l’utilisateur.<br/> |
| 0x40000000 | Ajouter : Ce bit est facultatif. Ne définissez pas à la fois les modificateurs Append et prefix.<br/>                                                                                            |
| 0x80000000 | Céder. Ce bit est facultatif. Ne définissez pas à la fois les modificateurs Append et prefix.<br/>                                                                                            |



 

 

 
