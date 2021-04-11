---
title: IMsTscAdvancedSettings propriété allowBackgroundInput
description: Spécifie si le mode d’entrée d’arrière-plan est activé.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété allowBackgroundInput
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385247"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a><span data-ttu-id="55c33-122">IMsTscAdvancedSettings :: allowBackgroundInput, propriété</span><span class="sxs-lookup"><span data-stu-id="55c33-122">IMsTscAdvancedSettings::allowBackgroundInput property</span></span>

<span data-ttu-id="55c33-123">Spécifie si le mode d’entrée d’arrière-plan est activé.</span><span class="sxs-lookup"><span data-stu-id="55c33-123">Specifies whether background input mode is enabled.</span></span> <span data-ttu-id="55c33-124">Lorsque l’entrée d’arrière-plan est activée, le client peut accepter l’entrée lorsque le client n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="55c33-124">When background input is enabled the client can accept input when the client does not have focus.</span></span>

<span data-ttu-id="55c33-125">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="55c33-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c33-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55c33-126">Syntax</span></span>


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a><span data-ttu-id="55c33-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="55c33-127">Property value</span></span>

<span data-ttu-id="55c33-128">Affectez à ce paramètre la valeur 0 pour désactiver le mode de saisie en arrière-plan ou une valeur différente de zéro pour activer le mode d’entrée d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="55c33-128">Set this parameter to 0 to disable background input mode or a nonzero value to enable background input mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55c33-129">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="55c33-129">Error codes</span></span>

<span data-ttu-id="55c33-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="55c33-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="55c33-131">Notes</span><span class="sxs-lookup"><span data-stu-id="55c33-131">Remarks</span></span>

<span data-ttu-id="55c33-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="55c33-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55c33-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55c33-133">Requirements</span></span>



| <span data-ttu-id="55c33-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55c33-134">Requirement</span></span> | <span data-ttu-id="55c33-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="55c33-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c33-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55c33-136">Minimum supported client</span></span><br/> | <span data-ttu-id="55c33-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55c33-137">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="55c33-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55c33-138">Minimum supported server</span></span><br/> | <span data-ttu-id="55c33-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55c33-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="55c33-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="55c33-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="55c33-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c33-141"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="55c33-142">DLL</span><span class="sxs-lookup"><span data-stu-id="55c33-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55c33-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c33-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="55c33-144">IID</span><span class="sxs-lookup"><span data-stu-id="55c33-144">IID</span></span><br/>                      | <span data-ttu-id="55c33-145">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="55c33-145">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55c33-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55c33-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c33-147">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="55c33-147">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="55c33-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="55c33-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="55c33-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="55c33-149">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="55c33-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="55c33-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="55c33-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="55c33-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="55c33-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="55c33-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="55c33-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="55c33-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="55c33-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="55c33-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="55c33-155">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="55c33-155">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





