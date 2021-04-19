---
description: Le ControlEvent, SpawnDialog indique au programme d’installation de créer un enfant d’une boîte de dialogue modale tout en conservant l’exécution de la boîte de dialogue actuelle.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512934"
---
# <a name="spawndialog-controlevent"></a>SpawnDialog ControlEvent,

Le ControlEvent, SpawnDialog indique au programme d’installation de créer un enfant d’une boîte de dialogue modale tout en conservant l’exécution de la boîte de dialogue actuelle.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne qui est le nom de la nouvelle boîte de dialogue.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour créer une boîte de dialogue enfant, telle que « voulez-vous vraiment annuler ? ». de l'application de partage.

 

 



