---
title: IMsRdpClientAdvancedSettings propriété HotKeyAltTab
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour ALT + TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyAltTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384312"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a><span data-ttu-id="11ddf-120">IMsRdpClientAdvancedSettings :: HotKeyAltTab, propriété</span><span class="sxs-lookup"><span data-stu-id="11ddf-120">IMsRdpClientAdvancedSettings::HotKeyAltTab property</span></span>

<span data-ttu-id="11ddf-121">Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="11ddf-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+TAB.</span></span>

<span data-ttu-id="11ddf-122">Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="11ddf-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="11ddf-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="11ddf-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ddf-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11ddf-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a><span data-ttu-id="11ddf-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="11ddf-125">Property value</span></span>

<span data-ttu-id="11ddf-126">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="11ddf-126">The new virtual-key code.</span></span> <span data-ttu-id="11ddf-127">**VK \_ AVANT** , il s’agit de la valeur par défaut, avec Alt + Pg. précédent comme séquence résultante.</span><span class="sxs-lookup"><span data-stu-id="11ddf-127">**VK\_PRIOR** is the default value, with ALT+PAGE UP as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11ddf-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="11ddf-128">Error codes</span></span>

<span data-ttu-id="11ddf-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="11ddf-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="11ddf-130">Notes</span><span class="sxs-lookup"><span data-stu-id="11ddf-130">Remarks</span></span>

<span data-ttu-id="11ddf-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="11ddf-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11ddf-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11ddf-132">Requirements</span></span>



| <span data-ttu-id="11ddf-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11ddf-133">Requirement</span></span> | <span data-ttu-id="11ddf-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="11ddf-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ddf-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11ddf-135">Minimum supported client</span></span><br/> | <span data-ttu-id="11ddf-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11ddf-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="11ddf-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11ddf-137">Minimum supported server</span></span><br/> | <span data-ttu-id="11ddf-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11ddf-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="11ddf-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="11ddf-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="11ddf-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11ddf-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="11ddf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="11ddf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11ddf-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11ddf-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="11ddf-143">IID</span><span class="sxs-lookup"><span data-stu-id="11ddf-143">IID</span></span><br/>                      | <span data-ttu-id="11ddf-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="11ddf-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11ddf-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11ddf-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ddf-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="11ddf-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="11ddf-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="11ddf-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="11ddf-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="11ddf-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="11ddf-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="11ddf-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="11ddf-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="11ddf-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="11ddf-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="11ddf-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="11ddf-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="11ddf-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="11ddf-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="11ddf-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





