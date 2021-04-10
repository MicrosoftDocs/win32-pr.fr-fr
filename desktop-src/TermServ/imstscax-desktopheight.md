---
title: IMsTscAx propriété DesktopHeight
description: Spécifie la hauteur, en pixels, du contrôle actuel sur le Bureau à distance initial.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété DesktopHeight
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb75467b35703420ce49fd99ea032b139d721505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942413"
---
# <a name="imstscaxdesktopheight-property"></a><span data-ttu-id="0e22f-124">IMsTscAx ::D propriété esktopHeight</span><span class="sxs-lookup"><span data-stu-id="0e22f-124">IMsTscAx::DesktopHeight property</span></span>

<span data-ttu-id="0e22f-125">Spécifie la hauteur, en pixels, du contrôle actuel sur le Bureau à distance initial.</span><span class="sxs-lookup"><span data-stu-id="0e22f-125">Specifies the current control's height, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="0e22f-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0e22f-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e22f-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e22f-127">Syntax</span></span>


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="0e22f-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0e22f-128">Property value</span></span>

<span data-ttu-id="0e22f-129">Nouvelle hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="0e22f-129">The new height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e22f-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0e22f-130">Error codes</span></span>

<span data-ttu-id="0e22f-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0e22f-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e22f-132">Notes</span><span class="sxs-lookup"><span data-stu-id="0e22f-132">Remarks</span></span>

<span data-ttu-id="0e22f-133">La définition de la propriété **DesktopHeight** est facultative, mais elle doit être définie avant d’appeler la méthode [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0e22f-133">Setting the **DesktopHeight** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="0e22f-134">Si la hauteur du Bureau n’est pas spécifiée ou si a la valeur zéro, la hauteur du Bureau est définie sur la hauteur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e22f-134">If a desktop height is not specified, or is set to zero, the desktop height is set to the height of the control.</span></span> <span data-ttu-id="0e22f-135">Les valeurs minimales et maximales dépendent de la version du système d’exploitation du client Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0e22f-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="0e22f-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e22f-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="0e22f-137">200 minimum, 8192 maximum</span><span class="sxs-lookup"><span data-stu-id="0e22f-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="0e22f-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e22f-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="0e22f-139">200 minimum, 2048 maximum</span><span class="sxs-lookup"><span data-stu-id="0e22f-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="0e22f-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e22f-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="0e22f-141">200 minimum, 1200 maximum</span><span class="sxs-lookup"><span data-stu-id="0e22f-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="0e22f-142">Après l’établissement d’une connexion, toute modification apportée à la hauteur du contrôle ne modifie pas la hauteur du Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0e22f-142">After a connection is established, any changes to the control's height do not change the height of the remote desktop.</span></span> <span data-ttu-id="0e22f-143">Au lieu de cela, le contrôle affiche des barres de défilement ou centre le Bureau à distance, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="0e22f-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="0e22f-144">Pour modifier la taille du Bureau d’une connexion active, utilisez la méthode [**IMsRdpClient8 :: reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0e22f-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="0e22f-145">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0e22f-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e22f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e22f-146">Requirements</span></span>



| <span data-ttu-id="0e22f-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e22f-147">Requirement</span></span> | <span data-ttu-id="0e22f-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e22f-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e22f-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e22f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0e22f-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e22f-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0e22f-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e22f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0e22f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e22f-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0e22f-153">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0e22f-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e22f-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e22f-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e22f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0e22f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e22f-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e22f-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e22f-157">IID</span><span class="sxs-lookup"><span data-stu-id="0e22f-157">IID</span></span><br/>                      | <span data-ttu-id="0e22f-158">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0e22f-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0e22f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e22f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e22f-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0e22f-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0e22f-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0e22f-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0e22f-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0e22f-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0e22f-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0e22f-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0e22f-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0e22f-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0e22f-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0e22f-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0e22f-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0e22f-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0e22f-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0e22f-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0e22f-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0e22f-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0e22f-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0e22f-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





