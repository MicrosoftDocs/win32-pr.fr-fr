---
title: IMsRdpClientAdvancedSettings propriété HotKeyAltShiftTab
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement des raccourcis clavier pour ALT + MAJ + TAB.
ms.assetid: da52f2fb-15cc-4d55-b26e-cf5465290889
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyAltShiftTab
- Services Bureau à distance de la propriété HotKeyAltShiftTab, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyAltShiftTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltShiftTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9819ddcba3f9cb10450525467eb8accce958c2f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511353"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltshifttab-property"></a><span data-ttu-id="425cc-120">IMsRdpClientAdvancedSettings :: HotKeyAltShiftTab, propriété</span><span class="sxs-lookup"><span data-stu-id="425cc-120">IMsRdpClientAdvancedSettings::HotKeyAltShiftTab property</span></span>

<span data-ttu-id="425cc-121">Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement des raccourcis clavier pour ALT + MAJ + TAB.</span><span class="sxs-lookup"><span data-stu-id="425cc-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SHIFT+TAB.</span></span>

<span data-ttu-id="425cc-122">Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="425cc-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="425cc-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="425cc-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="425cc-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="425cc-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltShiftTab(
  [in]  LONG hotKeyAltShiftTab
);

HRESULT get_HotKeyAltShiftTab(
  [out] LONG *photKeyAltShiftTab
);
```



## <a name="property-value"></a><span data-ttu-id="425cc-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="425cc-125">Property value</span></span>

<span data-ttu-id="425cc-126">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="425cc-126">The new virtual-key code.</span></span> <span data-ttu-id="425cc-127">**VK \_** La valeur par défaut est Next, avec Alt + Pg. suiv comme séquence résultante.</span><span class="sxs-lookup"><span data-stu-id="425cc-127">**VK\_NEXT** is the default value, with ALT+PAGE DOWN as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="425cc-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="425cc-128">Error codes</span></span>

<span data-ttu-id="425cc-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="425cc-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="425cc-130">Notes</span><span class="sxs-lookup"><span data-stu-id="425cc-130">Remarks</span></span>

<span data-ttu-id="425cc-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="425cc-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="425cc-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="425cc-132">Requirements</span></span>



| <span data-ttu-id="425cc-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="425cc-133">Requirement</span></span> | <span data-ttu-id="425cc-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="425cc-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="425cc-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="425cc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="425cc-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="425cc-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="425cc-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="425cc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="425cc-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="425cc-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="425cc-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="425cc-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="425cc-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="425cc-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="425cc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="425cc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="425cc-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="425cc-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="425cc-143">IID</span><span class="sxs-lookup"><span data-stu-id="425cc-143">IID</span></span><br/>                      | <span data-ttu-id="425cc-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="425cc-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="425cc-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="425cc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425cc-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="425cc-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="425cc-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="425cc-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="425cc-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="425cc-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="425cc-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="425cc-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="425cc-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="425cc-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="425cc-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="425cc-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="425cc-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="425cc-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="425cc-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="425cc-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





