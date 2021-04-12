---
title: IMsRdpClient2 propriété AdvancedSettings3
description: Récupère un pointeur vers l’interface IMsRdpClientAdvancedSettings2. L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings3
- Services Bureau à distance de la propriété AdvancedSettings3, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf16d56eaff321d313e3a27eb6dd774ef67e13ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317302"
---
# <a name="imsrdpclient2advancedsettings3-property"></a><span data-ttu-id="66360-123">IMsRdpClient2 :: AdvancedSettings3, propriété</span><span class="sxs-lookup"><span data-stu-id="66360-123">IMsRdpClient2::AdvancedSettings3 property</span></span>

<span data-ttu-id="66360-124">Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="66360-124">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="66360-125">L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.</span><span class="sxs-lookup"><span data-stu-id="66360-125">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="66360-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="66360-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66360-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66360-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="66360-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="66360-128">Property value</span></span>

<span data-ttu-id="66360-129">Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="66360-129">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66360-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="66360-130">Error codes</span></span>

<span data-ttu-id="66360-131">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="66360-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="66360-132">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="66360-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="66360-133">Notes</span><span class="sxs-lookup"><span data-stu-id="66360-133">Remarks</span></span>

<span data-ttu-id="66360-134">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="66360-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66360-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66360-135">Requirements</span></span>



| <span data-ttu-id="66360-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66360-136">Requirement</span></span> | <span data-ttu-id="66360-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="66360-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66360-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66360-138">Minimum supported client</span></span><br/> | <span data-ttu-id="66360-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66360-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="66360-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66360-140">Minimum supported server</span></span><br/> | <span data-ttu-id="66360-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66360-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="66360-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="66360-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="66360-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66360-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="66360-144">DLL</span><span class="sxs-lookup"><span data-stu-id="66360-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66360-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66360-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="66360-146">IID</span><span class="sxs-lookup"><span data-stu-id="66360-146">IID</span></span><br/>                      | <span data-ttu-id="66360-147">IID \_ IMsRdpClient2 est défini en tant que e7e17dc4-3b71-4BA7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="66360-147">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="66360-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66360-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66360-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="66360-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="66360-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="66360-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="66360-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="66360-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="66360-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="66360-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="66360-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="66360-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="66360-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="66360-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="66360-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="66360-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="66360-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="66360-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="66360-157">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="66360-157">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





