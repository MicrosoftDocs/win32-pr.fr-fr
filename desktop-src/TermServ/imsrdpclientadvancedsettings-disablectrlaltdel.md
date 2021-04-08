---
title: IMsRdpClientAdvancedSettings propriété DisableCtrlAltDel
description: Spécifie si l’écran explicatif initial de Winlogon doit s’afficher.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété DisableCtrlAltDel
- Services Bureau à distance de la propriété DisableCtrlAltDel, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété DisableCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380aa78c16c7e937637cc727fe81f054649f929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740557"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a><span data-ttu-id="9e8c6-120">IMsRdpClientAdvancedSettings ::D propriété isableCtrlAltDel</span><span class="sxs-lookup"><span data-stu-id="9e8c6-120">IMsRdpClientAdvancedSettings::DisableCtrlAltDel property</span></span>

<span data-ttu-id="9e8c6-121">Spécifie si l’écran explicatif initial de Winlogon doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-121">Specifies if the initial explanatory screen in Winlogon should display.</span></span>

<span data-ttu-id="9e8c6-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8c6-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e8c6-123">Syntax</span></span>


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="9e8c6-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9e8c6-124">Property value</span></span>

<span data-ttu-id="9e8c6-125">Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9e8c6-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9e8c6-126">Error codes</span></span>

<span data-ttu-id="9e8c6-127">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e8c6-128">Notes</span><span class="sxs-lookup"><span data-stu-id="9e8c6-128">Remarks</span></span>

<span data-ttu-id="9e8c6-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9e8c6-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8c6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e8c6-130">Requirements</span></span>



| <span data-ttu-id="9e8c6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e8c6-131">Requirement</span></span> | <span data-ttu-id="9e8c6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e8c6-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8c6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e8c6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9e8c6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e8c6-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9e8c6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e8c6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9e8c6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e8c6-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="9e8c6-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9e8c6-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e8c6-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8c6-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9e8c6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8c6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e8c6-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8c6-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9e8c6-141">IID</span><span class="sxs-lookup"><span data-stu-id="9e8c6-141">IID</span></span><br/>                      | <span data-ttu-id="9e8c6-142">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9e8c6-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e8c6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e8c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8c6-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9e8c6-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9e8c6-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9e8c6-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9e8c6-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9e8c6-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9e8c6-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9e8c6-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9e8c6-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





