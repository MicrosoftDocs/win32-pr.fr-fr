---
title: Fonctions de contrôle
description: Fonctions de contrôle
ms.assetid: 9774a320-1d00-48a4-ba13-fb1cd683a635
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7099afab5c035e394eafc30c4475dbe6bc97cec5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523796"
---
# <a name="control-functions"></a><span data-ttu-id="82bc1-103">Fonctions de contrôle</span><span class="sxs-lookup"><span data-stu-id="82bc1-103">Control Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="82bc1-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="82bc1-104">In This Section</span></span>

-   [<span data-ttu-id="82bc1-105">**DoReaderMode**</span><span class="sxs-lookup"><span data-stu-id="82bc1-105">**DoReaderMode**</span></span>](doreadermode.md)
-   [<span data-ttu-id="82bc1-106">**\_Clone DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-106">**DPA\_Clone**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_clone)
-   [<span data-ttu-id="82bc1-107">**\_Création DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-107">**DPA\_Create**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_create)
-   [<span data-ttu-id="82bc1-108">**\_CREATEEX DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-108">**DPA\_CreateEx**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_createex)
-   [<span data-ttu-id="82bc1-109">**\_DELETEALLPTRS DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-109">**DPA\_DeleteAllPtrs**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteallptrs)
-   [<span data-ttu-id="82bc1-110">**\_DELETEPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-110">**DPA\_DeletePtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteptr)
-   [<span data-ttu-id="82bc1-111">**\_Destruction DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-111">**DPA\_Destroy**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroy)
-   [<span data-ttu-id="82bc1-112">**\_DESTROYCALLBACK DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-112">**DPA\_DestroyCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroycallback)
-   [<span data-ttu-id="82bc1-113">**\_ENUMCALLBACK DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-113">**DPA\_EnumCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_enumcallback)
-   [<span data-ttu-id="82bc1-114">**\_GETPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-114">**DPA\_GetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptr)
-   [<span data-ttu-id="82bc1-115">**\_GETPTRINDEX DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-115">**DPA\_GetPtrIndex**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptrindex)
-   [<span data-ttu-id="82bc1-116">**\_Obtenir la propriété DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-116">**DPA\_GetSize**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getsize)
-   [<span data-ttu-id="82bc1-117">**\_Croissance DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-117">**DPA\_Grow**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_grow)
-   [<span data-ttu-id="82bc1-118">**\_INSERTPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-118">**DPA\_InsertPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_insertptr)
-   [<span data-ttu-id="82bc1-119">**\_LOADSTREAM DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-119">**DPA\_LoadStream**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_loadstream)
-   [<span data-ttu-id="82bc1-120">**\_Fusion DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-120">**DPA\_Merge**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_merge)
-   [<span data-ttu-id="82bc1-121">**\_SAVESTREAM DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-121">**DPA\_SaveStream**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_savestream)
-   [<span data-ttu-id="82bc1-122">**\_Recherche DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-122">**DPA\_Search**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search)
-   [<span data-ttu-id="82bc1-123">**\_SETPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-123">**DPA\_SetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_setptr)
-   [<span data-ttu-id="82bc1-124">**\_Tri DPA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-124">**DPA\_Sort**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_sort)
-   [<span data-ttu-id="82bc1-125">**DrawShadowText**</span><span class="sxs-lookup"><span data-stu-id="82bc1-125">**DrawShadowText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-drawshadowtext)
-   [<span data-ttu-id="82bc1-126">**DrawTextExPrivWrap**</span><span class="sxs-lookup"><span data-stu-id="82bc1-126">**DrawTextExPrivWrap**</span></span>](drawtextexprivwrap.md)
-   [<span data-ttu-id="82bc1-127">**DrawTextWrap**</span><span class="sxs-lookup"><span data-stu-id="82bc1-127">**DrawTextWrap**</span></span>](drawtextwrap.md)
-   [<span data-ttu-id="82bc1-128">**\_Clone DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-128">**DSA\_Clone**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_clone)
-   [<span data-ttu-id="82bc1-129">**\_Création DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-129">**DSA\_Create**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_create)
-   [<span data-ttu-id="82bc1-130">**\_DELETEALLITEMS DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-130">**DSA\_DeleteAllItems**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteallitems)
-   [<span data-ttu-id="82bc1-131">**DSA \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="82bc1-131">**DSA\_DeleteItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteitem)
-   [<span data-ttu-id="82bc1-132">**DSA \_ Destroy**</span><span class="sxs-lookup"><span data-stu-id="82bc1-132">**DSA\_Destroy**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroy)
-   [<span data-ttu-id="82bc1-133">**\_DESTROYCALLBACK DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-133">**DSA\_DestroyCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroycallback)
-   [<span data-ttu-id="82bc1-134">**\_ENUMCALLBACK DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-134">**DSA\_EnumCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_enumcallback)
-   [<span data-ttu-id="82bc1-135">**DSA \_ GetItem**</span><span class="sxs-lookup"><span data-stu-id="82bc1-135">**DSA\_GetItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitem)
-   [<span data-ttu-id="82bc1-136">**\_GETITEMPTR DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-136">**DSA\_GetItemPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitemptr)
-   [<span data-ttu-id="82bc1-137">**Obtient le DSA \_**</span><span class="sxs-lookup"><span data-stu-id="82bc1-137">**DSA\_GetSize**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getsize)
-   [<span data-ttu-id="82bc1-138">**L' \_ INSERTITEM DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-138">**DSA\_InsertItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_insertitem)
-   [<span data-ttu-id="82bc1-139">**\_SETITEM DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-139">**DSA\_SetItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_setitem)
-   [<span data-ttu-id="82bc1-140">**\_Tri DSA**</span><span class="sxs-lookup"><span data-stu-id="82bc1-140">**DSA\_Sort**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort)
-   [<span data-ttu-id="82bc1-141">**ExtTextOutWrap**</span><span class="sxs-lookup"><span data-stu-id="82bc1-141">**ExtTextOutWrap**</span></span>](exttextoutwrap.md)
-   [<span data-ttu-id="82bc1-142">**GetEffectiveClientRect**</span><span class="sxs-lookup"><span data-stu-id="82bc1-142">**GetEffectiveClientRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-geteffectiveclientrect)
-   [<span data-ttu-id="82bc1-143">**GetMUILanguage**</span><span class="sxs-lookup"><span data-stu-id="82bc1-143">**GetMUILanguage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage)
-   [<span data-ttu-id="82bc1-144">**GetTextExtentPoint32Wrap**</span><span class="sxs-lookup"><span data-stu-id="82bc1-144">**GetTextExtentPoint32Wrap**</span></span>](gettextextentpoint32wrap.md)
-   [<span data-ttu-id="82bc1-145">**InitCommonControls**</span><span class="sxs-lookup"><span data-stu-id="82bc1-145">**InitCommonControls**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)
-   [<span data-ttu-id="82bc1-146">**InitCommonControlsEx**</span><span class="sxs-lookup"><span data-stu-id="82bc1-146">**InitCommonControlsEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)
-   [<span data-ttu-id="82bc1-147">**InitMUILanguage**</span><span class="sxs-lookup"><span data-stu-id="82bc1-147">**InitMUILanguage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)
-   [<span data-ttu-id="82bc1-148">**LoadIconMetric**</span><span class="sxs-lookup"><span data-stu-id="82bc1-148">**LoadIconMetric**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-loadiconmetric)
-   [<span data-ttu-id="82bc1-149">**LoadIconWithScaleDown**</span><span class="sxs-lookup"><span data-stu-id="82bc1-149">**LoadIconWithScaleDown**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-loadiconwithscaledown)
-   [<span data-ttu-id="82bc1-150">**MirrorIcon**</span><span class="sxs-lookup"><span data-stu-id="82bc1-150">**MirrorIcon**</span></span>](mirroricon.md)
-   [<span data-ttu-id="82bc1-151">**PFNDACOMPARE**</span><span class="sxs-lookup"><span data-stu-id="82bc1-151">**PFNDACOMPARE**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare)
-   [<span data-ttu-id="82bc1-152">**PFNDACOMPARECONST**</span><span class="sxs-lookup"><span data-stu-id="82bc1-152">**PFNDACOMPARECONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompareconst)
-   [<span data-ttu-id="82bc1-153">**PFNDAENUMCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="82bc1-153">**PFNDAENUMCALLBACK**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback)
-   [<span data-ttu-id="82bc1-154">**PFNDAENUMCALLBACKCONST**</span><span class="sxs-lookup"><span data-stu-id="82bc1-154">**PFNDAENUMCALLBACKCONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallbackconst)
-   <span data-ttu-id="82bc1-155">[**PFNDPACOMPARE**](/previous-versions/windows/desktop/legacy/bb775715(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82bc1-155">[**PFNDPACOMPARE**](/previous-versions/windows/desktop/legacy/bb775715(v=vs.85))</span></span>
-   <span data-ttu-id="82bc1-156">[**PFNDPACOMPARECONST**](/previous-versions/windows/desktop/legacy/bb775717(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82bc1-156">[**PFNDPACOMPARECONST**](/previous-versions/windows/desktop/legacy/bb775717(v=vs.85))</span></span>
-   <span data-ttu-id="82bc1-157">[**PFNDPAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775719(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82bc1-157">[**PFNDPAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775719(v=vs.85))</span></span>
-   [<span data-ttu-id="82bc1-158">**PFNDPAMERGE**</span><span class="sxs-lookup"><span data-stu-id="82bc1-158">**PFNDPAMERGE**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge)
-   [<span data-ttu-id="82bc1-159">**PFNDPAMERGECONST**</span><span class="sxs-lookup"><span data-stu-id="82bc1-159">**PFNDPAMERGECONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamergeconst)
-   [<span data-ttu-id="82bc1-160">**PFNDPASTREAM**</span><span class="sxs-lookup"><span data-stu-id="82bc1-160">**PFNDPASTREAM**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpastream)
-   <span data-ttu-id="82bc1-161">[**PFNDSAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82bc1-161">[**PFNDSAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775727(v=vs.85))</span></span>
-   [<span data-ttu-id="82bc1-162">**ReaderScroll**</span><span class="sxs-lookup"><span data-stu-id="82bc1-162">**ReaderScroll**</span></span>](readerscroll.md)
-   [<span data-ttu-id="82bc1-163">**ShowHideMenuCtl**</span><span class="sxs-lookup"><span data-stu-id="82bc1-163">**ShowHideMenuCtl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-showhidemenuctl)
-   [<span data-ttu-id="82bc1-164">**Chaîne \_ GetPtr**</span><span class="sxs-lookup"><span data-stu-id="82bc1-164">**Str\_GetPtr**</span></span>](str-getptr.md)
-   [<span data-ttu-id="82bc1-165">**Chaîne \_ SetPtr**</span><span class="sxs-lookup"><span data-stu-id="82bc1-165">**Str\_SetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-str_setptrw)
-   [<span data-ttu-id="82bc1-166">**TranslateDispatch**</span><span class="sxs-lookup"><span data-stu-id="82bc1-166">**TranslateDispatch**</span></span>](translatedispatch.md)

 

 
