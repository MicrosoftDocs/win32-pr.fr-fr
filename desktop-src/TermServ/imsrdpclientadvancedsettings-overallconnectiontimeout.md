---
title: IMsRdpClientAdvancedSettings propriété overallConnectionTimeout
description: Spécifie la durée totale, en secondes, pendant laquelle le contrôle client attend qu’une connexion se termine.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété overallConnectionTimeout
- Services Bureau à distance de la propriété overallConnectionTimeout, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété overallConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510310"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a><span data-ttu-id="8b1b5-120">IMsRdpClientAdvancedSettings :: overallConnectionTimeout, propriété</span><span class="sxs-lookup"><span data-stu-id="8b1b5-120">IMsRdpClientAdvancedSettings::overallConnectionTimeout property</span></span>

<span data-ttu-id="8b1b5-121">Spécifie la durée totale, en secondes, pendant laquelle le contrôle client attend qu’une connexion se termine.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-121">Specifies the total length of time, in seconds, that the client control waits for a connection to complete.</span></span>

<span data-ttu-id="8b1b5-122">Si la durée spécifiée est écoulée avant la fin de la connexion, le contrôle se déconnecte et appelle la méthode [**IMsTscAxEvents :: OnDisconnected**](imstscaxevents-ondisconnected.md) .</span><span class="sxs-lookup"><span data-stu-id="8b1b5-122">If the specified time elapses before connection completes, the control disconnects and calls the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) method.</span></span>

<span data-ttu-id="8b1b5-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b1b5-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b1b5-124">Syntax</span></span>


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="8b1b5-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8b1b5-125">Property value</span></span>

<span data-ttu-id="8b1b5-126">Nouvelle durée, en secondes.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-126">The new time, in seconds.</span></span> <span data-ttu-id="8b1b5-127">La valeur maximale est 600, qui représente 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-127">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b1b5-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8b1b5-128">Error codes</span></span>

<span data-ttu-id="8b1b5-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b1b5-130">Notes</span><span class="sxs-lookup"><span data-stu-id="8b1b5-130">Remarks</span></span>

<span data-ttu-id="8b1b5-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8b1b5-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1b5-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b1b5-132">Requirements</span></span>



| <span data-ttu-id="8b1b5-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b1b5-133">Requirement</span></span> | <span data-ttu-id="8b1b5-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b1b5-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1b5-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b1b5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1b5-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b1b5-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="8b1b5-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b1b5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1b5-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b1b5-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="8b1b5-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8b1b5-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b1b5-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b1b5-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8b1b5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8b1b5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b1b5-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b1b5-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8b1b5-143">IID</span><span class="sxs-lookup"><span data-stu-id="8b1b5-143">IID</span></span><br/>                      | <span data-ttu-id="8b1b5-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="8b1b5-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b1b5-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b1b5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1b5-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8b1b5-154">**singleConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-154">**singleConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





