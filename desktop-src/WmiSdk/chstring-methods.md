---
description: La classe CHString expose les méthodes suivantes.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Méthodes CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034728"
---
# <a name="chstring-methods"></a><span data-ttu-id="99cc4-103">Méthodes CHString</span><span class="sxs-lookup"><span data-stu-id="99cc4-103">CHString Methods</span></span>

<span data-ttu-id="99cc4-104">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="99cc4-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="99cc4-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="99cc4-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="99cc4-106">La classe [**CHString**](chstring.md) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="99cc4-106">The [**CHString**](chstring.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99cc4-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="99cc4-107">In this section</span></span>

-   [<span data-ttu-id="99cc4-108">**Méthode AllocSysString**</span><span class="sxs-lookup"><span data-stu-id="99cc4-108">**AllocSysString method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   <span data-ttu-id="99cc4-109">[**Constructeurs CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="99cc4-109">[**CHString constructors**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span></span>
-   [<span data-ttu-id="99cc4-110">**COLLATE, méthode**</span><span class="sxs-lookup"><span data-stu-id="99cc4-110">**Collate method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [<span data-ttu-id="99cc4-111">**Compare (méthode)**</span><span class="sxs-lookup"><span data-stu-id="99cc4-111">**Compare method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [<span data-ttu-id="99cc4-112">**Méthode CompareNoCase**</span><span class="sxs-lookup"><span data-stu-id="99cc4-112">**CompareNoCase method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [<span data-ttu-id="99cc4-113">**Empty, méthode**</span><span class="sxs-lookup"><span data-stu-id="99cc4-113">**Empty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   <span data-ttu-id="99cc4-114">[**Méthodes Find**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span><span class="sxs-lookup"><span data-stu-id="99cc4-114">[**Find methods**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span></span>
-   [<span data-ttu-id="99cc4-115">**Méthode FindOneOf**</span><span class="sxs-lookup"><span data-stu-id="99cc4-115">**FindOneOf method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   <span data-ttu-id="99cc4-116">[**Méthodes de format**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span><span class="sxs-lookup"><span data-stu-id="99cc4-116">[**Format methods**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span></span>
-   <span data-ttu-id="99cc4-117">[**Méthodes FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span><span class="sxs-lookup"><span data-stu-id="99cc4-117">[**FormatMessageW methods**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span></span>
-   [<span data-ttu-id="99cc4-118">**Méthode FormatV**</span><span class="sxs-lookup"><span data-stu-id="99cc4-118">**FormatV method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [<span data-ttu-id="99cc4-119">**Méthode FreeExtra**</span><span class="sxs-lookup"><span data-stu-id="99cc4-119">**FreeExtra method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [<span data-ttu-id="99cc4-120">**Méthode GetAllocLength**</span><span class="sxs-lookup"><span data-stu-id="99cc4-120">**GetAllocLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   <span data-ttu-id="99cc4-121">[**GetAt, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span><span class="sxs-lookup"><span data-stu-id="99cc4-121">[**GetAt method**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span></span>
-   [<span data-ttu-id="99cc4-122">**GetBuffer (méthode)**</span><span class="sxs-lookup"><span data-stu-id="99cc4-122">**GetBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [<span data-ttu-id="99cc4-123">**Méthode GetBufferSetLength**</span><span class="sxs-lookup"><span data-stu-id="99cc4-123">**GetBufferSetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [<span data-ttu-id="99cc4-124">**GetData, méthode**</span><span class="sxs-lookup"><span data-stu-id="99cc4-124">**GetData method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [<span data-ttu-id="99cc4-125">**GetLength, méthode**</span><span class="sxs-lookup"><span data-stu-id="99cc4-125">**GetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [<span data-ttu-id="99cc4-126">**IsEmpty (méthode)**</span><span class="sxs-lookup"><span data-stu-id="99cc4-126">**IsEmpty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [<span data-ttu-id="99cc4-127">**Left, méthode**</span><span class="sxs-lookup"><span data-stu-id="99cc4-127">**Left method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   <span data-ttu-id="99cc4-128">[**Méthode LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span><span class="sxs-lookup"><span data-stu-id="99cc4-128">[**LoadStringW method**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span></span>
-   [<span data-ttu-id="99cc4-129">**Méthode LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="99cc4-129">**LockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [<span data-ttu-id="99cc4-130">**Méthode MakeLower**</span><span class="sxs-lookup"><span data-stu-id="99cc4-130">**MakeLower method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [<span data-ttu-id="99cc4-131">**Méthode MakeReverse**</span><span class="sxs-lookup"><span data-stu-id="99cc4-131">**MakeReverse method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [<span data-ttu-id="99cc4-132">**Méthode MakeUpper**</span><span class="sxs-lookup"><span data-stu-id="99cc4-132">**MakeUpper method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   <span data-ttu-id="99cc4-133">[**Méthodes Mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="99cc4-133">[**Mid methods**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>
-   <span data-ttu-id="99cc4-134">[**Method, opérateur \[ \]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-134">[**operator\[\] method**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span></span>
-   [<span data-ttu-id="99cc4-135">**CHString :: Operator +**</span><span class="sxs-lookup"><span data-stu-id="99cc4-135">**CHString::operator+**</span></span>](chstring--operator-plus.md)
-   [<span data-ttu-id="99cc4-136">**CHString :: Operator + =**</span><span class="sxs-lookup"><span data-stu-id="99cc4-136">**CHString::operator+=**</span></span>](chstring--operator-plus-equal.md)
-   [<span data-ttu-id="99cc4-137">**CHString :: Operator =**</span><span class="sxs-lookup"><span data-stu-id="99cc4-137">**CHString::operator=**</span></span>](chstring--operator-equal.md)
-   <span data-ttu-id="99cc4-138">[**Operator = = (constCHString&, constCHString&), méthode**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-138">[**operator==(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-139">[**Operator = = (constCHString&, constLPCWSTR&), méthode**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-139">[**operator==(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-140">[**méthode> Operator (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-140">[**operator>(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-141">[**méthode> Operator (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-141">[**operator>(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-142">[**Méthode Operator>= (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-142">[**operator>=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-143">[**Méthode Operator>= (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-143">[**operator>=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-144">[**méthode< Operator (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-144">[**operator<(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-145">[**méthode< Operator (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-145">[**operator<(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-146">[**Méthode Operator<= (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-146">[**operator<=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-147">[**Méthode Operator<= (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-147">[**operator<=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-148">[**Méthode Operator ! = (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-148">[**operator!=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span></span>
-   <span data-ttu-id="99cc4-149">[**Méthode Operator ! = (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99cc4-149">[**operator!=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span></span>
-   [<span data-ttu-id="99cc4-150">**Operator LPCWSTR, méthode**</span><span class="sxs-lookup"><span data-stu-id="99cc4-150">**operator LPCWSTR method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [<span data-ttu-id="99cc4-151">**Méthode ReleaseBuffer**</span><span class="sxs-lookup"><span data-stu-id="99cc4-151">**ReleaseBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [<span data-ttu-id="99cc4-152">**Méthode ReverseFind**</span><span class="sxs-lookup"><span data-stu-id="99cc4-152">**ReverseFind method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [<span data-ttu-id="99cc4-153">**Right, méthode**</span><span class="sxs-lookup"><span data-stu-id="99cc4-153">**Right method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [<span data-ttu-id="99cc4-154">**Méthode SetAt**</span><span class="sxs-lookup"><span data-stu-id="99cc4-154">**SetAt method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [<span data-ttu-id="99cc4-155">**Méthode SpanExcluding**</span><span class="sxs-lookup"><span data-stu-id="99cc4-155">**SpanExcluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [<span data-ttu-id="99cc4-156">**Méthode SpanIncluding**</span><span class="sxs-lookup"><span data-stu-id="99cc4-156">**SpanIncluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [<span data-ttu-id="99cc4-157">**Méthode TrimLeft**</span><span class="sxs-lookup"><span data-stu-id="99cc4-157">**TrimLeft method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [<span data-ttu-id="99cc4-158">**Méthode TrimRight**</span><span class="sxs-lookup"><span data-stu-id="99cc4-158">**TrimRight method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [<span data-ttu-id="99cc4-159">**Méthode UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="99cc4-159">**UnlockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
