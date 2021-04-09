---
description: La classe CInstance expose les méthodes suivantes.
ms.assetid: B9846350-405D-440E-AC35-16446D3F03F5
ms.tgt_platform: multiple
title: Méthodes CInstance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e088f4604263d3fd1673982e22e2f6c88f991b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866901"
---
# <a name="cinstance-methods"></a><span data-ttu-id="d0b1b-103">Méthodes CInstance</span><span class="sxs-lookup"><span data-stu-id="d0b1b-103">CInstance Methods</span></span>

<span data-ttu-id="d0b1b-104">\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="d0b1b-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d0b1b-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="d0b1b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d0b1b-106">La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0b1b-106">The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d0b1b-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d0b1b-107">In this section</span></span>

-   [<span data-ttu-id="d0b1b-108">**Commit, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-108">**Commit method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-commit)
-   [<span data-ttu-id="d0b1b-109">**Méthode Getbool**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-109">**Getbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbool)
-   [<span data-ttu-id="d0b1b-110">**GetByte, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-110">**GetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbyte)
-   [<span data-ttu-id="d0b1b-111">**Méthode GetCHString**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-111">**GetCHString method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getchstring)
-   [<span data-ttu-id="d0b1b-112">**Méthode GetClassObjectInterface**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-112">**GetClassObjectInterface method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getclassobjectinterface)
-   [<span data-ttu-id="d0b1b-113">**GetDateTime, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-113">**GetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdatetime)
-   [<span data-ttu-id="d0b1b-114">**GetDOUBLE, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-114">**GetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdouble)
-   [<span data-ttu-id="d0b1b-115">**Méthode GetDWORD**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-115">**GetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdword)
-   [<span data-ttu-id="d0b1b-116">**Méthode GetEmbeddedObject**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-116">**GetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getembeddedobject)
-   [<span data-ttu-id="d0b1b-117">**Méthode GetMethodContext**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-117">**GetMethodContext method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getmethodcontext)
-   [<span data-ttu-id="d0b1b-118">**GetStatus, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-118">**GetStatus method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstatus)
-   [<span data-ttu-id="d0b1b-119">**Méthode GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-119">**GetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstringarray)
-   [<span data-ttu-id="d0b1b-120">**GetTimeSpan, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-120">**GetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-gettimespan)
-   [<span data-ttu-id="d0b1b-121">**Méthode GetVariant**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-121">**GetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getvariant)
-   [<span data-ttu-id="d0b1b-122">**Méthode GetWBEMINT16**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-122">**GetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwbemint16)
-   [<span data-ttu-id="d0b1b-123">**Méthodes GetWBEMINT64**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-123">**GetWBEMINT64 methods**</span></span>](cinstance-getwbemint64.md)
-   [<span data-ttu-id="d0b1b-124">**Méthode GetWCHAR**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-124">**GetWCHAR method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwchar)
-   [<span data-ttu-id="d0b1b-125">**Méthode GetWORD**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-125">**GetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getword)
-   [<span data-ttu-id="d0b1b-126">**IsNull, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-126">**IsNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-isnull)
-   [<span data-ttu-id="d0b1b-127">**Méthode SetBool**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-127">**Setbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbool)
-   [<span data-ttu-id="d0b1b-128">**SetByte, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-128">**SetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbyte)
-   [<span data-ttu-id="d0b1b-129">**Méthodes SetCharSplat**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-129">**SetCharSplat methods**</span></span>](cinstance-setcharsplat.md)
-   [<span data-ttu-id="d0b1b-130">**Méthodes SetCHString**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-130">**SetCHString methods**</span></span>](cinstance-setchstring.md)
-   [<span data-ttu-id="d0b1b-131">**SetDateTime, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-131">**SetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdatetime)
-   [<span data-ttu-id="d0b1b-132">**SetDOUBLE, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-132">**SetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdouble)
-   [<span data-ttu-id="d0b1b-133">**Méthode SetDWORD**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-133">**SetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdword)
-   [<span data-ttu-id="d0b1b-134">**Méthode SetEmbeddedObject**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-134">**SetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setembeddedobject)
-   [<span data-ttu-id="d0b1b-135">**SetNull, méthode**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-135">**SetNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setnull)
-   [<span data-ttu-id="d0b1b-136">**Méthode SetStringArray**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-136">**SetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setstringarray)
-   [<span data-ttu-id="d0b1b-137">**Méthode SetTimeSpan**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-137">**SetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-settimespan)
-   [<span data-ttu-id="d0b1b-138">**Méthode SetVariant**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-138">**SetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setvariant)
-   [<span data-ttu-id="d0b1b-139">**Méthode SetWBEMINT16**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-139">**SetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwbemint16)
-   [<span data-ttu-id="d0b1b-140">**Méthode SetWCHARSplat**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-140">**SetWCHARSplat method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwcharsplat)
-   <span data-ttu-id="d0b1b-141">[**Méthodes SetWBEMINT64**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0b1b-141">[**SetWBEMINT64 methods**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span></span>
-   [<span data-ttu-id="d0b1b-142">**Méthode SetWORD**</span><span class="sxs-lookup"><span data-stu-id="d0b1b-142">**SetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setword)

 

 
