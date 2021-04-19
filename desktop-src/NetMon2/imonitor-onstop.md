---
description: La méthode OnStop doit être implémentée par l’analyse. Le MSCVC appelle cette méthode pour informer le moniteur que la capture sera arrêtée.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'IMonitor :: OnStop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513174"
---
# <a name="imonitoronstop-method"></a><span data-ttu-id="e290a-104">IMonitor :: OnStop, méthode</span><span class="sxs-lookup"><span data-stu-id="e290a-104">IMonitor::OnStop method</span></span>

<span data-ttu-id="e290a-105">La méthode **OnStop** doit être implémentée par l’analyse.</span><span class="sxs-lookup"><span data-stu-id="e290a-105">The **OnStop** method must be implemented by the monitor.</span></span> <span data-ttu-id="e290a-106">Le MSCVC appelle cette méthode pour informer le moniteur que la capture sera arrêtée.</span><span class="sxs-lookup"><span data-stu-id="e290a-106">The MSCVC calls this method to notify the monitor that the capture will be stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="e290a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e290a-107">Syntax</span></span>


```C++
HRESULT OnStop();
```



## <a name="parameters"></a><span data-ttu-id="e290a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e290a-108">Parameters</span></span>

<span data-ttu-id="e290a-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e290a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e290a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e290a-110">Return value</span></span>

<span data-ttu-id="e290a-111">Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).</span><span class="sxs-lookup"><span data-stu-id="e290a-111">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="e290a-112">Si la méthode échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e290a-112">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="e290a-113">Lorsqu’un code d’erreur est retourné, l’analyse ne peut pas être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="e290a-113">When an error code is returned, the monitor cannot be restarted.</span></span>

## <a name="remarks"></a><span data-ttu-id="e290a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e290a-114">Remarks</span></span>

<span data-ttu-id="e290a-115">MCSVC appelle cette méthode après l’appel de [IRTC :: Stop](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="e290a-115">The MCSVC calls this method after [IRTC::Stop](irtc-stop.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e290a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e290a-116">Requirements</span></span>



| <span data-ttu-id="e290a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e290a-117">Requirement</span></span> | <span data-ttu-id="e290a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e290a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e290a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e290a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e290a-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e290a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e290a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e290a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e290a-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e290a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e290a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e290a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e290a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e290a-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




