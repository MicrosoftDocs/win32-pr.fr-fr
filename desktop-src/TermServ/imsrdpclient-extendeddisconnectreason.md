---
title: IMsRdpClient propriété ExtendedDisconnectReason
description: Contient des informations étendues sur la raison de la déconnexion du contrôle.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété ExtendedDisconnectReason
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509282"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a><span data-ttu-id="07fc3-124">IMsRdpClient :: ExtendedDisconnectReason, propriété</span><span class="sxs-lookup"><span data-stu-id="07fc3-124">IMsRdpClient::ExtendedDisconnectReason property</span></span>

<span data-ttu-id="07fc3-125">Contient des informations étendues sur la raison de la déconnexion du contrôle.</span><span class="sxs-lookup"><span data-stu-id="07fc3-125">Contains extended information about the control's reason for disconnection.</span></span>

<span data-ttu-id="07fc3-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="07fc3-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07fc3-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07fc3-127">Syntax</span></span>


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a><span data-ttu-id="07fc3-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="07fc3-128">Property value</span></span>

<span data-ttu-id="07fc3-129">Pointeur vers la valeur [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) indiquant la raison de la déconnexion du client.</span><span class="sxs-lookup"><span data-stu-id="07fc3-129">Pointer to the [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) value indicating the reason for disconnection of the client.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07fc3-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="07fc3-130">Error codes</span></span>

<span data-ttu-id="07fc3-131">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="07fc3-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="07fc3-132">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="07fc3-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="07fc3-133">Notes</span><span class="sxs-lookup"><span data-stu-id="07fc3-133">Remarks</span></span>

<span data-ttu-id="07fc3-134">En général, cette méthode est appelée dans le gestionnaire d’événements [**IMsTscAxEvents :: OnDisconnected**](imstscaxevents-ondisconnected.md) pour récupérer des informations supplémentaires sur l’événement de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="07fc3-134">Typically this method is called in the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) event handler to retrieve additional information about the disconnection event.</span></span>

<span data-ttu-id="07fc3-135">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="07fc3-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07fc3-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07fc3-136">Requirements</span></span>



| <span data-ttu-id="07fc3-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07fc3-137">Requirement</span></span> | <span data-ttu-id="07fc3-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="07fc3-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07fc3-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07fc3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="07fc3-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07fc3-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="07fc3-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07fc3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="07fc3-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07fc3-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="07fc3-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="07fc3-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="07fc3-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07fc3-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07fc3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="07fc3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07fc3-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07fc3-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07fc3-147">IID</span><span class="sxs-lookup"><span data-stu-id="07fc3-147">IID</span></span><br/>                      | <span data-ttu-id="07fc3-148">IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="07fc3-148">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="07fc3-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07fc3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07fc3-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="07fc3-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="07fc3-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="07fc3-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="07fc3-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="07fc3-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="07fc3-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="07fc3-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="07fc3-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="07fc3-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="07fc3-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="07fc3-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="07fc3-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="07fc3-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="07fc3-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="07fc3-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="07fc3-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="07fc3-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="07fc3-159">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="07fc3-159">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="07fc3-160">**IMsTscAxEvents::OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="07fc3-160">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





