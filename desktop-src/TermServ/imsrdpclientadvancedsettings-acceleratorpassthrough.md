---
title: IMsRdpClientAdvancedSettings propriété AcceleratorPassthrough
description: Spécifie si les accélérateurs de clavier doivent être transmis au serveur.
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AcceleratorPassthrough
- Services Bureau à distance de la propriété AcceleratorPassthrough, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AcceleratorPassthrough
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c252c5c0477f331b66cf65b93ed2cab844fb88e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512563"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a><span data-ttu-id="91d01-120">IMsRdpClientAdvancedSettings :: AcceleratorPassthrough, propriété</span><span class="sxs-lookup"><span data-stu-id="91d01-120">IMsRdpClientAdvancedSettings::AcceleratorPassthrough property</span></span>

<span data-ttu-id="91d01-121">Spécifie si les accélérateurs de clavier doivent être transmis au serveur.</span><span class="sxs-lookup"><span data-stu-id="91d01-121">Specifies if keyboard accelerators should be passed to the server.</span></span>

<span data-ttu-id="91d01-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="91d01-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d01-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91d01-123">Syntax</span></span>


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a><span data-ttu-id="91d01-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="91d01-124">Property value</span></span>

<span data-ttu-id="91d01-125">Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="91d01-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="91d01-126">La valeur par défaut est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="91d01-126">The default is a nonzero value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="91d01-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="91d01-127">Error codes</span></span>

<span data-ttu-id="91d01-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="91d01-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d01-129">Notes</span><span class="sxs-lookup"><span data-stu-id="91d01-129">Remarks</span></span>

<span data-ttu-id="91d01-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="91d01-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91d01-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91d01-131">Requirements</span></span>



| <span data-ttu-id="91d01-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91d01-132">Requirement</span></span> | <span data-ttu-id="91d01-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="91d01-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d01-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d01-134">Minimum supported client</span></span><br/> | <span data-ttu-id="91d01-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91d01-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="91d01-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d01-136">Minimum supported server</span></span><br/> | <span data-ttu-id="91d01-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91d01-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="91d01-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="91d01-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="91d01-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91d01-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="91d01-140">DLL</span><span class="sxs-lookup"><span data-stu-id="91d01-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91d01-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91d01-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="91d01-142">IID</span><span class="sxs-lookup"><span data-stu-id="91d01-142">IID</span></span><br/>                      | <span data-ttu-id="91d01-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="91d01-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91d01-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91d01-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d01-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="91d01-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="91d01-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="91d01-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="91d01-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="91d01-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="91d01-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="91d01-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="91d01-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="91d01-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="91d01-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="91d01-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="91d01-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="91d01-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="91d01-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="91d01-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





