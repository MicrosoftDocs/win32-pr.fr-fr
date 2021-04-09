---
description: Le programme d’installation utilise cet événement pour publier le nom de l’action présente. Le nom peut être affiché sur une boîte de dialogue par un contrôle de texte qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951799"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent,

Le programme d’installation utilise cet événement pour publier le nom de l’action présente. Le nom peut être affiché sur une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) . Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Les abonnés sont affichés lorsqu’une nouvelle donnée de progression arrive à partir du programme d’installation.

## <a name="typical-use"></a>Utilisation courante

Un [contrôle de texte](text-control.md) sur une boîte de dialogue non modale s’abonne à cet événement via la [table EventMapping](eventmapping-table.md). L' [attribut de contrôle de texte](text-control-attribute.md) doit figurer dans le champ attributs de ce tableau pour recevoir le nom de l’action actuelle.

 

 



