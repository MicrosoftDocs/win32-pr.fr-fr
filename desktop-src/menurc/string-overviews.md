---
title: Fonctions strsafe
description: Fonctions strsafe
ms.assetid: 3590dd8d-3a88-4dde-a5fe-f10e12354919
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292e6f83175848338a6804c9787efb4660da9f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092647"
---
# <a name="strsafe-functions"></a><span data-ttu-id="3fbef-103">Fonctions strsafe</span><span class="sxs-lookup"><span data-stu-id="3fbef-103">Strsafe Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3fbef-104">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3fbef-104">In this section</span></span>

-   [<span data-ttu-id="3fbef-105">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="3fbef-105">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)
-   [<span data-ttu-id="3fbef-106">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-106">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)
-   [<span data-ttu-id="3fbef-107">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="3fbef-107">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)
-   [<span data-ttu-id="3fbef-108">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-108">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)
-   [<span data-ttu-id="3fbef-109">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="3fbef-109">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)
-   [<span data-ttu-id="3fbef-110">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-110">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)
-   [<span data-ttu-id="3fbef-111">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="3fbef-111">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)
-   [<span data-ttu-id="3fbef-112">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-112">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)
-   [<span data-ttu-id="3fbef-113">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="3fbef-113">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)
-   [<span data-ttu-id="3fbef-114">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-114">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)
-   [<span data-ttu-id="3fbef-115">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="3fbef-115">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)
-   [<span data-ttu-id="3fbef-116">**StringCbPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="3fbef-116">**StringCbPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_la)
-   [<span data-ttu-id="3fbef-117">**StringCbPrintf \_ Lex**</span><span class="sxs-lookup"><span data-stu-id="3fbef-117">**StringCbPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_lexa)
-   [<span data-ttu-id="3fbef-118">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="3fbef-118">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)
-   [<span data-ttu-id="3fbef-119">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-119">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)
-   [<span data-ttu-id="3fbef-120">**StringCbVPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="3fbef-120">**StringCbVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_la)
-   [<span data-ttu-id="3fbef-121">**StringCbVPrintf \_ Lex**</span><span class="sxs-lookup"><span data-stu-id="3fbef-121">**StringCbVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_lexa)
-   [<span data-ttu-id="3fbef-122">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="3fbef-122">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)
-   [<span data-ttu-id="3fbef-123">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-123">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)
-   [<span data-ttu-id="3fbef-124">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="3fbef-124">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)
-   [<span data-ttu-id="3fbef-125">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-125">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)
-   [<span data-ttu-id="3fbef-126">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="3fbef-126">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)
-   [<span data-ttu-id="3fbef-127">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-127">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)
-   [<span data-ttu-id="3fbef-128">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="3fbef-128">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)
-   [<span data-ttu-id="3fbef-129">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-129">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)
-   [<span data-ttu-id="3fbef-130">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="3fbef-130">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)
-   [<span data-ttu-id="3fbef-131">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-131">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)
-   [<span data-ttu-id="3fbef-132">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="3fbef-132">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)
-   [<span data-ttu-id="3fbef-133">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-133">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)
-   [<span data-ttu-id="3fbef-134">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="3fbef-134">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)
-   [<span data-ttu-id="3fbef-135">**StringCchPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="3fbef-135">**StringCchPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_la)
-   [<span data-ttu-id="3fbef-136">**StringCchPrintf \_ Lex**</span><span class="sxs-lookup"><span data-stu-id="3fbef-136">**StringCchPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_lexa)
-   [<span data-ttu-id="3fbef-137">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="3fbef-137">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)
-   [<span data-ttu-id="3fbef-138">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-138">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)
-   [<span data-ttu-id="3fbef-139">**StringCchVPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="3fbef-139">**StringCchVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_la)
-   [<span data-ttu-id="3fbef-140">**StringCchVPrintf \_ Lex**</span><span class="sxs-lookup"><span data-stu-id="3fbef-140">**StringCchVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_lexa)
-   [<span data-ttu-id="3fbef-141">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="3fbef-141">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)
-   [<span data-ttu-id="3fbef-142">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="3fbef-142">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)
-   <span data-ttu-id="3fbef-143">[**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3fbef-143">[**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span></span>
-   <span data-ttu-id="3fbef-144">[**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3fbef-144">[**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span></span>

 

 
