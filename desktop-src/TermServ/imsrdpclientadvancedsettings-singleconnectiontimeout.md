---
title: IMsRdpClientAdvancedSettings propriété singleConnectionTimeout
description: Spécifie la durée maximale, en secondes, pendant laquelle le contrôle client attend une connexion à une adresse IP.
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété singleConnectionTimeout
- Services Bureau à distance de la propriété singleConnectionTimeout, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété singleConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383892"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a><span data-ttu-id="d8259-120">IMsRdpClientAdvancedSettings :: singleConnectionTimeout, propriété</span><span class="sxs-lookup"><span data-stu-id="d8259-120">IMsRdpClientAdvancedSettings::singleConnectionTimeout property</span></span>

<span data-ttu-id="d8259-121">Spécifie la durée maximale, en secondes, pendant laquelle le contrôle client attend une connexion à une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="d8259-121">Specifies the maximum length of time, in seconds, that the client control waits for a connection to an IP address.</span></span>

<span data-ttu-id="d8259-122">Pendant la connexion, le contrôle peut tenter de se connecter à plusieurs adresses IP.</span><span class="sxs-lookup"><span data-stu-id="d8259-122">During connection, the control may attempt to connect to multiple IP addresses.</span></span>

<span data-ttu-id="d8259-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d8259-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8259-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8259-124">Syntax</span></span>


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="d8259-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d8259-125">Property value</span></span>

<span data-ttu-id="d8259-126">Nouvelle durée, en secondes.</span><span class="sxs-lookup"><span data-stu-id="d8259-126">The new time, in seconds.</span></span> <span data-ttu-id="d8259-127">La valeur maximale est 600.</span><span class="sxs-lookup"><span data-stu-id="d8259-127">The maximum value is 600.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8259-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d8259-128">Error codes</span></span>

<span data-ttu-id="d8259-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="d8259-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8259-130">Notes</span><span class="sxs-lookup"><span data-stu-id="d8259-130">Remarks</span></span>

<span data-ttu-id="d8259-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d8259-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8259-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8259-132">Requirements</span></span>



| <span data-ttu-id="d8259-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8259-133">Requirement</span></span> | <span data-ttu-id="d8259-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8259-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8259-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8259-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d8259-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8259-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d8259-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8259-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d8259-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8259-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d8259-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d8259-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8259-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8259-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d8259-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d8259-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8259-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8259-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d8259-143">IID</span><span class="sxs-lookup"><span data-stu-id="d8259-143">IID</span></span><br/>                      | <span data-ttu-id="d8259-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d8259-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8259-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8259-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8259-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d8259-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d8259-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d8259-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d8259-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d8259-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d8259-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d8259-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d8259-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d8259-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d8259-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d8259-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d8259-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d8259-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d8259-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d8259-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d8259-154">**overallConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="d8259-154">**overallConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





