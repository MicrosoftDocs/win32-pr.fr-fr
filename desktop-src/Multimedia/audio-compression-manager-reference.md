---
title: Référence du gestionnaire de compression audio
description: Référence du gestionnaire de compression audio
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Windows Multimedia, référence ACM
- multimédia, référence ACM
- audio multimédia, référence ACM
- audio, référence ACM)
- Audio Compression Manager (ACM), référence
- ACM (gestionnaire de compression audio), référence
- Référence ACM, à propos de
- référence pour ACM, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d365b0a69ecd94a07811b24762aa4bffdc8c9f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507870"
---
# <a name="audio-compression-manager-reference"></a><span data-ttu-id="2e9b0-111">Référence du gestionnaire de compression audio</span><span class="sxs-lookup"><span data-stu-id="2e9b0-111">Audio Compression Manager Reference</span></span>

<span data-ttu-id="2e9b0-112">Cette section décrit les fonctions, les structures et les messages associés à l’ACM.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-112">This section describes the functions, structures, and messages associated with the ACM.</span></span> <span data-ttu-id="2e9b0-113">Ces éléments sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-113">These elements are grouped as follows.</span></span>

## <a name="drivers"></a><span data-ttu-id="2e9b0-114">Pilotes</span><span class="sxs-lookup"><span data-stu-id="2e9b0-114">Drivers</span></span>

-   [<span data-ttu-id="2e9b0-115">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-115">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="2e9b0-116">**acmDriverClose**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-116">**acmDriverClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [<span data-ttu-id="2e9b0-117">**ACMDRIVERDETAILS**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-117">**ACMDRIVERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [<span data-ttu-id="2e9b0-118">**acmDriverEnum**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-118">**acmDriverEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [<span data-ttu-id="2e9b0-119">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-119">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="2e9b0-120">**acmDriverID**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-120">**acmDriverID**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [<span data-ttu-id="2e9b0-121">**acmDriverMessage**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-121">**acmDriverMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [<span data-ttu-id="2e9b0-122">**acmDriverOpen**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-122">**acmDriverOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [<span data-ttu-id="2e9b0-123">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-123">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="2e9b0-124">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-124">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [<span data-ttu-id="2e9b0-125">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-125">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a><span data-ttu-id="2e9b0-126">Filtres</span><span class="sxs-lookup"><span data-stu-id="2e9b0-126">Filters</span></span>

-   [<span data-ttu-id="2e9b0-127">**ACMFILTERCHOOSE**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-127">**ACMFILTERCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [<span data-ttu-id="2e9b0-128">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-128">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="2e9b0-129">**ACMFILTERDETAILS**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-129">**ACMFILTERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [<span data-ttu-id="2e9b0-130">**acmFilterEnum**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-130">**acmFilterEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [<span data-ttu-id="2e9b0-131">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-131">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="2e9b0-132">**ACMFILTERTAGDETAILS**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-132">**ACMFILTERTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [<span data-ttu-id="2e9b0-133">**acmFilterTagEnum**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-133">**acmFilterTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [<span data-ttu-id="2e9b0-134">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-134">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a><span data-ttu-id="2e9b0-135">Formats</span><span class="sxs-lookup"><span data-stu-id="2e9b0-135">Formats</span></span>

-   [<span data-ttu-id="2e9b0-136">**ACMFORMATCHOOSE**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-136">**ACMFORMATCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [<span data-ttu-id="2e9b0-137">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-137">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [<span data-ttu-id="2e9b0-138">**ACMFORMATDETAILS**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-138">**ACMFORMATDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [<span data-ttu-id="2e9b0-139">**acmFormatEnum**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-139">**acmFormatEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [<span data-ttu-id="2e9b0-140">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-140">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="2e9b0-141">**acmFormatSuggest**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-141">**acmFormatSuggest**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [<span data-ttu-id="2e9b0-142">**ACMFORMATTAGDETAILS**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-142">**ACMFORMATTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [<span data-ttu-id="2e9b0-143">**acmFormatTagEnum**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-143">**acmFormatTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [<span data-ttu-id="2e9b0-144">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-144">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a><span data-ttu-id="2e9b0-145">Messages</span><span class="sxs-lookup"><span data-stu-id="2e9b0-145">Messages</span></span>

-   [<span data-ttu-id="2e9b0-146">**MM \_ \_ FILTERCHOOSE ACM**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-146">**MM\_ACM\_FILTERCHOOSE**</span></span>](mm-acm-filterchoose.md)
-   [<span data-ttu-id="2e9b0-147">**MM \_ \_ FORMATCHOOSE ACM**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-147">**MM\_ACM\_FORMATCHOOSE**</span></span>](mm-acm-formatchoose.md)

## <a name="streams"></a><span data-ttu-id="2e9b0-148">Flux</span><span class="sxs-lookup"><span data-stu-id="2e9b0-148">Streams</span></span>

-   [<span data-ttu-id="2e9b0-149">**acmStreamClose**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-149">**acmStreamClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [<span data-ttu-id="2e9b0-150">**acmStreamConvert**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-150">**acmStreamConvert**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   <span data-ttu-id="2e9b0-151">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2e9b0-151">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>
-   [<span data-ttu-id="2e9b0-152">**ACMSTREAMHEADER**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-152">**ACMSTREAMHEADER**</span></span>](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [<span data-ttu-id="2e9b0-153">**acmStreamMessage**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-153">**acmStreamMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [<span data-ttu-id="2e9b0-154">**acmStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-154">**acmStreamOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [<span data-ttu-id="2e9b0-155">**acmStreamPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-155">**acmStreamPrepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [<span data-ttu-id="2e9b0-156">**acmStreamReset**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-156">**acmStreamReset**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [<span data-ttu-id="2e9b0-157">**acmStreamSize**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-157">**acmStreamSize**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [<span data-ttu-id="2e9b0-158">**acmStreamUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-158">**acmStreamUnprepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a><span data-ttu-id="2e9b0-159">Divers</span><span class="sxs-lookup"><span data-stu-id="2e9b0-159">Miscellaneous</span></span>

-   [<span data-ttu-id="2e9b0-160">**acmGetVersion**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-160">**acmGetVersion**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [<span data-ttu-id="2e9b0-161">**acmMetrics**</span><span class="sxs-lookup"><span data-stu-id="2e9b0-161">**acmMetrics**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a><span data-ttu-id="2e9b0-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2e9b0-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e9b0-163">Gestionnaire de compression audio</span><span class="sxs-lookup"><span data-stu-id="2e9b0-163">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> </dl>

 

 