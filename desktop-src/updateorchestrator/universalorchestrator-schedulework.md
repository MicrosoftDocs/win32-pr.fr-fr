---
title: IUniversalOrchestrator::ScheduleWork
description: Appelle Universal Orchestrator pour planifier le travail
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106525764"
---
# <a name="iuniversalorchestratorschedulework-method"></a><span data-ttu-id="04f10-103">IUniversalOrchestrator :: ScheduleWork, méthode</span><span class="sxs-lookup"><span data-stu-id="04f10-103">IUniversalOrchestrator::ScheduleWork method</span></span>

> [!NOTE] 
> <span data-ttu-id="04f10-104">Cette API appartient à l’API Universal Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="04f10-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="04f10-105">Permet aux clients d’informer Universal Orchestrator que le travail est en attente et de fournir un fichier binaire qui sera appelé par Universal Orchestrator pour effectuer la mise à jour ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="04f10-105">Allows clients to inform Universal Orchestrator that work is pending and provide a binary that will be called by Universal Orchestrator to perform the update work at a later time.</span></span>

<span data-ttu-id="04f10-106">Le binaire de rappel doit être signé avec un certificat Microsoft valide, et l’appelant doit appeler l’appel ScheduleWork à partir du contexte système.</span><span class="sxs-lookup"><span data-stu-id="04f10-106">The callback binary must be signed with a valid Microsoft certificate, and the caller must be invoking the ScheduleWork call from SYSTEM context.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f10-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04f10-107">Syntax</span></span>

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a><span data-ttu-id="04f10-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04f10-108">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="04f10-109">Chaîne unique qui identifie tous les appels de ce client spécifique.</span><span class="sxs-lookup"><span data-stu-id="04f10-109">A unique string that identifies all calls from this specific client.</span></span>

`cmdLine`

<span data-ttu-id="04f10-110">Chemin d’accès complet au fichier binaire de rappel qui sera appelé par Universal Orchestrator pour effectuer le travail.</span><span class="sxs-lookup"><span data-stu-id="04f10-110">The full path to the callback binary that will be invoked by Universal Orchestrator to perform work.</span></span>

`startArg`

<span data-ttu-id="04f10-111">Paramètres à passer au binaire de rappel pour indiquer que Start est demandé.</span><span class="sxs-lookup"><span data-stu-id="04f10-111">Parameters to pass to the callback binary to indicate Start is requested.</span></span>

`pauseArg`

<span data-ttu-id="04f10-112">*(facultatif)* Paramètres à passer au binaire de rappel pour indiquer qu’une pause est demandée.</span><span class="sxs-lookup"><span data-stu-id="04f10-112">*(optional)* Parameters to pass to the callback binary to indicate Pause is requested.</span></span>

## <a name="return-value"></a><span data-ttu-id="04f10-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04f10-113">Return value</span></span>
<span data-ttu-id="04f10-114">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="04f10-114">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="04f10-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04f10-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f10-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04f10-116">Requirements</span></span>

| <span data-ttu-id="04f10-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04f10-117">Requirement</span></span> | <span data-ttu-id="04f10-118">Version</span><span class="sxs-lookup"><span data-stu-id="04f10-118">Version</span></span> |
|---|---|
| <span data-ttu-id="04f10-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04f10-119">Minimum supported client</span></span> | <span data-ttu-id="04f10-120">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="04f10-120">Windows 10 1903</span></span> |
|   |   |



 

 



