---
title: IMsRdpClient3 propriété AdvancedSettings4
description: Récupère un pointeur vers l’interface IMsRdpClientAdvancedSettings3.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings4
- Services Bureau à distance de la propriété AdvancedSettings4, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843221"
---
# <a name="imsrdpclient3advancedsettings4-property"></a><span data-ttu-id="f965c-120">IMsRdpClient3 :: AdvancedSettings4, propriété</span><span class="sxs-lookup"><span data-stu-id="f965c-120">IMsRdpClient3::AdvancedSettings4 property</span></span>

<span data-ttu-id="f965c-121">Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="f965c-121">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span>

<span data-ttu-id="f965c-122">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f965c-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f965c-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f965c-123">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="f965c-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f965c-124">Property value</span></span>

<span data-ttu-id="f965c-125">Pointeur vers l’interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="f965c-125">Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="f965c-126">L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.</span><span class="sxs-lookup"><span data-stu-id="f965c-126">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f965c-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f965c-127">Error codes</span></span>

<span data-ttu-id="f965c-128">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="f965c-128">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="f965c-129">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="f965c-129">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f965c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="f965c-130">Remarks</span></span>

<span data-ttu-id="f965c-131">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="f965c-131">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="f965c-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f965c-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f965c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f965c-133">Requirements</span></span>



| <span data-ttu-id="f965c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f965c-134">Requirement</span></span> | <span data-ttu-id="f965c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f965c-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f965c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f965c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f965c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f965c-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f965c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f965c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f965c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f965c-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f965c-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f965c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f965c-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f965c-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f965c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f965c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f965c-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f965c-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f965c-144">IID</span><span class="sxs-lookup"><span data-stu-id="f965c-144">IID</span></span><br/>                      | <span data-ttu-id="f965c-145">IID \_ IMsRdpClient3 est défini en tant que 91b7cbc5-a72e-4FA0-9300-d647d7e897ff</span><span class="sxs-lookup"><span data-stu-id="f965c-145">IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f965c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f965c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f965c-147">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f965c-147">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f965c-148">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f965c-148">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f965c-149">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f965c-149">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f965c-150">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f965c-150">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f965c-151">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f965c-151">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f965c-152">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f965c-152">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f965c-153">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f965c-153">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f965c-154">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f965c-154">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





