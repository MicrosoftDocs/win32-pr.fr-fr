---
title: IMsTscAx propriété VerticalScrollBarVisible
description: Indique si le contrôle affiche une barre de défilement verticale.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464682"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a><span data-ttu-id="e1e08-124">IMsTscAx :: VerticalScrollBarVisible, propriété</span><span class="sxs-lookup"><span data-stu-id="e1e08-124">IMsTscAx::VerticalScrollBarVisible property</span></span>

<span data-ttu-id="e1e08-125">Indique si le contrôle affiche une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="e1e08-125">Indicates whether the control displays a vertical scroll bar.</span></span>

<span data-ttu-id="e1e08-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e1e08-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e08-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1e08-127">Syntax</span></span>


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="e1e08-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e1e08-128">Property value</span></span>

<span data-ttu-id="e1e08-129">La valeur de ce paramètre est **true** si la barre de défilement verticale est visible, et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e1e08-129">The value of this parameter is **TRUE** if the vertical scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e1e08-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e1e08-130">Error codes</span></span>

<span data-ttu-id="e1e08-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e1e08-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1e08-132">Notes</span><span class="sxs-lookup"><span data-stu-id="e1e08-132">Remarks</span></span>

<span data-ttu-id="e1e08-133">Le contrôle affiche automatiquement une barre de défilement verticale si la hauteur du contrôle actuel est inférieure à la hauteur du bureau.</span><span class="sxs-lookup"><span data-stu-id="e1e08-133">The control automatically displays a vertical scroll bar if the height of the current control is less than the height of the desktop.</span></span>

<span data-ttu-id="e1e08-134">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e1e08-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1e08-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1e08-135">Requirements</span></span>



| <span data-ttu-id="e1e08-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1e08-136">Requirement</span></span> | <span data-ttu-id="e1e08-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e08-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e08-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e08-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e08-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1e08-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e1e08-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e08-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e08-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1e08-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e1e08-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e1e08-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1e08-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1e08-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1e08-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e1e08-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1e08-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1e08-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1e08-146">IID</span><span class="sxs-lookup"><span data-stu-id="e1e08-146">IID</span></span><br/>                      | <span data-ttu-id="e1e08-147">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e1e08-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e1e08-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1e08-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1e08-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="e1e08-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e1e08-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e1e08-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e1e08-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e1e08-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e1e08-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e1e08-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e1e08-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e1e08-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e1e08-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e1e08-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e1e08-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e1e08-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e1e08-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e1e08-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e1e08-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e1e08-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e1e08-158">**HorizontalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="e1e08-158">**HorizontalScrollBarVisible**</span></span>](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[<span data-ttu-id="e1e08-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="e1e08-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





