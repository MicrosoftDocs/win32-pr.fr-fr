---
title: IMsRdpClientAdvancedSettings propriété MinutesToIdleTimeout
description: Spécifie la durée maximale, en minutes, pendant laquelle le client doit rester connecté sans entrée d’utilisateur. Si la durée spécifiée est écoulée, le contrôle appelle la méthode IMsTscAxEvents OnIdleTimeoutNotification.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété MinutesToIdleTimeout
- Services Bureau à distance de la propriété MinutesToIdleTimeout, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété MinutesToIdleTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511751"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a><span data-ttu-id="7dd20-121">IMsRdpClientAdvancedSettings :: MinutesToIdleTimeout, propriété</span><span class="sxs-lookup"><span data-stu-id="7dd20-121">IMsRdpClientAdvancedSettings::MinutesToIdleTimeout property</span></span>

<span data-ttu-id="7dd20-122">Spécifie la durée maximale, en minutes, pendant laquelle le client doit rester connecté sans entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7dd20-122">Specifies the maximum length of time, in minutes, that the client should remain connected without user input.</span></span> <span data-ttu-id="7dd20-123">Si la durée spécifiée est écoulée, le contrôle appelle la méthode [**IMsTscAxEvents :: OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="7dd20-123">If the specified time elapses, the control calls the [**IMsTscAxEvents::OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) method.</span></span>

<span data-ttu-id="7dd20-124">Vous pouvez utiliser cette propriété dans une situation où vous devez déconnecter une session inactive ; par exemple, dans un environnement plein écran.</span><span class="sxs-lookup"><span data-stu-id="7dd20-124">You can use this property in a situation where you need to disconnect an idle session; for example, in a kiosk environment.</span></span>

<span data-ttu-id="7dd20-125">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7dd20-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd20-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dd20-126">Syntax</span></span>


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="7dd20-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7dd20-127">Property value</span></span>

<span data-ttu-id="7dd20-128">Nouvelle durée, en minutes.</span><span class="sxs-lookup"><span data-stu-id="7dd20-128">The new time, in minutes.</span></span> <span data-ttu-id="7dd20-129">La valeur par défaut est zéro, ce qui désactive la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7dd20-129">The default value is zero, which disables the feature.</span></span> <span data-ttu-id="7dd20-130">La valeur maximale est 240, qui représente 4 heures.</span><span class="sxs-lookup"><span data-stu-id="7dd20-130">The maximum value is 240, which represents 4 hours.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7dd20-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7dd20-131">Error codes</span></span>

<span data-ttu-id="7dd20-132">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="7dd20-132">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dd20-133">Notes</span><span class="sxs-lookup"><span data-stu-id="7dd20-133">Remarks</span></span>

<span data-ttu-id="7dd20-134">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7dd20-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7dd20-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dd20-135">Requirements</span></span>



| <span data-ttu-id="7dd20-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dd20-136">Requirement</span></span> | <span data-ttu-id="7dd20-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dd20-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd20-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dd20-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd20-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7dd20-139">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="7dd20-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dd20-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd20-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7dd20-141">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="7dd20-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7dd20-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="7dd20-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd20-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7dd20-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7dd20-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dd20-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd20-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7dd20-146">IID</span><span class="sxs-lookup"><span data-stu-id="7dd20-146">IID</span></span><br/>                      | <span data-ttu-id="7dd20-147">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="7dd20-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7dd20-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dd20-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd20-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7dd20-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7dd20-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7dd20-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7dd20-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7dd20-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7dd20-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7dd20-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7dd20-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7dd20-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7dd20-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7dd20-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7dd20-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7dd20-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7dd20-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7dd20-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





