---
title: IMsRdpClientAdvancedSettings propriété EnableWindowsKey
description: Spécifie si la clé Windows peut être utilisée dans la session à distance.
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété EnableWindowsKey
- Services Bureau à distance de la propriété EnableWindowsKey, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété EnableWindowsKey
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e31571e44d6b391250c32268750b25a76105eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743300"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a><span data-ttu-id="a54c8-120">IMsRdpClientAdvancedSettings :: EnableWindowsKey, propriété</span><span class="sxs-lookup"><span data-stu-id="a54c8-120">IMsRdpClientAdvancedSettings::EnableWindowsKey property</span></span>

<span data-ttu-id="a54c8-121">Spécifie si la clé Windows peut être utilisée dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="a54c8-121">Specifies if the Windows key can be used in the remote session.</span></span>

<span data-ttu-id="a54c8-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a54c8-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54c8-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a54c8-123">Syntax</span></span>


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
);
```



## <a name="property-value"></a><span data-ttu-id="a54c8-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a54c8-124">Property value</span></span>

<span data-ttu-id="a54c8-125">Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a54c8-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a54c8-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a54c8-126">Error codes</span></span>

<span data-ttu-id="a54c8-127">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a54c8-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a54c8-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a54c8-128">Remarks</span></span>

<span data-ttu-id="a54c8-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a54c8-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a54c8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a54c8-130">Requirements</span></span>



| <span data-ttu-id="a54c8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a54c8-131">Requirement</span></span> | <span data-ttu-id="a54c8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a54c8-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54c8-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a54c8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a54c8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a54c8-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a54c8-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a54c8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a54c8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a54c8-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a54c8-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a54c8-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a54c8-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a54c8-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a54c8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a54c8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a54c8-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a54c8-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a54c8-141">IID</span><span class="sxs-lookup"><span data-stu-id="a54c8-141">IID</span></span><br/>                      | <span data-ttu-id="a54c8-142">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a54c8-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a54c8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a54c8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54c8-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a54c8-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a54c8-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a54c8-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a54c8-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a54c8-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a54c8-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a54c8-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a54c8-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a54c8-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a54c8-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a54c8-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a54c8-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a54c8-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a54c8-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a54c8-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





