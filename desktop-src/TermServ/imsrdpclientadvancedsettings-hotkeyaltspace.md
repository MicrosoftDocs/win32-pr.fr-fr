---
title: IMsRdpClientAdvancedSettings propriété HotKeyAltSpace
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour ALT + espace.
ms.assetid: 943935e9-a6f1-496e-895c-e993755e25cc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyAltSpace
- Services Bureau à distance de la propriété HotKeyAltSpace, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyAltSpace
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltSpace
- IMsRdpClientAdvancedSettings.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.put_HotKeyAltSpace
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b257bd04171f8bff22bbe91ee7310fafe89c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942049"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltspace-property"></a><span data-ttu-id="a5fce-120">IMsRdpClientAdvancedSettings :: HotKeyAltSpace, propriété</span><span class="sxs-lookup"><span data-stu-id="a5fce-120">IMsRdpClientAdvancedSettings::HotKeyAltSpace property</span></span>

<span data-ttu-id="a5fce-121">Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour ALT + espace.</span><span class="sxs-lookup"><span data-stu-id="a5fce-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SPACE.</span></span>

<span data-ttu-id="a5fce-122">Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="a5fce-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="a5fce-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a5fce-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fce-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5fce-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltSpace(
  [in]  LONG hotKeyAltSpace
);

HRESULT get_HotKeyAltSpace(
  [out] LONG *photKeyAltSpace
);
```



## <a name="property-value"></a><span data-ttu-id="a5fce-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a5fce-125">Property value</span></span>

<span data-ttu-id="a5fce-126">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5fce-126">The new virtual-key code.</span></span> <span data-ttu-id="a5fce-127">**VK \_ DELETE** est la valeur par défaut, avec Alt + Suppr comme séquence résultante.</span><span class="sxs-lookup"><span data-stu-id="a5fce-127">**VK\_DELETE** is the default, with ALT+DELETE as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5fce-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a5fce-128">Error codes</span></span>

<span data-ttu-id="a5fce-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a5fce-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5fce-130">Notes</span><span class="sxs-lookup"><span data-stu-id="a5fce-130">Remarks</span></span>

<span data-ttu-id="a5fce-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a5fce-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fce-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5fce-132">Requirements</span></span>



| <span data-ttu-id="a5fce-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5fce-133">Requirement</span></span> | <span data-ttu-id="a5fce-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5fce-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fce-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5fce-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a5fce-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5fce-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a5fce-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5fce-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a5fce-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5fce-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a5fce-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a5fce-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5fce-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5fce-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a5fce-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a5fce-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5fce-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5fce-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a5fce-143">IID</span><span class="sxs-lookup"><span data-stu-id="a5fce-143">IID</span></span><br/>                      | <span data-ttu-id="a5fce-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a5fce-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5fce-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5fce-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fce-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a5fce-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a5fce-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a5fce-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a5fce-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a5fce-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a5fce-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a5fce-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a5fce-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a5fce-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a5fce-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a5fce-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a5fce-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a5fce-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a5fce-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a5fce-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





