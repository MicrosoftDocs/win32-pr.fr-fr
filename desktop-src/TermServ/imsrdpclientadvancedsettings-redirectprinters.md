---
title: IMsRdpClientAdvancedSettings propriété RedirectPrinters
description: Spécifie si la redirection des imprimantes est autorisée.
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectPrinters
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fecc3b6f72b8706168c75d220d78fc49340752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740021"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a><span data-ttu-id="9a654-120">IMsRdpClientAdvancedSettings :: RedirectPrinters, propriété</span><span class="sxs-lookup"><span data-stu-id="9a654-120">IMsRdpClientAdvancedSettings::RedirectPrinters property</span></span>

<span data-ttu-id="9a654-121">Spécifie si la redirection des imprimantes est autorisée.</span><span class="sxs-lookup"><span data-stu-id="9a654-121">Specifies if redirection of printers is allowed.</span></span>

<span data-ttu-id="9a654-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9a654-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a654-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a654-123">Syntax</span></span>


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a><span data-ttu-id="9a654-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a654-124">Property value</span></span>

<span data-ttu-id="9a654-125">Affectez à ce paramètre la valeur **Variant \_ true** pour autoriser la redirection ou la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9a654-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a654-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9a654-126">Error codes</span></span>

<span data-ttu-id="9a654-127">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9a654-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a654-128">Notes</span><span class="sxs-lookup"><span data-stu-id="9a654-128">Remarks</span></span>

<span data-ttu-id="9a654-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9a654-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a654-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a654-130">Requirements</span></span>



| <span data-ttu-id="9a654-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a654-131">Requirement</span></span> | <span data-ttu-id="9a654-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a654-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a654-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a654-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9a654-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a654-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9a654-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a654-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9a654-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a654-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="9a654-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9a654-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a654-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a654-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9a654-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9a654-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a654-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a654-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9a654-141">IID</span><span class="sxs-lookup"><span data-stu-id="9a654-141">IID</span></span><br/>                      | <span data-ttu-id="9a654-142">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9a654-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a654-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a654-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a654-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9a654-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9a654-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9a654-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9a654-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9a654-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9a654-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9a654-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9a654-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9a654-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9a654-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9a654-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9a654-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9a654-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9a654-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9a654-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





