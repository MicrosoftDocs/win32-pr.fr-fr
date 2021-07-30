---
title: IUniversalOrchestrator, interface
description: Interface COM qui fournit des méthodes pour permettre à un client de communiquer avec l’Orchestrator universel.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: 5dbbaafb38ab9d790d32beca9b014f933d5d53d5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991846"
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