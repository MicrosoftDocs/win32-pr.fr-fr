---
title: IMsRdpClientAdvancedSettings propriété minInputSendInterval
description: Spécifie l’intervalle minimal, en millisecondes, entre l’envoi d’événements de souris.
ms.assetid: d186c05f-0b45-47bd-8a8e-e1f9baf2bd75
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété minInputSendInterval
- Services Bureau à distance de la propriété minInputSendInterval, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété minInputSendInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.minInputSendInterval
- IMsRdpClientAdvancedSettings.get_minInputSendInterval
- IMsRdpClientAdvancedSettings.put_minInputSendInterval
- IMsRdpClientAdvancedSettings2.minInputSendInterval
- IMsRdpClientAdvancedSettings2.get_minInputSendInterval
- IMsRdpClientAdvancedSettings2.put_minInputSendInterval
- IMsRdpClientAdvancedSettings3.minInputSendInterval
- IMsRdpClientAdvancedSettings3.get_minInputSendInterval
- IMsRdpClientAdvancedSettings3.put_minInputSendInterval
- IMsRdpClientAdvancedSettings4.minInputSendInterval
- IMsRdpClientAdvancedSettings4.get_minInputSendInterval
- IMsRdpClientAdvancedSettings4.put_minInputSendInterval
- IMsRdpClientAdvancedSettings5.minInputSendInterval
- IMsRdpClientAdvancedSettings5.get_minInputSendInterval
- IMsRdpClientAdvancedSettings5.put_minInputSendInterval
- IMsRdpClientAdvancedSettings6.minInputSendInterval
- IMsRdpClientAdvancedSettings6.get_minInputSendInterval
- IMsRdpClientAdvancedSettings6.put_minInputSendInterval
- IMsRdpClientAdvancedSettings7.minInputSendInterval
- IMsRdpClientAdvancedSettings7.get_minInputSendInterval
- IMsRdpClientAdvancedSettings7.put_minInputSendInterval
- IMsRdpClientAdvancedSettings8.minInputSendInterval
- IMsRdpClientAdvancedSettings8.get_minInputSendInterval
- IMsRdpClientAdvancedSettings8.put_minInputSendInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56070e2ba395c4b89dc9caa9e6e5181bb03d81ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384307"
---
# <a name="imsrdpclientadvancedsettingsmininputsendinterval-property"></a><span data-ttu-id="2e403-120">IMsRdpClientAdvancedSettings :: minInputSendInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="2e403-120">IMsRdpClientAdvancedSettings::minInputSendInterval property</span></span>

<span data-ttu-id="2e403-121">Spécifie l’intervalle minimal, en millisecondes, entre l’envoi d’événements de souris.</span><span class="sxs-lookup"><span data-stu-id="2e403-121">Specifies the minimum interval, in milliseconds, between the sending of mouse events.</span></span>

<span data-ttu-id="2e403-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2e403-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e403-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e403-123">Syntax</span></span>


```C++
HRESULT put_minInputSendInterval(
  [in]  LONG minInputSendInterval
);

HRESULT get_minInputSendInterval(
  [out] LONG *pminInputSendInterval
);
```



## <a name="property-value"></a><span data-ttu-id="2e403-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2e403-124">Property value</span></span>

<span data-ttu-id="2e403-125">Nouvel intervalle, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2e403-125">The new interval, in milliseconds.</span></span> <span data-ttu-id="2e403-126">La valeur par défaut est 100.</span><span class="sxs-lookup"><span data-stu-id="2e403-126">The default value is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e403-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2e403-127">Error codes</span></span>

<span data-ttu-id="2e403-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="2e403-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e403-129">Notes</span><span class="sxs-lookup"><span data-stu-id="2e403-129">Remarks</span></span>

<span data-ttu-id="2e403-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2e403-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e403-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e403-131">Requirements</span></span>



| <span data-ttu-id="2e403-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e403-132">Requirement</span></span> | <span data-ttu-id="2e403-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e403-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e403-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e403-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2e403-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2e403-135">Windows 7</span></span><br/>                                                                            |
| <span data-ttu-id="2e403-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e403-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2e403-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e403-137">Windows Server 2008 R2</span></span><br/>                                                               |
| <span data-ttu-id="2e403-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2e403-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e403-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e403-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2e403-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2e403-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e403-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e403-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2e403-142">IID</span><span class="sxs-lookup"><span data-stu-id="2e403-142">IID</span></span><br/>                      | <span data-ttu-id="2e403-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="2e403-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e403-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e403-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e403-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2e403-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2e403-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2e403-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2e403-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2e403-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2e403-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2e403-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2e403-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2e403-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2e403-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2e403-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2e403-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2e403-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2e403-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2e403-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





