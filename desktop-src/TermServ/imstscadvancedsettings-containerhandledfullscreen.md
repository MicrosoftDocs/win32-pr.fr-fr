---
title: IMsTscAdvancedSettings propriété ContainerHandledFullScreen
description: Spécifie si le mode plein écran géré par le conteneur est activé.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384888"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a><span data-ttu-id="99175-122">IMsTscAdvancedSettings :: ContainerHandledFullScreen, propriété</span><span class="sxs-lookup"><span data-stu-id="99175-122">IMsTscAdvancedSettings::ContainerHandledFullScreen property</span></span>

<span data-ttu-id="99175-123">Spécifie si le mode plein écran géré par le conteneur est activé.</span><span class="sxs-lookup"><span data-stu-id="99175-123">Specifies whether the container-handled full-screen mode is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="99175-124">La valeur de la propriété **ContainerHandledFullScreen** n’a aucun effet lorsque le contrôle ActiveX Bureau à distance est sécurisé pour l’écriture de scripts, et renvoie la valeur **\_ false** en cas de tentative de modification de la valeur.</span><span class="sxs-lookup"><span data-stu-id="99175-124">The value of the **ContainerHandledFullScreen** property has no effect when the Remote Desktop ActiveX control is safe for scripting, and returns **S\_FALSE** when an attempt is made to change the value.</span></span>

 

<span data-ttu-id="99175-125">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="99175-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99175-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99175-126">Syntax</span></span>


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="99175-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="99175-127">Property value</span></span>

<span data-ttu-id="99175-128">Définissez ce paramètre sur **true** pour activer le mode ou une autre valeur pour désactiver le mode.</span><span class="sxs-lookup"><span data-stu-id="99175-128">Set this parameter to **TRUE** to enable the mode or another value to disable the mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99175-129">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="99175-129">Error codes</span></span>

<span data-ttu-id="99175-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="99175-130">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="99175-131">Retourne **S \_ false** s’il n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="99175-131">Returns **S\_FALSE** if not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="99175-132">Notes</span><span class="sxs-lookup"><span data-stu-id="99175-132">Remarks</span></span>

<span data-ttu-id="99175-133">Quand ce mode est activé, le conteneur actuel traite le commutateur dans et hors du mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="99175-133">When this mode is enabled, the current container processes the switch into and out of full-screen mode.</span></span> <span data-ttu-id="99175-134">Cette méthode doit être utilisée uniquement si le conteneur actuel a besoin d’un contrôle étendu sur le comportement du mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="99175-134">This method should be used only if the current container needs extensive control over full-screen mode behavior.</span></span> <span data-ttu-id="99175-135">Quand cette propriété est définie, le contrôle n’entre pas en mode plein écran en réponse à la combinaison de touches de raccourci du mode plein écran (CTRL + ALT + ATTN); au lieu de cela, les événements [**IMsTscAxEvents :: OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) et [**IMsTscAxEvents :: OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) sont appelés.</span><span class="sxs-lookup"><span data-stu-id="99175-135">When this property is set, the control does not enter or leave full-screen mode in response to the full-screen mode shortcut key combination (CTRL+ALT+BREAK); instead, the [**IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) and [**IMsTscAxEvents::OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) events are called.</span></span> <span data-ttu-id="99175-136">Pour plus d’informations sur ces événements, consultez [**IMsTscAxEvents**](imstscaxevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="99175-136">See [**IMsTscAxEvents**](imstscaxevents-interface.md) for more information about these events.</span></span>

<span data-ttu-id="99175-137">La plupart des applications de conteneur n’ont pas besoin d’utiliser le mode plein écran géré par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="99175-137">Most container applications will not need to use container-handled full-screen mode.</span></span>

<span data-ttu-id="99175-138">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="99175-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99175-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99175-139">Requirements</span></span>



| <span data-ttu-id="99175-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99175-140">Requirement</span></span> | <span data-ttu-id="99175-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="99175-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="99175-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99175-142">Minimum supported client</span></span><br/> | <span data-ttu-id="99175-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99175-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="99175-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99175-144">Minimum supported server</span></span><br/> | <span data-ttu-id="99175-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99175-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="99175-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="99175-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="99175-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99175-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="99175-148">DLL</span><span class="sxs-lookup"><span data-stu-id="99175-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99175-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99175-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="99175-150">IID</span><span class="sxs-lookup"><span data-stu-id="99175-150">IID</span></span><br/>                      | <span data-ttu-id="99175-151">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="99175-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99175-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99175-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99175-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="99175-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="99175-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="99175-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="99175-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="99175-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="99175-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="99175-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="99175-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="99175-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="99175-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="99175-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="99175-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="99175-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="99175-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="99175-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="99175-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="99175-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





