---
title: Codes d’erreur DirectComposition (Dcomp. h)
description: Cette section décrit les codes d’erreur spécifiques à DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104893"
---
# <a name="directcomposition-error-codes"></a><span data-ttu-id="26c46-103">Codes d’erreur DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26c46-103">DirectComposition error codes</span></span>

<span data-ttu-id="26c46-104">Si une erreur se produit, Microsoft DirectComposition retourne un code en tant que valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26c46-104">If an error occurs, Microsoft DirectComposition returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="26c46-105">Cette section décrit les codes d’erreur spécifiques à DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="26c46-105">This section describes the error codes that are specific to DirectComposition.</span></span> <span data-ttu-id="26c46-106">Pour obtenir la liste des codes d’erreur COM (Component Object Model) généraux, consultez [codes d’erreur com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="26c46-106">For a list of general Component Object Model (COM) error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="26c46-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_ \_ accès à l’erreur DCOMPOSITION \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="26c46-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION\_ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="26c46-108"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="26c46-108"><dt>


</dt> <dt></span></span>



<span data-ttu-id="26c46-109">Le handle de fenêtre qui a été spécifié dans un appel à la méthode [**IDCompositionDevice :: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) appartient à un processus différent de celui qui a créé l’objet appareil.</span><span class="sxs-lookup"><span data-stu-id="26c46-109">The window handle that was specified in a call to the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method belongs to a different process from the one that created the device object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26c46-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**</span><span class="sxs-lookup"><span data-stu-id="26c46-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="26c46-111"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="26c46-111"><dt>


</dt> <dt></span></span>



<span data-ttu-id="26c46-112">La surface était déjà rendue lorsque l’application a appelé la méthode [**IDCompositionSurface :: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface :: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)ou [**IDCompositionSurface :: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) .</span><span class="sxs-lookup"><span data-stu-id="26c46-112">The surface was already being rendered when the application called the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), or [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) method.</span></span> <span data-ttu-id="26c46-113">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="26c46-113">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26c46-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue**</span><span class="sxs-lookup"><span data-stu-id="26c46-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="26c46-115"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="26c46-115"><dt>


</dt> <dt></span></span>



<span data-ttu-id="26c46-116">L’application a appelé la méthode [**IDCompositionSurface :: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface :: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)ou [**IDCompositionSurface :: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) pour une surface qui n’est pas rendue.</span><span class="sxs-lookup"><span data-stu-id="26c46-116">The application called the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw), or [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) method for a surface that is not being rendered.</span></span> <span data-ttu-id="26c46-117">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="26c46-117">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26c46-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**\_fenêtre d’erreur DCOMPOSITION \_ \_ déjà \_ composée**</span><span class="sxs-lookup"><span data-stu-id="26c46-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION\_ERROR\_WINDOW\_ALREADY\_COMPOSED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="26c46-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="26c46-119"><dt>


</dt> <dt></span></span>



<span data-ttu-id="26c46-120">La méthode [**IDCompositionDevice :: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) a été appelée avec *HWND* et les paramètres de niveau *supérieur* pour lesquels une arborescence d’éléments visuels existe déjà.</span><span class="sxs-lookup"><span data-stu-id="26c46-120">The [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method was called with *hwnd* and *topmost* parameters for which a visual tree already exists.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26c46-121">Notes</span><span class="sxs-lookup"><span data-stu-id="26c46-121">Remarks</span></span>

<span data-ttu-id="26c46-122">Si un appel à [**IDCompositionSurface :: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) était l’action la plus récente :</span><span class="sxs-lookup"><span data-stu-id="26c46-122">If a call to the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) was the most recent action:</span></span>



| <span data-ttu-id="26c46-123">Appel de cette méthode :</span><span class="sxs-lookup"><span data-stu-id="26c46-123">Calling this method:</span></span>                                    | <span data-ttu-id="26c46-124">Retourne cette valeur :</span><span class="sxs-lookup"><span data-stu-id="26c46-124">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="26c46-125">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-125">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="26c46-126">**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**</span><span class="sxs-lookup"><span data-stu-id="26c46-126">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="26c46-127">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-127">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="26c46-128">\_OK</span><span class="sxs-lookup"><span data-stu-id="26c46-128">S\_OK</span></span>                                             |
| [<span data-ttu-id="26c46-129">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-129">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="26c46-130">\_OK</span><span class="sxs-lookup"><span data-stu-id="26c46-130">S\_OK</span></span>                                             |
| [<span data-ttu-id="26c46-131">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-131">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="26c46-132">**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**</span><span class="sxs-lookup"><span data-stu-id="26c46-132">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |



 

<span data-ttu-id="26c46-133">Si un appel à [**IDCompositionSurface :: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) était l’action la plus récente :</span><span class="sxs-lookup"><span data-stu-id="26c46-133">If a call to the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) was the most recent action:</span></span>



| <span data-ttu-id="26c46-134">Appel de cette méthode :</span><span class="sxs-lookup"><span data-stu-id="26c46-134">Calling this method:</span></span>                                    | <span data-ttu-id="26c46-135">Retourne cette valeur :</span><span class="sxs-lookup"><span data-stu-id="26c46-135">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="26c46-136">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-136">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="26c46-137">**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**</span><span class="sxs-lookup"><span data-stu-id="26c46-137">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="26c46-138">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-138">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="26c46-139">\_OK</span><span class="sxs-lookup"><span data-stu-id="26c46-139">S\_OK</span></span>                                             |
| [<span data-ttu-id="26c46-140">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-140">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="26c46-141">**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**</span><span class="sxs-lookup"><span data-stu-id="26c46-141">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="26c46-142">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-142">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="26c46-143">\_OK</span><span class="sxs-lookup"><span data-stu-id="26c46-143">S\_OK</span></span>                                             |



 

<span data-ttu-id="26c46-144">Si un appel à [**IDCompositionSurface :: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) était l’action la plus récente :</span><span class="sxs-lookup"><span data-stu-id="26c46-144">If a call to the [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) was the most recent action:</span></span>



| <span data-ttu-id="26c46-145">Appel de cette méthode :</span><span class="sxs-lookup"><span data-stu-id="26c46-145">Calling this method:</span></span>                                    | <span data-ttu-id="26c46-146">Retourne cette valeur :</span><span class="sxs-lookup"><span data-stu-id="26c46-146">Returns this value:</span></span>                                |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="26c46-147">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-147">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="26c46-148">**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**</span><span class="sxs-lookup"><span data-stu-id="26c46-148">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>  |
| [<span data-ttu-id="26c46-149">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-149">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="26c46-150">\_OK</span><span class="sxs-lookup"><span data-stu-id="26c46-150">S\_OK</span></span>                                              |
| [<span data-ttu-id="26c46-151">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-151">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="26c46-152">\_OK</span><span class="sxs-lookup"><span data-stu-id="26c46-152">S\_OK</span></span>                                              |
| [<span data-ttu-id="26c46-153">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-153">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="26c46-154">**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue.**</span><span class="sxs-lookup"><span data-stu-id="26c46-154">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED.**</span></span> |



 

<span data-ttu-id="26c46-155">Si un appel à [**IDCompositionSurface :: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) était l’action la plus récente :</span><span class="sxs-lookup"><span data-stu-id="26c46-155">If a call to the [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) was the most recent action:</span></span>



| <span data-ttu-id="26c46-156">Appel de cette méthode :</span><span class="sxs-lookup"><span data-stu-id="26c46-156">Calling this method:</span></span>                                    | <span data-ttu-id="26c46-157">Retourne cette valeur :</span><span class="sxs-lookup"><span data-stu-id="26c46-157">Returns this value:</span></span>                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="26c46-158">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-158">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="26c46-159">\_OK</span><span class="sxs-lookup"><span data-stu-id="26c46-159">S\_OK</span></span>                                                   |
| [<span data-ttu-id="26c46-160">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-160">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="26c46-161">**la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue.**</span><span class="sxs-lookup"><span data-stu-id="26c46-161">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="26c46-162">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-162">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="26c46-163">**la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue.**</span><span class="sxs-lookup"><span data-stu-id="26c46-163">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="26c46-164">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="26c46-164">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="26c46-165">**la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue.**</span><span class="sxs-lookup"><span data-stu-id="26c46-165">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="26c46-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26c46-166">Requirements</span></span>



| <span data-ttu-id="26c46-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26c46-167">Requirement</span></span> | <span data-ttu-id="26c46-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="26c46-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26c46-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26c46-169">Minimum supported client</span></span><br/> | <span data-ttu-id="26c46-170">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26c46-170">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="26c46-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26c46-171">Minimum supported server</span></span><br/> | <span data-ttu-id="26c46-172">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26c46-172">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26c46-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="26c46-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="26c46-174"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26c46-174"><dt>Dcomp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26c46-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26c46-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c46-176">Référence DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26c46-176">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

