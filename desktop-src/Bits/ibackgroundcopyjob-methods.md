---
title: Méthodes méthode ibackgroundcopyjob (BITS)
description: L’interface méthode ibackgroundcopyjob expose les méthodes suivantes. | Méthodes méthode ibackgroundcopyjob (BITS)
ms.assetid: CB1C6D64-416A-4F31-AC9D-B3C1A6818034
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a7ebeeefa90c90435f1294d78c4816cf77be3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530627"
---
# <a name="ibackgroundcopyjob-methods-bits"></a><span data-ttu-id="ef1f1-104">Méthodes méthode ibackgroundcopyjob (BITS)</span><span class="sxs-lookup"><span data-stu-id="ef1f1-104">IBackgroundCopyJob Methods (BITS)</span></span>

<span data-ttu-id="ef1f1-105">L’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-105">The [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef1f1-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ef1f1-106">In this section</span></span>

-   [<span data-ttu-id="ef1f1-107">**AddFile, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-107">**AddFile Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
-   [<span data-ttu-id="ef1f1-108">**Méthode AddFileSet**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-108">**AddFileSet Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
-   [<span data-ttu-id="ef1f1-109">**Cancel (méthode)**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-109">**Cancel Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   [<span data-ttu-id="ef1f1-110">**Méthode complète**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-110">**Complete Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
-   [<span data-ttu-id="ef1f1-111">**EnumFiles, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-111">**EnumFiles Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles)
-   [<span data-ttu-id="ef1f1-112">**GetDescription, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-112">**GetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdescription)
-   [<span data-ttu-id="ef1f1-113">**GetDisplayName, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-113">**GetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)
-   [<span data-ttu-id="ef1f1-114">**Méthode GetError**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-114">**GetError Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror)
-   [<span data-ttu-id="ef1f1-115">**Méthode GetErrorCount**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-115">**GetErrorCount Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterrorcount)
-   [<span data-ttu-id="ef1f1-116">**GetId, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-116">**GetId Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getid)
-   [<span data-ttu-id="ef1f1-117">**Méthode GetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-117">**GetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay)
-   [<span data-ttu-id="ef1f1-118">**Méthode GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-118">**GetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout)
-   [<span data-ttu-id="ef1f1-119">**Méthode GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-119">**GetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyflags)
-   [<span data-ttu-id="ef1f1-120">**Méthode GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-120">**GetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyinterface)
-   [<span data-ttu-id="ef1f1-121">**Méthode GetOwner**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-121">**GetOwner Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)
-   [<span data-ttu-id="ef1f1-122">**GetPriority, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-122">**GetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getpriority)
-   [<span data-ttu-id="ef1f1-123">**Méthode GetProgress**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-123">**GetProgress Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)
-   [<span data-ttu-id="ef1f1-124">**Méthode GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-124">**GetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getproxysettings)
-   [<span data-ttu-id="ef1f1-125">**Méthode GetState**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-125">**GetState Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate)
-   [<span data-ttu-id="ef1f1-126">**Méthode GetTimes**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-126">**GetTimes Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettimes)
-   [<span data-ttu-id="ef1f1-127">**GetType, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-127">**GetType Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettype)
-   [<span data-ttu-id="ef1f1-128">**Resume, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-128">**Resume Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
-   [<span data-ttu-id="ef1f1-129">**Méthode SetDescription**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-129">**SetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdescription)
-   [<span data-ttu-id="ef1f1-130">**Méthode SetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-130">**SetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdisplayname)
-   [<span data-ttu-id="ef1f1-131">**Méthode SetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-131">**SetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)
-   [<span data-ttu-id="ef1f1-132">**Méthode SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-132">**SetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)
-   [<span data-ttu-id="ef1f1-133">**Méthode SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-133">**SetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)
-   [<span data-ttu-id="ef1f1-134">**Méthode SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-134">**SetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)
-   [<span data-ttu-id="ef1f1-135">**SetPriority, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-135">**SetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)
-   [<span data-ttu-id="ef1f1-136">**Méthode Setproxysettings n'**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-136">**SetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)
-   [<span data-ttu-id="ef1f1-137">**Suspend, méthode**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-137">**Suspend Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)
-   [<span data-ttu-id="ef1f1-138">**Méthode TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="ef1f1-138">**TakeOwnership Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)

 

 




