---
title: IMsRdpClientAdvancedSettings propriété RedirectDrives
description: Spécifie si la redirection des lecteurs de disque est autorisée.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectDrives
- Services Bureau à distance de la propriété RedirectDrives, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectDrives
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743653"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a><span data-ttu-id="a73c7-120">IMsRdpClientAdvancedSettings :: RedirectDrives, propriété</span><span class="sxs-lookup"><span data-stu-id="a73c7-120">IMsRdpClientAdvancedSettings::RedirectDrives property</span></span>

<span data-ttu-id="a73c7-121">Spécifie si la redirection des lecteurs de disque est autorisée.</span><span class="sxs-lookup"><span data-stu-id="a73c7-121">Specifies if redirection of disk drives is allowed.</span></span>

<span data-ttu-id="a73c7-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a73c7-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73c7-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a73c7-123">Syntax</span></span>


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a><span data-ttu-id="a73c7-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a73c7-124">Property value</span></span>

<span data-ttu-id="a73c7-125">Affectez à ce paramètre la valeur **Variant \_ true** pour autoriser la redirection ou la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a73c7-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="a73c7-126">**Variante \_ TRUE** demande à l’utilisateur de confirmer l’autorisation de la redirection au moment de la connexion, pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a73c7-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a73c7-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a73c7-127">Error codes</span></span>

<span data-ttu-id="a73c7-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a73c7-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a73c7-129">Notes</span><span class="sxs-lookup"><span data-stu-id="a73c7-129">Remarks</span></span>

<span data-ttu-id="a73c7-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a73c7-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a73c7-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a73c7-131">Requirements</span></span>



| <span data-ttu-id="a73c7-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a73c7-132">Requirement</span></span> | <span data-ttu-id="a73c7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a73c7-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73c7-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73c7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a73c7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a73c7-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a73c7-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73c7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a73c7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a73c7-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a73c7-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a73c7-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="a73c7-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a73c7-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a73c7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a73c7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a73c7-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a73c7-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a73c7-142">IID</span><span class="sxs-lookup"><span data-stu-id="a73c7-142">IID</span></span><br/>                      | <span data-ttu-id="a73c7-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a73c7-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a73c7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a73c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73c7-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a73c7-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a73c7-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a73c7-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a73c7-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a73c7-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a73c7-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a73c7-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a73c7-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a73c7-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a73c7-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a73c7-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a73c7-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a73c7-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a73c7-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a73c7-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





