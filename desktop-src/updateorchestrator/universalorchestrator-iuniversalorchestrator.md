---
title: IUniversalOrchestrator, interface
description: Interface COM qui fournit des méthodes pour permettre à un client de communiquer avec l’Orchestrator universel.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: f3635f76236eb6c7a11bfa62311003b7d76357a9fbacc9fde85f0bdffed0c129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966137"
---
# <a name="iuniversalorchestrator-interface"></a>IUniversalOrchestrator, interface

> [!NOTE] 
> Cette API appartient à l’API Universal Orchestrator.

**IUniversalOrchestrator** est une interface com qui fournit les méthodes suivantes pour permettre à un client de communiquer avec Universal Orchestrator.

## <a name="methods"></a>Méthodes

|Méthode | Description |
|---|---|
|[::ScheduleWork](universalorchestrator-schedulework.md) | Inscrit le travail en attente dans Universal Orchestrator. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informe Universal Orchestrator que tout le travail est terminé. |
|[::HasMoratoriumPassed](universalorchestrator-hasmoratoriumpassed.md) | Interroge Universal Orchestrator pour déterminer s’il fonctionne immédiatement après le nouvel appareil. |


## <a name="requirements"></a>Configuration requise

| Condition requise | Version |
|---|---|
| Client minimal pris en charge | Windows 10 1903 |
|   |   |