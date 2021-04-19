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
# <a name="iuniversalorchestrator-interface"></a><span data-ttu-id="86792-103">IUniversalOrchestrator, interface</span><span class="sxs-lookup"><span data-stu-id="86792-103">IUniversalOrchestrator interface</span></span>

> [!NOTE] 
> <span data-ttu-id="86792-104">Cette API appartient à l’API Universal Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="86792-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="86792-105">**IUniversalOrchestrator** est une interface com qui fournit les méthodes suivantes pour permettre à un client de communiquer avec Universal Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="86792-105">**IUniversalOrchestrator** is a COM interface that provides the following methods to allow a client to communicate with the Universal Orchestrator.</span></span>

## <a name="methods"></a><span data-ttu-id="86792-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="86792-106">Methods</span></span>

|<span data-ttu-id="86792-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="86792-107">Method</span></span> | <span data-ttu-id="86792-108">Description</span><span class="sxs-lookup"><span data-stu-id="86792-108">Description</span></span> |
|---|---|
|[<span data-ttu-id="86792-109">::ScheduleWork</span><span class="sxs-lookup"><span data-stu-id="86792-109">::ScheduleWork</span></span>](universalorchestrator-schedulework.md) | <span data-ttu-id="86792-110">Inscrit le travail en attente dans Universal Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="86792-110">Registers pending work with the Universal Orchestrator.</span></span> |
|[<span data-ttu-id="86792-111">::WorkCompleted</span><span class="sxs-lookup"><span data-stu-id="86792-111">::WorkCompleted</span></span>](universalorchestrator-workcompleted.md) | <span data-ttu-id="86792-112">Informe Universal Orchestrator que tout le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="86792-112">Informs the Universal Orchestrator that all work is complete.</span></span> |
|[<span data-ttu-id="86792-113">::HasMoratoriumPassed</span><span class="sxs-lookup"><span data-stu-id="86792-113">::HasMoratoriumPassed</span></span>](universalorchestrator-hasmoratoriumpassed.md) | <span data-ttu-id="86792-114">Interroge Universal Orchestrator pour déterminer s’il fonctionne immédiatement après le nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="86792-114">Queries Universal Orchestrator to determine if it is operating immediately after the new device Out of Box Experience.</span></span> |


## <a name="requirements"></a><span data-ttu-id="86792-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86792-115">Requirements</span></span>

| <span data-ttu-id="86792-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86792-116">Requirement</span></span> | <span data-ttu-id="86792-117">Version</span><span class="sxs-lookup"><span data-stu-id="86792-117">Version</span></span> |
|---|---|
| <span data-ttu-id="86792-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86792-118">Minimum supported client</span></span> | <span data-ttu-id="86792-119">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="86792-119">Windows 10 1903</span></span> |
|   |   |