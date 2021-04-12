---
title: IMsRdpClientAdvancedSettings propriété PerformanceFlags
description: Spécifie un ensemble de fonctionnalités qui peuvent être définies sur le serveur pour améliorer les performances.
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété PerformanceFlags
- Services Bureau à distance de la propriété PerformanceFlags, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété PerformanceFlags
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384300"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a><span data-ttu-id="10a28-120">IMsRdpClientAdvancedSettings ::P propriété erformanceFlags</span><span class="sxs-lookup"><span data-stu-id="10a28-120">IMsRdpClientAdvancedSettings::PerformanceFlags property</span></span>

<span data-ttu-id="10a28-121">Spécifie un ensemble de fonctionnalités qui peuvent être définies sur le serveur pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="10a28-121">Specifies a set of features that can be set at the server to improve performance.</span></span>

<span data-ttu-id="10a28-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="10a28-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a28-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10a28-123">Syntax</span></span>


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a><span data-ttu-id="10a28-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="10a28-124">Property value</span></span>

<span data-ttu-id="10a28-125">Nouveaux indicateurs.</span><span class="sxs-lookup"><span data-stu-id="10a28-125">The new flags.</span></span> <span data-ttu-id="10a28-126">La valeur par défaut est 0 (les **performances TS ne sont pas \_ \_ activées \_**).</span><span class="sxs-lookup"><span data-stu-id="10a28-126">The default is 0 (**TS\_PERF\_DISABLE\_NOTHING**.)</span></span>

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span data-ttu-id="10a28-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS \_ \_ \_ Ne pas désactiver les performances** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="10a28-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS\_PERF\_DISABLE\_NOTHING** (0x00000000)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-128">Aucune fonctionnalité n’est désactivée.</span><span class="sxs-lookup"><span data-stu-id="10a28-128">No features are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span data-ttu-id="10a28-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS \_ \_ \_ Papier peint de désactivation des performances** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="10a28-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS\_PERF\_DISABLE\_WALLPAPER** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-130">Le papier peint sur le bureau n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="10a28-130">Wallpaper on the desktop is not displayed.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span data-ttu-id="10a28-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS \_ \_ \_ FULLWINDOWDRAG désactiver les performances** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="10a28-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS\_PERF\_DISABLE\_FULLWINDOWDRAG** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-132">Le glissement de fenêtre entière est désactivé ; seul le contour de la fenêtre s’affiche lorsque la fenêtre est déplacée.</span><span class="sxs-lookup"><span data-stu-id="10a28-132">Full-window drag is disabled; only the window outline is displayed when the window is moved.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span data-ttu-id="10a28-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS \_ \_ \_ MENUANIMATIONS désactiver les performances** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="10a28-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS\_PERF\_DISABLE\_MENUANIMATIONS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-134">Les animations de menus sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="10a28-134">Menu animations are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span data-ttu-id="10a28-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS \_ \_Désactivation \_ des performances** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="10a28-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS\_PERF\_DISABLE\_THEMING** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-136">Les thèmes sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="10a28-136">Themes are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span data-ttu-id="10a28-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS \_ PERFORMANCE \_ \_ ENHANCEd Graphics** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="10a28-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS\_PERF\_ENABLE\_ENHANCED GRAPHICS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-138">Activez les graphiques améliorés.</span><span class="sxs-lookup"><span data-stu-id="10a28-138">Enable enhanced graphics.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span data-ttu-id="10a28-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS \_ \_Ombre du \_ curseur \_ de désactivation des performances** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="10a28-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS\_PERF\_DISABLE\_CURSOR\_SHADOW** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-140">Aucune ombre n’est affichée pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="10a28-140">No shadow is displayed for the cursor.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span data-ttu-id="10a28-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS \_ PERF \_ Disable \_ CURSORSETTINGS** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="10a28-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS\_PERF\_DISABLE\_CURSORSETTINGS** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-142">Le clignotement du curseur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="10a28-142">Cursor blinking is disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span data-ttu-id="10a28-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS \_ \_Lissage des \_ polices \_** pour l’activation des performances (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="10a28-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS\_PERF\_ENABLE\_FONT\_SMOOTHING** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-144">Activez le lissage des polices.</span><span class="sxs-lookup"><span data-stu-id="10a28-144">Enable font smoothing.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span data-ttu-id="10a28-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS \_ 0x00000100 (performance \_ Enable \_ Desktop \_ composition** )</span><span class="sxs-lookup"><span data-stu-id="10a28-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS\_PERF\_ENABLE\_DESKTOP\_COMPOSITION** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-146">Activez la composition du bureau.</span><span class="sxs-lookup"><span data-stu-id="10a28-146">Enable desktop composition.</span></span>

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span data-ttu-id="10a28-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS \_ \_ \_ \_ Paramètre NONPERFCLIENT par défaut des performances** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="10a28-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS\_PERF\_DEFAULT\_NONPERFCLIENT\_SETTING** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-148">Définissez en interne pour les clients ne connaissant pas ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="10a28-148">Set internally for clients not aware of this setting.</span></span>

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span data-ttu-id="10a28-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS \_ PERF \_ RESERVED1** (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="10a28-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS\_PERF\_RESERVED1** (0x80000000)</span></span>


</dt> <dd>

<span data-ttu-id="10a28-150">Réservé et utilisé en interne par le client.</span><span class="sxs-lookup"><span data-stu-id="10a28-150">Reserved and used internally by the client.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="10a28-151">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="10a28-151">Error codes</span></span>

<span data-ttu-id="10a28-152">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="10a28-152">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="10a28-153">Notes</span><span class="sxs-lookup"><span data-stu-id="10a28-153">Remarks</span></span>

<span data-ttu-id="10a28-154">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="10a28-154">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10a28-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10a28-155">Requirements</span></span>



| <span data-ttu-id="10a28-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10a28-156">Requirement</span></span> | <span data-ttu-id="10a28-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="10a28-157">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a28-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a28-158">Minimum supported client</span></span><br/> | <span data-ttu-id="10a28-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10a28-159">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="10a28-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a28-160">Minimum supported server</span></span><br/> | <span data-ttu-id="10a28-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10a28-161">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="10a28-162">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="10a28-162">Type library</span></span><br/>             | <dl> <span data-ttu-id="10a28-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10a28-163"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="10a28-164">DLL</span><span class="sxs-lookup"><span data-stu-id="10a28-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10a28-165"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10a28-165"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="10a28-166">IID</span><span class="sxs-lookup"><span data-stu-id="10a28-166">IID</span></span><br/>                      | <span data-ttu-id="10a28-167">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="10a28-167">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10a28-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10a28-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a28-169">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="10a28-169">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="10a28-170">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="10a28-170">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="10a28-171">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="10a28-171">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="10a28-172">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="10a28-172">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="10a28-173">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="10a28-173">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="10a28-174">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="10a28-174">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="10a28-175">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="10a28-175">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="10a28-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="10a28-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





