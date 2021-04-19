---
title: IMsRdpClientAdvancedSettings propriété GrabFocusOnConnect
description: Spécifie si le contrôle client doit avoir le focus lors de la connexion.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété GrabFocusOnConnect
- Services Bureau à distance de la propriété GrabFocusOnConnect, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété GrabFocusOnConnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518114"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a><span data-ttu-id="2bed1-120">IMsRdpClientAdvancedSettings :: GrabFocusOnConnect, propriété</span><span class="sxs-lookup"><span data-stu-id="2bed1-120">IMsRdpClientAdvancedSettings::GrabFocusOnConnect property</span></span>

<span data-ttu-id="2bed1-121">Spécifie si le contrôle client doit avoir le focus lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="2bed1-121">Specifies if the client control should have the focus while connecting.</span></span> <span data-ttu-id="2bed1-122">Le contrôle ne tente pas de récupérer le focus d’une fenêtre s’exécutant dans un processus différent.</span><span class="sxs-lookup"><span data-stu-id="2bed1-122">The control will not attempt to grab focus from a window running in a different process.</span></span>

<span data-ttu-id="2bed1-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2bed1-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bed1-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bed1-124">Syntax</span></span>


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a><span data-ttu-id="2bed1-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2bed1-125">Property value</span></span>

<span data-ttu-id="2bed1-126">Affectez à ce paramètre la valeur **Variant \_ false** pour désactiver la fonctionnalité ou la **variante \_ true** pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2bed1-126">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="2bed1-127">L’affectation de la **\_ valeur false** à cette propriété empêche le contrôle de prendre le focus lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="2bed1-127">Setting this property to **VARIANT\_FALSE** prevents the control from grabbing focus when connecting.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2bed1-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2bed1-128">Error codes</span></span>

<span data-ttu-id="2bed1-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="2bed1-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bed1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="2bed1-130">Remarks</span></span>

<span data-ttu-id="2bed1-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2bed1-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bed1-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bed1-132">Requirements</span></span>



| <span data-ttu-id="2bed1-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bed1-133">Requirement</span></span> | <span data-ttu-id="2bed1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bed1-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bed1-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bed1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2bed1-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bed1-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="2bed1-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bed1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2bed1-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bed1-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="2bed1-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2bed1-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="2bed1-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bed1-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2bed1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2bed1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bed1-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bed1-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2bed1-143">IID</span><span class="sxs-lookup"><span data-stu-id="2bed1-143">IID</span></span><br/>                      | <span data-ttu-id="2bed1-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="2bed1-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bed1-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bed1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bed1-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2bed1-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2bed1-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2bed1-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2bed1-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2bed1-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2bed1-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2bed1-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2bed1-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2bed1-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2bed1-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2bed1-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2bed1-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2bed1-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2bed1-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2bed1-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





