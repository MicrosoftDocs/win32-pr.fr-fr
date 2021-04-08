---
title: IMsRdpClientAdvancedSettings propriété PinConnectionBar
description: Spécifie l’état de la barre de connexion de l’interface utilisateur.
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété PinConnectionBar
- Services Bureau à distance de la propriété PinConnectionBar, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété PinConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843113"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a><span data-ttu-id="63800-120">IMsRdpClientAdvancedSettings ::P propriété inConnectionBar</span><span class="sxs-lookup"><span data-stu-id="63800-120">IMsRdpClientAdvancedSettings::PinConnectionBar property</span></span>

<span data-ttu-id="63800-121">Spécifie l’état de la barre de connexion de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63800-121">Specifies the state of the UI connection bar.</span></span>

<span data-ttu-id="63800-122">Cette propriété renvoie **E \_ NOTIMPL** si le conteneur appelle la méthode [**IObjectSafety :: SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="63800-122">This property returns **E\_NOTIMPL** if the container calls the [**IObjectSafety::SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) method.</span></span>

<span data-ttu-id="63800-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="63800-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63800-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63800-124">Syntax</span></span>


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="63800-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="63800-125">Property value</span></span>

<span data-ttu-id="63800-126">Si vous affectez à cette propriété la **\_ valeur variant true** , l’État est défini sur « abaissé », c’est-à-dire invisible pour l’utilisateur et non disponible pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="63800-126">Setting this property to **VARIANT\_TRUE** sets the state to "lowered", that is, invisible to the user and unavailable for input.</span></span> <span data-ttu-id="63800-127">**Variante \_ FALSe** définit l’État sur « déclenché » et disponible pour l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63800-127">**VARIANT\_FALSE** sets the state to "raised" and available for user input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63800-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="63800-128">Error codes</span></span>

<span data-ttu-id="63800-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="63800-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="63800-130">Notes</span><span class="sxs-lookup"><span data-stu-id="63800-130">Remarks</span></span>

<span data-ttu-id="63800-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="63800-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63800-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63800-132">Requirements</span></span>



| <span data-ttu-id="63800-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63800-133">Requirement</span></span> | <span data-ttu-id="63800-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="63800-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63800-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63800-135">Minimum supported client</span></span><br/> | <span data-ttu-id="63800-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63800-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="63800-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63800-137">Minimum supported server</span></span><br/> | <span data-ttu-id="63800-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63800-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="63800-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="63800-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="63800-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63800-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="63800-141">DLL</span><span class="sxs-lookup"><span data-stu-id="63800-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63800-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63800-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="63800-143">IID</span><span class="sxs-lookup"><span data-stu-id="63800-143">IID</span></span><br/>                      | <span data-ttu-id="63800-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="63800-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63800-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63800-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63800-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="63800-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="63800-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="63800-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="63800-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="63800-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="63800-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="63800-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="63800-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="63800-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="63800-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="63800-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="63800-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="63800-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="63800-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="63800-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

