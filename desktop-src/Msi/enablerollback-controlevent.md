---
description: Ce ControlEvent, peut être utilisé pour activer ou désactiver les fonctionnalités de restauration du programme d’installation.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3b0cd93a65a9402c915606585f3eb1cd43c058847e2907b1134e1c84982b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143110"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent,

Ce ControlEvent, peut être utilisé pour activer ou désactiver les fonctionnalités de restauration du programme d’installation.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

False désactive les fonctionnalités de restauration du programme d’installation. True active les fonctionnalités de restauration du programme d’installation.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Peut être utilisé pour désactiver les fonctionnalités de restauration si le programme d’installation détecte que l’espace disque disponible est insuffisant pour terminer l’installation. Dans ce cas, ControlEvent, doit être utilisé avec les propriétés [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)et [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .

 

 



