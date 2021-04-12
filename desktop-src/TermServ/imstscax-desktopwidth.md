---
title: IMsTscAx propriété DesktopWidth
description: Spécifie la largeur, en pixels, du contrôle actif sur le Bureau à distance initial.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété DesktopWidth
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508554"
---
# <a name="imstscaxdesktopwidth-property"></a><span data-ttu-id="30cee-124">IMsTscAx ::D propriété esktopWidth</span><span class="sxs-lookup"><span data-stu-id="30cee-124">IMsTscAx::DesktopWidth property</span></span>

<span data-ttu-id="30cee-125">Spécifie la largeur, en pixels, du contrôle actif sur le Bureau à distance initial.</span><span class="sxs-lookup"><span data-stu-id="30cee-125">Specifies the current control's width, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="30cee-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="30cee-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cee-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30cee-127">Syntax</span></span>


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="30cee-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="30cee-128">Property value</span></span>

<span data-ttu-id="30cee-129">Nouvelle largeur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="30cee-129">The new width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30cee-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="30cee-130">Error codes</span></span>

<span data-ttu-id="30cee-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="30cee-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="30cee-132">Notes</span><span class="sxs-lookup"><span data-stu-id="30cee-132">Remarks</span></span>

<span data-ttu-id="30cee-133">La définition de la propriété **DesktopWidth** est facultative, mais elle doit être définie avant d’appeler la méthode [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="30cee-133">Setting the **DesktopWidth** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="30cee-134">Si la largeur du Bureau n’est pas spécifiée ou si elle est définie sur zéro, la largeur du Bureau est définie sur la largeur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30cee-134">If a desktop width is not specified, or is set to zero, the desktop width is set to the width of the control.</span></span> <span data-ttu-id="30cee-135">Les valeurs minimales et maximales dépendent de la version du système d’exploitation du client Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="30cee-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="30cee-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30cee-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="30cee-137">200 minimum, 8192 maximum</span><span class="sxs-lookup"><span data-stu-id="30cee-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="30cee-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30cee-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="30cee-139">200 minimum, 2048 maximum</span><span class="sxs-lookup"><span data-stu-id="30cee-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="30cee-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30cee-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="30cee-141">200 minimum, 1200 maximum</span><span class="sxs-lookup"><span data-stu-id="30cee-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="30cee-142">Après l’établissement d’une connexion, toute modification apportée à la largeur du contrôle ne modifie pas la largeur du Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="30cee-142">After a connection is established, any changes to the control's width do not change the width of the remote desktop.</span></span> <span data-ttu-id="30cee-143">Au lieu de cela, le contrôle affiche des barres de défilement ou centre le Bureau à distance, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="30cee-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="30cee-144">Pour modifier la taille du Bureau d’une connexion active, utilisez la méthode [**IMsRdpClient8 :: reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="30cee-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="30cee-145">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30cee-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30cee-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30cee-146">Requirements</span></span>



| <span data-ttu-id="30cee-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30cee-147">Requirement</span></span> | <span data-ttu-id="30cee-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="30cee-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30cee-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30cee-149">Minimum supported client</span></span><br/> | <span data-ttu-id="30cee-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30cee-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="30cee-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30cee-151">Minimum supported server</span></span><br/> | <span data-ttu-id="30cee-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30cee-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="30cee-153">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="30cee-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="30cee-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30cee-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30cee-155">DLL</span><span class="sxs-lookup"><span data-stu-id="30cee-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30cee-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30cee-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30cee-157">IID</span><span class="sxs-lookup"><span data-stu-id="30cee-157">IID</span></span><br/>                      | <span data-ttu-id="30cee-158">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="30cee-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="30cee-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30cee-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30cee-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="30cee-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="30cee-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="30cee-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="30cee-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="30cee-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="30cee-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="30cee-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="30cee-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="30cee-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="30cee-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="30cee-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="30cee-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="30cee-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="30cee-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="30cee-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="30cee-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="30cee-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="30cee-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="30cee-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





