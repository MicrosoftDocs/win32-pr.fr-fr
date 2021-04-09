---
title: IMsRdpClientAdvancedSettings propriété RedirectPorts
description: Spécifie si la redirection des ports locaux (par exemple, COM et LPT) est autorisée.
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectPorts
- Services Bureau à distance de la propriété RedirectPorts, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectPorts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 714b26081bb4caadface283553b1dd3ebd91192d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941683"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a><span data-ttu-id="716a5-120">IMsRdpClientAdvancedSettings :: RedirectPorts, propriété</span><span class="sxs-lookup"><span data-stu-id="716a5-120">IMsRdpClientAdvancedSettings::RedirectPorts property</span></span>

<span data-ttu-id="716a5-121">Spécifie si la redirection des ports locaux (par exemple, COM et LPT) est autorisée.</span><span class="sxs-lookup"><span data-stu-id="716a5-121">Specifies if redirection of local ports (for example, COM and LPT) is allowed.</span></span>

<span data-ttu-id="716a5-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="716a5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="716a5-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="716a5-123">Syntax</span></span>


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a><span data-ttu-id="716a5-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="716a5-124">Property value</span></span>

<span data-ttu-id="716a5-125">Affectez à ce paramètre la valeur **Variant \_ true** pour autoriser la redirection ou la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="716a5-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="716a5-126">**Variante \_ TRUE** demande à l’utilisateur de confirmer l’autorisation de la redirection au moment de la connexion, pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="716a5-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="716a5-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="716a5-127">Error codes</span></span>

<span data-ttu-id="716a5-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="716a5-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="716a5-129">Notes</span><span class="sxs-lookup"><span data-stu-id="716a5-129">Remarks</span></span>

<span data-ttu-id="716a5-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="716a5-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="716a5-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="716a5-131">Requirements</span></span>



| <span data-ttu-id="716a5-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="716a5-132">Requirement</span></span> | <span data-ttu-id="716a5-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="716a5-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="716a5-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="716a5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="716a5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="716a5-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="716a5-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="716a5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="716a5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="716a5-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="716a5-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="716a5-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="716a5-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="716a5-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="716a5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="716a5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="716a5-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="716a5-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="716a5-142">IID</span><span class="sxs-lookup"><span data-stu-id="716a5-142">IID</span></span><br/>                      | <span data-ttu-id="716a5-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="716a5-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="716a5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="716a5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716a5-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="716a5-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="716a5-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="716a5-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="716a5-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="716a5-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="716a5-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="716a5-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="716a5-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="716a5-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="716a5-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="716a5-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="716a5-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="716a5-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="716a5-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="716a5-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





