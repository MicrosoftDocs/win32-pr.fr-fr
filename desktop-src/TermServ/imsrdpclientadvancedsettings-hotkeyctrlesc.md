---
title: IMsRdpClientAdvancedSettings propriété HotKeyCtrlEsc
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour CTRL + ESC.
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyCtrlEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510535"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a><span data-ttu-id="948f1-120">IMsRdpClientAdvancedSettings :: HotKeyCtrlEsc, propriété</span><span class="sxs-lookup"><span data-stu-id="948f1-120">IMsRdpClientAdvancedSettings::HotKeyCtrlEsc property</span></span>

<span data-ttu-id="948f1-121">Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour CTRL + ESC.</span><span class="sxs-lookup"><span data-stu-id="948f1-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for CTRL+ESC.</span></span>

<span data-ttu-id="948f1-122">Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="948f1-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="948f1-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="948f1-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="948f1-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="948f1-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a><span data-ttu-id="948f1-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="948f1-125">Property value</span></span>

<span data-ttu-id="948f1-126">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="948f1-126">The new virtual-key code.</span></span> <span data-ttu-id="948f1-127">**VK \_ Page d’hébergement** est la valeur par défaut, avec Alt + début comme séquence résultante.</span><span class="sxs-lookup"><span data-stu-id="948f1-127">**VK\_HOME** is the default value, with ALT+HOME as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="948f1-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="948f1-128">Error codes</span></span>

<span data-ttu-id="948f1-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="948f1-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="948f1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="948f1-130">Remarks</span></span>

<span data-ttu-id="948f1-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="948f1-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="948f1-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="948f1-132">Requirements</span></span>



| <span data-ttu-id="948f1-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="948f1-133">Requirement</span></span> | <span data-ttu-id="948f1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="948f1-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="948f1-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="948f1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="948f1-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="948f1-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="948f1-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="948f1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="948f1-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="948f1-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="948f1-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="948f1-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="948f1-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="948f1-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="948f1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="948f1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="948f1-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="948f1-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="948f1-143">IID</span><span class="sxs-lookup"><span data-stu-id="948f1-143">IID</span></span><br/>                      | <span data-ttu-id="948f1-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="948f1-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="948f1-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="948f1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948f1-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="948f1-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="948f1-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="948f1-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="948f1-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="948f1-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="948f1-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="948f1-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="948f1-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="948f1-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="948f1-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="948f1-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="948f1-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="948f1-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="948f1-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="948f1-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





