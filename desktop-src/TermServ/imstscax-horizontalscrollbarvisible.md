---
title: IMsTscAx propriété HorizontalScrollBarVisible
description: Indique si le contrôle a affiché une barre de défilement horizontale.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété HorizontalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032786"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a><span data-ttu-id="9a58b-124">IMsTscAx :: HorizontalScrollBarVisible, propriété</span><span class="sxs-lookup"><span data-stu-id="9a58b-124">IMsTscAx::HorizontalScrollBarVisible property</span></span>

<span data-ttu-id="9a58b-125">Indique si le contrôle a affiché une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="9a58b-125">Indicates whether the control has displayed a horizontal scroll bar.</span></span>

<span data-ttu-id="9a58b-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a58b-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a58b-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a58b-127">Syntax</span></span>


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="9a58b-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a58b-128">Property value</span></span>

<span data-ttu-id="9a58b-129">La valeur de ce paramètre est **true** si la barre de défilement horizontale est visible, et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9a58b-129">The value of this parameter is **TRUE** if the horizontal scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a58b-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9a58b-130">Error codes</span></span>

<span data-ttu-id="9a58b-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9a58b-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a58b-132">Notes</span><span class="sxs-lookup"><span data-stu-id="9a58b-132">Remarks</span></span>

<span data-ttu-id="9a58b-133">Le contrôle affiche automatiquement une barre de défilement horizontale si la largeur du contrôle est inférieure à la largeur du bureau.</span><span class="sxs-lookup"><span data-stu-id="9a58b-133">The control automatically displays a horizontal scroll bar if the width of the control is less than the desktop width.</span></span>

<span data-ttu-id="9a58b-134">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9a58b-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a58b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a58b-135">Requirements</span></span>



| <span data-ttu-id="9a58b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a58b-136">Requirement</span></span> | <span data-ttu-id="9a58b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a58b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a58b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a58b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9a58b-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a58b-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9a58b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a58b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9a58b-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a58b-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9a58b-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9a58b-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a58b-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a58b-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a58b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9a58b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a58b-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a58b-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a58b-146">IID</span><span class="sxs-lookup"><span data-stu-id="9a58b-146">IID</span></span><br/>                      | <span data-ttu-id="9a58b-147">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="9a58b-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9a58b-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a58b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a58b-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="9a58b-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="9a58b-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="9a58b-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="9a58b-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="9a58b-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="9a58b-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="9a58b-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="9a58b-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9a58b-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9a58b-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9a58b-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9a58b-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9a58b-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9a58b-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9a58b-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9a58b-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9a58b-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9a58b-158">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="9a58b-158">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="9a58b-159">**VerticalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="9a58b-159">**VerticalScrollBarVisible**</span></span>](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





