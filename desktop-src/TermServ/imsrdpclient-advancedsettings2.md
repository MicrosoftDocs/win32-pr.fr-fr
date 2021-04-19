---
title: IMsRdpClient propriété AdvancedSettings2
description: Récupère un pointeur vers l’interface IMsRdpClientAdvancedSettings. L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings2
- Services Bureau à distance de la propriété AdvancedSettings2, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513826"
---
# <a name="imsrdpclientadvancedsettings2-property"></a><span data-ttu-id="ef492-125">IMsRdpClient :: AdvancedSettings2, propriété</span><span class="sxs-lookup"><span data-stu-id="ef492-125">IMsRdpClient::AdvancedSettings2 property</span></span>

<span data-ttu-id="ef492-126">Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ef492-126">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="ef492-127">L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.</span><span class="sxs-lookup"><span data-stu-id="ef492-127">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="ef492-128">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ef492-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef492-129">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef492-129">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="ef492-130">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ef492-130">Property value</span></span>

<span data-ttu-id="ef492-131">Pointeur vers l’interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ef492-131">Pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="ef492-132">L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.</span><span class="sxs-lookup"><span data-stu-id="ef492-132">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef492-133">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ef492-133">Error codes</span></span>

<span data-ttu-id="ef492-134">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="ef492-134">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ef492-135">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="ef492-135">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef492-136">Notes</span><span class="sxs-lookup"><span data-stu-id="ef492-136">Remarks</span></span>

<span data-ttu-id="ef492-137">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ef492-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef492-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef492-138">Requirements</span></span>



| <span data-ttu-id="ef492-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef492-139">Requirement</span></span> | <span data-ttu-id="ef492-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef492-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef492-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef492-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ef492-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef492-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ef492-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef492-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ef492-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef492-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ef492-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ef492-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef492-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef492-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef492-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ef492-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef492-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef492-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef492-149">IID</span><span class="sxs-lookup"><span data-stu-id="ef492-149">IID</span></span><br/>                      | <span data-ttu-id="ef492-150">IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="ef492-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ef492-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef492-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef492-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="ef492-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ef492-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ef492-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ef492-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ef492-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ef492-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ef492-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ef492-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ef492-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ef492-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ef492-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ef492-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ef492-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ef492-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ef492-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ef492-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ef492-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ef492-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ef492-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





