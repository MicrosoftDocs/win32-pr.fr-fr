---
title: IMsRdpClient propriété SecuredSettings2
description: Récupère un pointeur vers l’interface IMsRdpClientSecuredSettings. Cette interface peut être utilisée pour définir des paramètres sécurisés pour le contrôle client.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété SecuredSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508301"
---
# <a name="imsrdpclientsecuredsettings2-property"></a><span data-ttu-id="777b5-125">IMsRdpClient :: SecuredSettings2, propriété</span><span class="sxs-lookup"><span data-stu-id="777b5-125">IMsRdpClient::SecuredSettings2 property</span></span>

<span data-ttu-id="777b5-126">Récupère un pointeur vers l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="777b5-126">Retrieves a pointer to the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span> <span data-ttu-id="777b5-127">Cette interface peut être utilisée pour définir des paramètres sécurisés pour le contrôle client.</span><span class="sxs-lookup"><span data-stu-id="777b5-127">This interface can be used to set secured settings for the client control.</span></span>

<span data-ttu-id="777b5-128">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="777b5-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="777b5-129">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="777b5-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="777b5-130">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="777b5-130">Property value</span></span>

<span data-ttu-id="777b5-131">Pointeur d’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="777b5-131">An [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="777b5-132">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="777b5-132">Error codes</span></span>

<span data-ttu-id="777b5-133">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="777b5-133">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="777b5-134">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="777b5-134">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="777b5-135">Notes</span><span class="sxs-lookup"><span data-stu-id="777b5-135">Remarks</span></span>

<span data-ttu-id="777b5-136">Pour plus d’informations, consultez l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) et [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="777b5-136">For more information, see the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="777b5-137">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="777b5-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="777b5-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="777b5-138">Requirements</span></span>



| <span data-ttu-id="777b5-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="777b5-139">Requirement</span></span> | <span data-ttu-id="777b5-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="777b5-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="777b5-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="777b5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="777b5-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="777b5-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="777b5-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="777b5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="777b5-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="777b5-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="777b5-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="777b5-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="777b5-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="777b5-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="777b5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="777b5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="777b5-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="777b5-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="777b5-149">IID</span><span class="sxs-lookup"><span data-stu-id="777b5-149">IID</span></span><br/>                      | <span data-ttu-id="777b5-150">IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="777b5-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="777b5-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="777b5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="777b5-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="777b5-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="777b5-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="777b5-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="777b5-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="777b5-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="777b5-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="777b5-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="777b5-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="777b5-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="777b5-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="777b5-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="777b5-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="777b5-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="777b5-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="777b5-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="777b5-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="777b5-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="777b5-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="777b5-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





