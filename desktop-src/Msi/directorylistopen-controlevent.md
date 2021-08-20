---
description: Cet événement sélectionne et met en surbrillance un répertoire dans le contrôle DirectoryList que l’utilisateur a choisi d’ouvrir. Pour obtenir des informations connexes, consultez boîte de dialogue Parcourir.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1453ffd42e0763ec747f02f7030818eaba3d533e5dfcca4570c13596efdcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947323"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent,

Cet événement sélectionne et met en surbrillance un répertoire dans le [contrôle DirectoryList](directorylist-control.md) que l’utilisateur a choisi d’ouvrir. Pour obtenir des informations connexes, consultez [boîte de dialogue Parcourir](browse-dialog.md).

Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement. L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Si aucun répertoire n’a été sélectionné dans le [contrôle DirectoryList](directorylist-control.md), un événement DirectoryListOpen désactive tous les autres contrôles qui publient un événement DirectoryListOpen.

## <a name="published-by"></a>Publié par

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue aucune action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) dans la même boîte de dialogue modale que le DirectoryList est utilisé pour déclencher le pas à pas détaillé dans le chemin d’accès.

 

 



