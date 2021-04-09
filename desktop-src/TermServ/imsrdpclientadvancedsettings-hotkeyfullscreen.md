---
title: IMsRdpClientAdvancedSettings propriété HotKeyFullScreen
description: Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement du raccourci clavier pour passer en mode plein écran.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyFullScreen
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941753"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a><span data-ttu-id="4e291-120">IMsRdpClientAdvancedSettings :: HotKeyFullScreen, propriété</span><span class="sxs-lookup"><span data-stu-id="4e291-120">IMsRdpClientAdvancedSettings::HotKeyFullScreen property</span></span>

<span data-ttu-id="4e291-121">Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement du raccourci clavier pour passer en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="4e291-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for switching to full-screen mode.</span></span>

<span data-ttu-id="4e291-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4e291-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e291-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e291-123">Syntax</span></span>


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="4e291-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4e291-124">Property value</span></span>

<span data-ttu-id="4e291-125">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4e291-125">The new virtual-key code.</span></span> <span data-ttu-id="4e291-126">**VK \_ CANCEL** est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e291-126">**VK\_CANCEL** is the default value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e291-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4e291-127">Error codes</span></span>

<span data-ttu-id="4e291-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="4e291-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e291-129">Notes</span><span class="sxs-lookup"><span data-stu-id="4e291-129">Remarks</span></span>

<span data-ttu-id="4e291-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4e291-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e291-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e291-131">Requirements</span></span>



| <span data-ttu-id="4e291-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e291-132">Requirement</span></span> | <span data-ttu-id="4e291-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e291-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e291-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e291-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4e291-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e291-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4e291-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e291-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4e291-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e291-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4e291-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4e291-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e291-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e291-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4e291-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4e291-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e291-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e291-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4e291-142">IID</span><span class="sxs-lookup"><span data-stu-id="4e291-142">IID</span></span><br/>                      | <span data-ttu-id="4e291-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4e291-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e291-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e291-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e291-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4e291-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4e291-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4e291-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4e291-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4e291-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4e291-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4e291-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4e291-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4e291-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4e291-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4e291-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4e291-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4e291-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4e291-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4e291-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





