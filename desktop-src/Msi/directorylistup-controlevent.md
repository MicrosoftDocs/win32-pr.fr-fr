---
description: Cet événement avertit le contrôle DirectoryList que l’utilisateur souhaite sélectionner le parent du répertoire actuel. Pour obtenir des informations connexes, consultez boîte de dialogue Parcourir.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953253"
---
# <a name="directorylistup-controlevent"></a>DirectoryListUp ControlEvent,

Cet événement avertit le [contrôle DirectoryList](directorylist-control.md) que l’utilisateur souhaite sélectionner le parent du répertoire actuel. Pour obtenir des informations connexes, consultez [boîte de dialogue Parcourir](browse-dialog.md).

Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement. L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Si le répertoire actif est le répertoire racine du lecteur, un événement DirectoryListUp désactive tous les autres contrôles qui publient un événement DirectoryListUp.

## <a name="published-by"></a>Publié par

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur la même boîte de dialogue modale que le DirectoryList est utilisé pour déclencher un pas à pas détaillé dans le chemin d’accès.

 

 



