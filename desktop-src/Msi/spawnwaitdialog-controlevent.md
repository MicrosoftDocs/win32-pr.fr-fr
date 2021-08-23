---
description: Le ControlEvent, SpawnWaitDialog déclenche la boîte de dialogue spécifiée par la colonne argument de la table ControlEvent,, si l’expression dans la colonne condition prend la valeur FALSe.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffeddfcb46f67d292de81a5a8195ba17c2a63b305be229ae96b2133448d41f00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628009"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent,

Le ControlEvent, SpawnWaitDialog déclenche la boîte de dialogue spécifiée par la colonne argument de la [table ControlEvent,](controlevent-table.md), si l’expression dans la colonne condition prend la valeur false. La boîte de dialogue reste valable tant que l’expression conditionnelle conserve la valeur FALSe et est supprimée dès que la condition prend la valeur TRUE.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Boîte de dialogue de la [table de boîte de dialogue](dialog-table.md).

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Le ControlEvent, SpawnWaitDialog peut être utilisé pour attendre toute tâche d’arrière-plan dont l’achèvement peut être testé à l’aide d’une expression conditionnelle telle que l’état d’une propriété. Pour obtenir un exemple d’utilisation de SpawnWaitDialog ControlEvent,, consultez la section [création d’un conditionnel « Veuillez patienter... » MessageBox.](authoring-a-conditional-please-wait-------message-box.md)

 

 



