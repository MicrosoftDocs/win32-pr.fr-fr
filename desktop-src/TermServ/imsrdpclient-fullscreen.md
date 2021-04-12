---
title: Propriété FullScreen IMsRdpClient
description: Détermine si le contrôle client est en mode plein écran.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété FullScreen
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105874"
---
# <a name="imsrdpclientfullscreen-property"></a><span data-ttu-id="5a5fa-124">IMsRdpClient :: FullScreen, propriété</span><span class="sxs-lookup"><span data-stu-id="5a5fa-124">IMsRdpClient::FullScreen property</span></span>

<span data-ttu-id="5a5fa-125">Détermine si le contrôle client est en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="5a5fa-125">Determines whether the client control is in full-screen mode.</span></span>

<span data-ttu-id="5a5fa-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5a5fa-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a5fa-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a5fa-127">Syntax</span></span>


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="5a5fa-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5a5fa-128">Property value</span></span>

<span data-ttu-id="5a5fa-129">**True** pour passer en mode plein écran, **false** pour conserver le mode plein écran et revenir en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a5fa-129">**True** to enter full-screen mode, **False** to leave full-screen mode and return to window mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a5fa-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5a5fa-130">Error codes</span></span>

<span data-ttu-id="5a5fa-131">Si les méthodes sont correctement exécutées, la méthode **S \_ OK** est retournée.</span><span class="sxs-lookup"><span data-stu-id="5a5fa-131">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="5a5fa-132">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="5a5fa-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a5fa-133">Notes</span><span class="sxs-lookup"><span data-stu-id="5a5fa-133">Remarks</span></span>

<span data-ttu-id="5a5fa-134">Vous pouvez définir cette propriété lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="5a5fa-134">You can set this property when the control is connected.</span></span>

<span data-ttu-id="5a5fa-135">Vous devez appeler la méthode [**IMsRdpClientNonScriptable3 ::p ut \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) avant d’appeler la méthode [**IMsTscSecuredSettings ::P ut \_ fullscreen**](imstscsecuredsettings-fullscreen.md) ou **IMsRdpClient ::p ut \_ fullscreen** .</span><span class="sxs-lookup"><span data-stu-id="5a5fa-135">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the **IMsRdpClient::put\_Fullscreen** method.</span></span>

<span data-ttu-id="5a5fa-136">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5a5fa-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a5fa-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a5fa-137">Requirements</span></span>



| <span data-ttu-id="5a5fa-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a5fa-138">Requirement</span></span> | <span data-ttu-id="5a5fa-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a5fa-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a5fa-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a5fa-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5a5fa-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a5fa-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5a5fa-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a5fa-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5a5fa-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a5fa-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5a5fa-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5a5fa-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a5fa-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a5fa-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a5fa-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5a5fa-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a5fa-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a5fa-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a5fa-148">IID</span><span class="sxs-lookup"><span data-stu-id="5a5fa-148">IID</span></span><br/>                      | <span data-ttu-id="5a5fa-149">IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="5a5fa-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="5a5fa-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a5fa-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a5fa-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5a5fa-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="5a5fa-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





