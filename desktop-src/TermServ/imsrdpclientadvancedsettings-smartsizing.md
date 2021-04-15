---
title: IMsRdpClientAdvancedSettings propriété SmartSizing
description: Spécifie si l’affichage doit être mis à l’échelle pour s’ajuster à la zone cliente du contrôle. Notez que les barres de défilement ne s’affichent pas lorsque la propriété SmartSizing est activée.
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété SmartSizing
- Services Bureau à distance de la propriété SmartSizing, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété SmartSizing
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec2a825725e01d876b9e8658f215de6595f32f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383891"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a><span data-ttu-id="c6dda-121">IMsRdpClientAdvancedSettings :: SmartSizing, propriété</span><span class="sxs-lookup"><span data-stu-id="c6dda-121">IMsRdpClientAdvancedSettings::SmartSizing property</span></span>

<span data-ttu-id="c6dda-122">Spécifie si l’affichage doit être mis à l’échelle pour s’ajuster à la zone cliente du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6dda-122">Specifies if the display should be scaled to fit the client area of the control.</span></span> <span data-ttu-id="c6dda-123">Notez que les barres de défilement ne s’affichent pas lorsque la propriété **SmartSizing** est activée.</span><span class="sxs-lookup"><span data-stu-id="c6dda-123">Note that scroll bars do not appear when the **SmartSizing** property is enabled.</span></span>

<span data-ttu-id="c6dda-124">Contrairement à la plupart des autres propriétés, cette propriété peut être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="c6dda-124">Unlike most other properties, this property can be set when the control is connected.</span></span>

<span data-ttu-id="c6dda-125">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c6dda-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6dda-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6dda-126">Syntax</span></span>


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a><span data-ttu-id="c6dda-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c6dda-127">Property value</span></span>

<span data-ttu-id="c6dda-128">Affectez à ce paramètre la valeur **Variant \_ false** pour désactiver la fonctionnalité ou la **variante \_ true** pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c6dda-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6dda-129">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c6dda-129">Error codes</span></span>

<span data-ttu-id="c6dda-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="c6dda-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6dda-131">Notes</span><span class="sxs-lookup"><span data-stu-id="c6dda-131">Remarks</span></span>

<span data-ttu-id="c6dda-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c6dda-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6dda-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6dda-133">Requirements</span></span>



| <span data-ttu-id="c6dda-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6dda-134">Requirement</span></span> | <span data-ttu-id="c6dda-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6dda-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dda-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6dda-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c6dda-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6dda-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c6dda-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6dda-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c6dda-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6dda-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c6dda-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c6dda-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6dda-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6dda-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c6dda-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c6dda-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6dda-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6dda-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c6dda-144">IID</span><span class="sxs-lookup"><span data-stu-id="c6dda-144">IID</span></span><br/>                      | <span data-ttu-id="c6dda-145">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="c6dda-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6dda-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6dda-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6dda-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c6dda-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c6dda-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c6dda-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c6dda-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c6dda-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c6dda-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c6dda-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c6dda-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c6dda-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c6dda-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c6dda-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c6dda-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c6dda-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c6dda-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c6dda-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





