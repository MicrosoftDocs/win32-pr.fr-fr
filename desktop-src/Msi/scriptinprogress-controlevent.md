---
description: Le programme d’installation utilise cet événement pour afficher une chaîne d’information pendant la compilation du script d’exécution de l’installation.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119662"
---
# <a name="scriptinprogress-controlevent"></a>ScriptInProgress ControlEvent,

Le programme d’installation utilise cet événement pour afficher une chaîne d’information pendant la compilation du script d’exécution de l’installation. La chaîne d’information peut être affichée dans une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) . Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Un [contrôle de texte](text-control.md) s’abonnant à ScriptInProgress affiche la chaîne de texte spécifiée dans la [table UIText](uitext-table.md).

## <a name="typical-use"></a>Utilisation courante

Pendant la compilation du script d’exécution, le programme d’installation affiche un ProgressBar indiquant l’heure restante avant le début de l’exécution du script. L’auteur du package peut afficher un message préliminaire à ce stade, expliquant le ProgressBar. Pour afficher un message préliminaire, incluez un [contrôle de texte](text-control.md) dans la même boîte de dialogue non modale que le ProgressBar. Spécifiez que ce contrôle de texte s’abonne au ControlEvent, ScriptInProgress via la [table EventMapping](eventmapping-table.md). Incluez une entrée dans la [table UIText](uitext-table.md) avec ScriptInProgress spécifié dans le champ clé. Spécifiez le message préliminaire sous la forme d’une chaîne de texte dans le champ de texte de la table UIText. Ensuite, pendant la compilation du script, le programme d’installation affiche cette chaîne dans le contrôle de texte. Le texte affiché disparaît dès que la compilation du script est terminée.

Le même contrôle de texte qui s’abonne au ControlEvent, ScriptInProgress peut également s’abonner au [ControlEvent, TimeRemaining](timeremaining-controlevent.md). Dans ce cas, comme le texte de la chaîne ScriptInProgress préliminaire disparaît, il est remplacé par la chaîne « temps restant : XX minutes ».

 

 



