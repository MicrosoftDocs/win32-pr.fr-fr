---
title: IMsRdpClientAdvancedSettings propriété HotKeyAltEsc
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier ALT + ÉCHAP.
ms.assetid: 17cae4ca-8e97-4713-bb4e-ac9a9876c16c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyAltEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltEsc
- IMsRdpClientAdvancedSettings.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyAltEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b661a91a0204177525063629825c478b40b4c29e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467030"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltesc-property"></a><span data-ttu-id="82e70-120">IMsRdpClientAdvancedSettings :: HotKeyAltEsc, propriété</span><span class="sxs-lookup"><span data-stu-id="82e70-120">IMsRdpClientAdvancedSettings::HotKeyAltEsc property</span></span>

<span data-ttu-id="82e70-121">Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier ALT + ÉCHAP.</span><span class="sxs-lookup"><span data-stu-id="82e70-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+ESC.</span></span>

<span data-ttu-id="82e70-122">Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="82e70-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="82e70-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="82e70-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e70-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82e70-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltEsc(
  [in]  LONG hotKeyAltEsc
);

HRESULT get_HotKeyAltEsc(
  [out] LONG *photKeyAltEsc
);
```



## <a name="property-value"></a><span data-ttu-id="82e70-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="82e70-125">Property value</span></span>

<span data-ttu-id="82e70-126">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="82e70-126">The new virtual-key code.</span></span> <span data-ttu-id="82e70-127">**VK \_ INSERT** est la valeur par défaut, avec Alt + Inser comme séquence résultante.</span><span class="sxs-lookup"><span data-stu-id="82e70-127">**VK\_INSERT** is the default value, with ALT+INSERT as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="82e70-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="82e70-128">Error codes</span></span>

<span data-ttu-id="82e70-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="82e70-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="82e70-130">Notes</span><span class="sxs-lookup"><span data-stu-id="82e70-130">Remarks</span></span>

<span data-ttu-id="82e70-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="82e70-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82e70-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82e70-132">Requirements</span></span>



| <span data-ttu-id="82e70-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82e70-133">Requirement</span></span> | <span data-ttu-id="82e70-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="82e70-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e70-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82e70-135">Minimum supported client</span></span><br/> | <span data-ttu-id="82e70-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82e70-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="82e70-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82e70-137">Minimum supported server</span></span><br/> | <span data-ttu-id="82e70-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82e70-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="82e70-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="82e70-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="82e70-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82e70-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="82e70-141">DLL</span><span class="sxs-lookup"><span data-stu-id="82e70-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82e70-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82e70-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="82e70-143">IID</span><span class="sxs-lookup"><span data-stu-id="82e70-143">IID</span></span><br/>                      | <span data-ttu-id="82e70-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="82e70-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82e70-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82e70-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e70-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="82e70-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="82e70-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="82e70-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="82e70-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="82e70-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="82e70-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="82e70-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="82e70-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="82e70-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="82e70-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="82e70-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="82e70-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="82e70-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="82e70-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="82e70-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





