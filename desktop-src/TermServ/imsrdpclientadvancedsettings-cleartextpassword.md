---
title: IMsRdpClientAdvancedSettings propriété ClearTextPassword
description: Spécifie le mot de passe avec lequel se connecter. Pour plus d’informations, consultez l’interface IMsTscNonScriptable.
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ClearTextPassword
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465138"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a><span data-ttu-id="06806-121">IMsRdpClientAdvancedSettings :: ClearTextPassword, propriété</span><span class="sxs-lookup"><span data-stu-id="06806-121">IMsRdpClientAdvancedSettings::ClearTextPassword property</span></span>

<span data-ttu-id="06806-122">Spécifie le mot de passe avec lequel se connecter.</span><span class="sxs-lookup"><span data-stu-id="06806-122">Specifies the password with which to connect.</span></span> <span data-ttu-id="06806-123">Pour plus d’informations, consultez l’interface [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="06806-123">For more information, see the [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) interface.</span></span>

> [!Caution]  
> <span data-ttu-id="06806-124">Même si l’accès scriptable aux mots de passe en texte en clair est disponible via cette propriété, il est toujours de la responsabilité du développeur de faire preuve de prudence et de maintenir la sécurité lors du passage des mots de passe dans leurs applications.</span><span class="sxs-lookup"><span data-stu-id="06806-124">Even though scriptable access to plaintext passwords is available through this property, it is still the responsibility of the developer to exercise every caution and maintain security when passing passwords in their applications.</span></span>

 

<span data-ttu-id="06806-125">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="06806-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06806-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06806-126">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a><span data-ttu-id="06806-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="06806-127">Property value</span></span>

<span data-ttu-id="06806-128">Nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="06806-128">The new password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06806-129">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="06806-129">Error codes</span></span>

<span data-ttu-id="06806-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="06806-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="06806-131">Notes</span><span class="sxs-lookup"><span data-stu-id="06806-131">Remarks</span></span>

<span data-ttu-id="06806-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="06806-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06806-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06806-133">Requirements</span></span>



| <span data-ttu-id="06806-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06806-134">Requirement</span></span> | <span data-ttu-id="06806-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="06806-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06806-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06806-136">Minimum supported client</span></span><br/> | <span data-ttu-id="06806-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06806-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="06806-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06806-138">Minimum supported server</span></span><br/> | <span data-ttu-id="06806-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06806-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="06806-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="06806-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="06806-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06806-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="06806-142">DLL</span><span class="sxs-lookup"><span data-stu-id="06806-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06806-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06806-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="06806-144">IID</span><span class="sxs-lookup"><span data-stu-id="06806-144">IID</span></span><br/>                      | <span data-ttu-id="06806-145">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="06806-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06806-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06806-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06806-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="06806-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="06806-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="06806-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="06806-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="06806-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="06806-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="06806-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="06806-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="06806-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="06806-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="06806-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="06806-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="06806-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="06806-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="06806-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





