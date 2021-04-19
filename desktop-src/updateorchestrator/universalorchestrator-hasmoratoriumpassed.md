---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Interroge Universal Orchestrator pour déterminer si la période postérieure à OOBE a été dépassée.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106527717"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a><span data-ttu-id="57224-103">IUniversalOrchestrator :: HasMoratoriumPassed, méthode</span><span class="sxs-lookup"><span data-stu-id="57224-103">IUniversalOrchestrator::HasMoratoriumPassed method</span></span>

> [!NOTE] 
> <span data-ttu-id="57224-104">Cette API appartient à l’API Universal Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="57224-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="57224-105">Permet aux clients de déterminer si Universal Orchestrator fonctionne immédiatement après le nouvel appareil, ce qui limite les tentatives de travail visant à minimiser l’interruption de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57224-105">Allows clients to determine if Universal Orchestrator is operating immediately after the new device Out of Box Experience, which limits work attempts to minimize user interruption.</span></span> 

## <a name="syntax"></a><span data-ttu-id="57224-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57224-106">Syntax</span></span>

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a><span data-ttu-id="57224-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57224-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="57224-108">Chaîne unique qui identifie tous les appels de ce client spécifique.</span><span class="sxs-lookup"><span data-stu-id="57224-108">A unique string that identifies all calls from this specific client.</span></span>

`hasMoratoriumPassed`

<span data-ttu-id="57224-109">Paramètre de sortie qui stocke le résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="57224-109">Output parameter that stores the result of the query.</span></span>

## <a name="return-value"></a><span data-ttu-id="57224-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57224-110">Return value</span></span>
<span data-ttu-id="57224-111">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="57224-111">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="57224-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57224-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="57224-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57224-113">Requirements</span></span>

| <span data-ttu-id="57224-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57224-114">Requirement</span></span> | <span data-ttu-id="57224-115">Version</span><span class="sxs-lookup"><span data-stu-id="57224-115">Version</span></span> |
|---|---|
| <span data-ttu-id="57224-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57224-116">Minimum supported client</span></span> | <span data-ttu-id="57224-117">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="57224-117">Windows 10 1903</span></span> |
|   |   |



 

 



