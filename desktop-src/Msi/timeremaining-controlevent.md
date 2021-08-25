---
description: Le programme d’installation utilise l’événement TimeRemaining pour publier le temps approximatif restant, en secondes, pour la séquence de progression actuelle.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa29184c489e3d3a0b0f71d0dcd01297aa5359b25b3c463d3ccd3def6991257
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810709"
---
# <a name="timeremaining-controlevent"></a>TimeRemaining ControlEvent,

Le programme d’installation utilise l’événement TimeRemaining pour publier le temps approximatif restant, en secondes, pour la séquence de progression actuelle. Le temps restant peut être affiché sur une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) . Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un [contrôle de texte](text-control.md) sur une boîte de dialogue non modale s’abonne à cet événement via la [table EventMapping](eventmapping-table.md) et utilise l' [attribut TimeRemaining](timeremaining-control-attribute.md) pour afficher le temps restant.

Le même contrôle de texte qui s’abonne au ControlEvent, TimeRemaining peut également s’abonner au [ControlEvent, ScriptInProgress](scriptinprogress-controlevent.md). Dans ce cas, en tant que chaîne de message ScriptInProgress préliminaire, il est remplacé par la chaîne « temps restant : XX minutes ».

 

 



