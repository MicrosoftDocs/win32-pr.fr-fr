---
title: IMsRdpClientAdvancedSettings propriété RedirectSmartCards
description: Spécifie si la redirection des cartes à puce est autorisée.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectSmartCards
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba58a492ede5371c0f43d996f46ed7a898df7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509504"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a><span data-ttu-id="42c68-120">IMsRdpClientAdvancedSettings :: RedirectSmartCards, propriété</span><span class="sxs-lookup"><span data-stu-id="42c68-120">IMsRdpClientAdvancedSettings::RedirectSmartCards property</span></span>

<span data-ttu-id="42c68-121">Spécifie si la redirection des cartes à puce est autorisée.</span><span class="sxs-lookup"><span data-stu-id="42c68-121">Specifies if redirection of smart cards is allowed.</span></span>

<span data-ttu-id="42c68-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="42c68-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c68-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42c68-123">Syntax</span></span>


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a><span data-ttu-id="42c68-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="42c68-124">Property value</span></span>

<span data-ttu-id="42c68-125">Affectez à ce paramètre la valeur **Variant \_ true** pour autoriser la redirection ou la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="42c68-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="42c68-126">**Variante \_ TRUE** demande à l’utilisateur de confirmer l’autorisation de la redirection au moment de la connexion, pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="42c68-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42c68-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="42c68-127">Error codes</span></span>

<span data-ttu-id="42c68-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="42c68-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="42c68-129">Notes</span><span class="sxs-lookup"><span data-stu-id="42c68-129">Remarks</span></span>

<span data-ttu-id="42c68-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="42c68-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42c68-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42c68-131">Requirements</span></span>



| <span data-ttu-id="42c68-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42c68-132">Requirement</span></span> | <span data-ttu-id="42c68-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="42c68-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42c68-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c68-134">Minimum supported client</span></span><br/> | <span data-ttu-id="42c68-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42c68-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="42c68-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c68-136">Minimum supported server</span></span><br/> | <span data-ttu-id="42c68-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42c68-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="42c68-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="42c68-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="42c68-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42c68-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="42c68-140">DLL</span><span class="sxs-lookup"><span data-stu-id="42c68-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42c68-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42c68-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="42c68-142">IID</span><span class="sxs-lookup"><span data-stu-id="42c68-142">IID</span></span><br/>                      | <span data-ttu-id="42c68-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="42c68-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42c68-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42c68-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c68-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="42c68-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="42c68-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="42c68-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="42c68-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="42c68-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="42c68-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="42c68-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="42c68-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="42c68-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="42c68-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="42c68-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="42c68-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="42c68-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="42c68-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="42c68-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





