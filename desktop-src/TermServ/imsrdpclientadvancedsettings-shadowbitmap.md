---
title: IMsRdpClientAdvancedSettings propriété ShadowBitmap
description: Spécifie si les bitmaps secondaires doivent être utilisés.
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ShadowBitmap
- Services Bureau à distance de la propriété ShadowBitmap, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ShadowBitmap
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6c43862b498fe5828d2746666c5e414de4c71e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464318"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a><span data-ttu-id="dd51f-120">IMsRdpClientAdvancedSettings :: ShadowBitmap, propriété</span><span class="sxs-lookup"><span data-stu-id="dd51f-120">IMsRdpClientAdvancedSettings::ShadowBitmap property</span></span>

<span data-ttu-id="dd51f-121">\[Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dd51f-121">\[This property is not supported.</span></span> <span data-ttu-id="dd51f-122">À compter de Windows Server 2008 et Windows 7, les appels à **ShadowBitmap** retournent toujours **S \_ false**.\]</span><span class="sxs-lookup"><span data-stu-id="dd51f-122">Starting with Windows Server 2008 and Windows 7, calls to **ShadowBitmap** always return **S\_FALSE**.\]</span></span>

<span data-ttu-id="dd51f-123">Spécifie si les bitmaps secondaires doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="dd51f-123">Specifies if shadow bitmaps should be used.</span></span>

<span data-ttu-id="dd51f-124">Les bitmaps fantômes sont toujours désactivées en mode plein écran. par conséquent, cette propriété n’a aucun effet en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="dd51f-124">Shadow bitmaps are always disabled in full-screen mode, therefore this property has no effect when in full-screen mode.</span></span>

<span data-ttu-id="dd51f-125">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dd51f-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd51f-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd51f-126">Syntax</span></span>


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="dd51f-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dd51f-127">Property value</span></span>

<span data-ttu-id="dd51f-128">Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="dd51f-128">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="dd51f-129">La désactivation de cette fonctionnalité améliore généralement les performances, mais peut entraîner des artefacts lors de la peinture des écrans.</span><span class="sxs-lookup"><span data-stu-id="dd51f-129">Disabling this feature typically improves performance but can result in artifacts when painting screens.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd51f-130">Notes</span><span class="sxs-lookup"><span data-stu-id="dd51f-130">Remarks</span></span>

<span data-ttu-id="dd51f-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="dd51f-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd51f-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd51f-132">Requirements</span></span>



| <span data-ttu-id="dd51f-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd51f-133">Requirement</span></span> | <span data-ttu-id="dd51f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd51f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd51f-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd51f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dd51f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd51f-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="dd51f-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd51f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dd51f-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd51f-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="dd51f-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dd51f-139">End of client support</span></span><br/>    | <span data-ttu-id="dd51f-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd51f-140">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="dd51f-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="dd51f-141">End of server support</span></span><br/>    | <span data-ttu-id="dd51f-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd51f-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="dd51f-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dd51f-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd51f-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd51f-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="dd51f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dd51f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd51f-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd51f-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="dd51f-147">IID</span><span class="sxs-lookup"><span data-stu-id="dd51f-147">IID</span></span><br/>                      | <span data-ttu-id="dd51f-148">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="dd51f-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd51f-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd51f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd51f-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="dd51f-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="dd51f-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="dd51f-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="dd51f-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="dd51f-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="dd51f-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="dd51f-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="dd51f-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="dd51f-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="dd51f-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="dd51f-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="dd51f-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="dd51f-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="dd51f-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="dd51f-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





