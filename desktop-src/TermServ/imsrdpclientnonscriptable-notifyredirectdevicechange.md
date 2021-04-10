---
title: Méthode IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: Notifie le module de redirection de périphérique du contrôle ActiveX Bureau à distance qu’une modification de périphérique s’est produite sur le système. Cette méthode passe \_ les notifications WM DEVICECHANGE au contrôle.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, méthode NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942791"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a><span data-ttu-id="cfc3e-115">IMsRdpClientNonScriptable :: NotifyRedirectDeviceChange, méthode</span><span class="sxs-lookup"><span data-stu-id="cfc3e-115">IMsRdpClientNonScriptable::NotifyRedirectDeviceChange method</span></span>

<span data-ttu-id="cfc3e-116">Notifie le module de redirection de périphérique du contrôle ActiveX Bureau à distance qu’une modification de périphérique s’est produite sur le système.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-116">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="cfc3e-117">Cette méthode passe les notifications [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) au contrôle.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-117">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc3e-118">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfc3e-118">Syntax</span></span>


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="cfc3e-119">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfc3e-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc3e-120">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cfc3e-120">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc3e-121">Spécifie l’événement d’appareil.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-121">Specifies the device event.</span></span> <span data-ttu-id="cfc3e-122">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-122">This parameter can be one of the following values.</span></span>

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span data-ttu-id="cfc3e-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT\_CONFIGCHANGECANCELED**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-124">Une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-124">A request to change the current configuration (dock or undock) has been canceled.</span></span>

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span data-ttu-id="cfc3e-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT\_CONFIGCHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-126">La configuration actuelle a été modifiée en raison d’une station d’accueil ou d’une déconnexion.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-126">The current configuration has changed due to a dock or undock.</span></span>

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span data-ttu-id="cfc3e-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT\_CUSTOMEVENT**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-128">Un événement personnalisé s’est produit.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-128">A custom event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span data-ttu-id="cfc3e-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT\_DEVICEARRIVAL**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-130">Un appareil a été inséré et est maintenant disponible.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-130">A device has been inserted and is now available.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span data-ttu-id="cfc3e-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT\_DEVICEQUERYREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-132">Une autorisation est requise pour supprimer un appareil.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-132">Permission is requested to remove a device.</span></span> <span data-ttu-id="cfc3e-133">Toute application peut refuser cette demande et annuler la suppression.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-133">Any application can deny this request and cancel the removal.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span data-ttu-id="cfc3e-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT\_DEVICEQUERYREMOVEFAILED**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-135">Une demande de suppression d’un appareil a été annulée.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-135">A request to remove a device has been canceled.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span data-ttu-id="cfc3e-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT\_DEVICEREMOVECOMPLETE**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-137">Un appareil a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-137">A device has been removed.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span data-ttu-id="cfc3e-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT\_DEVICEREMOVEPENDING**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-139">Un appareil va être supprimé.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-139">A device is about to be removed.</span></span> <span data-ttu-id="cfc3e-140">La suppression ne peut pas être refusée.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-140">The removal cannot be denied.</span></span>

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span data-ttu-id="cfc3e-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT\_DEVICETYPESPECIFIC**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-142">Un événement spécifique à l’appareil s’est produit.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-142">A device-specific event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span data-ttu-id="cfc3e-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ modifié**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT\_DEVNODES\_CHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-144">Un appareil a été ajouté ou supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-144">A device has been added to or removed from the system.</span></span>

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span data-ttu-id="cfc3e-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT\_QUERYCHANGECONFIG**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-146">Une autorisation est requise pour modifier la configuration actuelle (ancrer ou détacher).</span><span class="sxs-lookup"><span data-stu-id="cfc3e-146">Permission is requested to change the current configuration (dock or undock).</span></span>

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span data-ttu-id="cfc3e-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ USERDEFINED**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT\_USERDEFINED**</span></span>


</dt> <dd>

<span data-ttu-id="cfc3e-148">La signification de ce message est définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-148">The meaning of this message is user-defined.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cfc3e-149">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cfc3e-149">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc3e-150">Pointeur vers une structure qui contient des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-150">Pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="cfc3e-151">Son format dépend de la valeur du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cfc3e-151">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="cfc3e-152">Pour plus d’informations, reportez-vous à la documentation de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-152">For more information, refer to the documentation for each event.</span></span> <span data-ttu-id="cfc3e-153">Pour plus d’informations, consultez [types d’événements d’appareil](/windows/desktop/DevIO/device-event-types).</span><span class="sxs-lookup"><span data-stu-id="cfc3e-153">For more information, see [Device Event Types](/windows/desktop/DevIO/device-event-types).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc3e-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfc3e-154">Return value</span></span>

<span data-ttu-id="cfc3e-155">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-155">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc3e-156">Notes</span><span class="sxs-lookup"><span data-stu-id="cfc3e-156">Remarks</span></span>

<span data-ttu-id="cfc3e-157">Une application conteneur qui permet l’ajout ou la suppression dynamique d’appareils doit traiter le message [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) dans sa fenêtre de niveau supérieur et transférer le message au contrôle à l’aide de la méthode **NotifyRedirectDeviceChange** .</span><span class="sxs-lookup"><span data-stu-id="cfc3e-157">A container application that allows dynamic addition or removal of devices should process the [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) message in its top level window and forward the message to the control using the **NotifyRedirectDeviceChange** method.</span></span> <span data-ttu-id="cfc3e-158">Par exemple, un changement de périphérique dynamique se fait lorsqu’un lecteur de disque Redirigé est ajouté ou supprimé pendant que le système est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cfc3e-158">An example of a dynamic device change is when a redirected disk drive is added or removed while the system is running.</span></span>

<span data-ttu-id="cfc3e-159">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cfc3e-159">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc3e-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfc3e-160">Requirements</span></span>



| <span data-ttu-id="cfc3e-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfc3e-161">Requirement</span></span> | <span data-ttu-id="cfc3e-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfc3e-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc3e-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfc3e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc3e-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfc3e-164">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="cfc3e-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfc3e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc3e-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfc3e-166">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="cfc3e-167">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cfc3e-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="cfc3e-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc3e-168"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="cfc3e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="cfc3e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfc3e-170"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc3e-170"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="cfc3e-171">IID</span><span class="sxs-lookup"><span data-stu-id="cfc3e-171">IID</span></span><br/>                      | <span data-ttu-id="cfc3e-172">IID \_ IMsRdpClientNonScriptable est défini en tant que 2f079c4c-87B2-4AFD-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="cfc3e-172">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfc3e-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc3e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc3e-174">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-174">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="cfc3e-175">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-175">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="cfc3e-176">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-176">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="cfc3e-177">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-177">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="cfc3e-178">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="cfc3e-178">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

