---
title: IUniversalOrchestrator::WorkCompleted
description: Appelle Universal Orchestrator pour indiquer que le travail est terminé
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106542069"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a><span data-ttu-id="4219b-103">IUniversalOrchestrator :: WorkCompleted, méthode</span><span class="sxs-lookup"><span data-stu-id="4219b-103">IUniversalOrchestrator::WorkCompleted method</span></span>

> [!NOTE] 
> <span data-ttu-id="4219b-104">Cette API appartient à l’API Universal Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="4219b-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="4219b-105">Permet aux clients d’informer Universal Orchestrator que le travail précédemment planifié a été effectué et d’arrêter les rappels pour effectuer le travail jusqu’au prochain appel ScheduleWork réussi.</span><span class="sxs-lookup"><span data-stu-id="4219b-105">Allows clients to inform Universal Orchestrator that the previously scheduled work has been completed and stop callbacks to perform work until the next successful ScheduleWork call.</span></span>

## <a name="syntax"></a><span data-ttu-id="4219b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4219b-106">Syntax</span></span>

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a><span data-ttu-id="4219b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4219b-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="4219b-108">Chaîne unique qui identifie tous les appels de ce client spécifique.</span><span class="sxs-lookup"><span data-stu-id="4219b-108">A unique string that identifies all calls from this specific client.</span></span>

`workCompleted`

<span data-ttu-id="4219b-109">**True** si le travail s’est terminé avec succès.</span><span class="sxs-lookup"><span data-stu-id="4219b-109">**TRUE** if the work successfully completed.</span></span> <span data-ttu-id="4219b-110">Sinon, **false** si la tentative de travail a échoué et doit être retentée à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="4219b-110">Otherwise, **FALSE** if the work attempt failed and should be retried in the future.</span></span> 

## <a name="return-value"></a><span data-ttu-id="4219b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4219b-111">Return value</span></span>
<span data-ttu-id="4219b-112">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="4219b-112">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="4219b-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4219b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4219b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4219b-114">Requirements</span></span>

| <span data-ttu-id="4219b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4219b-115">Requirement</span></span> | <span data-ttu-id="4219b-116">Version</span><span class="sxs-lookup"><span data-stu-id="4219b-116">Version</span></span> |
|---|---|
| <span data-ttu-id="4219b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4219b-117">Minimum supported client</span></span> | <span data-ttu-id="4219b-118">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="4219b-118">Windows 10 1903</span></span> |
|   |   |



 

 



