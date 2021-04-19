---
title: IUniversalOrchestrator, interface
description: Interface COM qui fournit des méthodes pour permettre à un client de communiquer avec l’Orchestrator universel.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106535083"
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