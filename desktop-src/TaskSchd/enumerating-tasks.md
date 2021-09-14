---
title: Énumération des tâches
description: Planificateur de tâches 1,0 fournit un objet d’énumération pour l’énumération des tâches dans le dossier tâches planifiées.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- énumération des tâches Planificateur de tâches
- énumération des tâches Planificateur de tâches, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008664"
---
# <a name="enumerating-tasks"></a>Énumération des tâches

Planificateur de tâches 1,0 fournit un objet d’énumération pour l’énumération des tâches dans le [*dossier tâches planifiées*](s.md).

> [!Note]  
> pour un ordinateur Windows Server 2003, Windows XP ou Windows 2000 pour créer, surveiller ou contrôler des tâches sur un ordinateur Windows vista, certaines opérations doivent être effectuées sur l’ordinateur Windows vista. Pour plus d’informations, consultez l’article [Tâches MSBuild](tasks.md).

 

## <a name="using-the-enumeration-object"></a>Utilisation de l’objet d’énumération

L’interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) de cet objet fournit des méthodes pour énumérer les tâches dans le dossier, réinitialisation de la séquence d’énumération au début de la liste, ignorer des tâches et faire une copie de l’objet d’énumération actuel pour une utilisation ultérieure.

Pour plus d’informations sur l’énumération des tâches du dossier tâches planifiées, consultez [**IEnumWorkItems :: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).

Pour plus d’informations sur la réinitialisation de l’énumération au début de la liste, consultez [**IEnumWorkItems :: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).

Pour plus d’informations sur les tâches ignorées, consultez [**IEnumWorkItems :: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).

Pour plus d’informations sur la création d’une copie de l’objet d’énumération actuel, consultez [**IEnumWorkItems :: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).

Pour obtenir un exemple d’énumération des tâches dans le dossier tâches planifiées, consultez [exemple d’énumération de tâches](enumerating-tasks-example.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Informations sur la tâche Planificateur de tâches 1,0](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




