---
title: IMsRdpClientAdvancedSettings propriété DisplayConnectionBar
description: Spécifie s’il faut utiliser la barre de connexion. La valeur par défaut est \_ true, ce qui active la propriété.
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété DisplayConnectionBar
- Services Bureau à distance de la propriété DisplayConnectionBar, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété DisplayConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513770"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a><span data-ttu-id="6e361-121">IMsRdpClientAdvancedSettings ::D propriété isplayConnectionBar</span><span class="sxs-lookup"><span data-stu-id="6e361-121">IMsRdpClientAdvancedSettings::DisplayConnectionBar property</span></span>

<span data-ttu-id="6e361-122">Spécifie s’il faut utiliser la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="6e361-122">Specifies whether to use the connection bar.</span></span> <span data-ttu-id="6e361-123">La valeur par défaut **est \_ true**, ce qui active la propriété.</span><span class="sxs-lookup"><span data-stu-id="6e361-123">The default value is **VARIANT\_TRUE**, which enables the property.</span></span> <span data-ttu-id="6e361-124">L’affectation de la **\_ valeur false** à cette propriété dans un environnement de script sécurisé renvoie l' **\_ erreur E Fail**.</span><span class="sxs-lookup"><span data-stu-id="6e361-124">Setting this property to **VARIANT\_FALSE** in a safe scripting environment returns **E\_FAIL**.</span></span>

<span data-ttu-id="6e361-125">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6e361-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e361-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e361-126">Syntax</span></span>


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="6e361-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6e361-127">Property value</span></span>

<span data-ttu-id="6e361-128">Affectez à ce paramètre la valeur **Variant \_ false** pour désactiver la fonctionnalité ou la **variante \_ true** pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6e361-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="6e361-129">La valeur par défaut **est \_ true**.</span><span class="sxs-lookup"><span data-stu-id="6e361-129">The default value is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e361-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6e361-130">Error codes</span></span>

<span data-ttu-id="6e361-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="6e361-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e361-132">Notes</span><span class="sxs-lookup"><span data-stu-id="6e361-132">Remarks</span></span>

<span data-ttu-id="6e361-133">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6e361-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e361-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e361-134">Requirements</span></span>



| <span data-ttu-id="6e361-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e361-135">Requirement</span></span> | <span data-ttu-id="6e361-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e361-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e361-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e361-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6e361-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e361-138">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6e361-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e361-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6e361-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e361-140">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6e361-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6e361-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e361-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e361-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6e361-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6e361-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e361-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e361-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6e361-145">IID</span><span class="sxs-lookup"><span data-stu-id="6e361-145">IID</span></span><br/>                      | <span data-ttu-id="6e361-146">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6e361-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e361-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e361-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e361-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6e361-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6e361-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6e361-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6e361-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6e361-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6e361-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6e361-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6e361-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6e361-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6e361-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6e361-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6e361-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6e361-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6e361-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6e361-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





