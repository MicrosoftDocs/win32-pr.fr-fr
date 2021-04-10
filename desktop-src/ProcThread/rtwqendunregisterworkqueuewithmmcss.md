---
description: Termine une demande asynchrone pour annuler l’inscription d’une file d’attente de travail à l’aide d’une tâche du service Planificateur de classes multimédias (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865737"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a><span data-ttu-id="aabde-103">RtwqEndUnregisterWorkQueueWithMMCSS fonction)</span><span class="sxs-lookup"><span data-stu-id="aabde-103">RtwqEndUnregisterWorkQueueWithMMCSS function</span></span>

<span data-ttu-id="aabde-104">Termine une demande asynchrone pour annuler l’inscription d’une file d’attente de travail à l’aide d’une tâche du service Planificateur de classes multimédias (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="aabde-104">Completes an asynchronous request to unregister a work queue with a Multimedia Class Scheduler Service (MMCSS) task.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabde-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aabde-105">Syntax</span></span>


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a><span data-ttu-id="aabde-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aabde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aabde-107">*pResult*</span><span class="sxs-lookup"><span data-stu-id="aabde-107">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="aabde-108">Pointeur vers l’interface [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="aabde-108">Pointer to the [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="aabde-109">Transmettez le même pointeur que celui reçu dans la méthode [**IRtwqAsyncCallback :: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="aabde-109">Pass in the same pointer that your callback object received in the [**IRtwqAsyncCallback::Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aabde-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aabde-110">Return value</span></span>

<span data-ttu-id="aabde-111">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aabde-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aabde-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aabde-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aabde-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aabde-113">Requirements</span></span>



| <span data-ttu-id="aabde-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aabde-114">Requirement</span></span> | <span data-ttu-id="aabde-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aabde-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aabde-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aabde-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aabde-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aabde-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aabde-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aabde-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aabde-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aabde-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aabde-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="aabde-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aabde-121"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="aabde-121"><dt>None</dt></span></span> </dl>        |
| <span data-ttu-id="aabde-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aabde-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="aabde-123"><dt>Rtworkq. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aabde-123"><dt>Rtworkq.lib</dt></span></span> </dl> |
| <span data-ttu-id="aabde-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aabde-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aabde-125"><dt>RTWorkQ.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aabde-125"><dt>RTWorkQ.dll</dt></span></span> </dl> |



 

 
