---
title: IMsRdpClientAdvancedSettings propriété DoubleClickDetect
description: Spécifie si le client identifie les double-clics pour le serveur.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété DoubleClickDetect
- Services Bureau à distance de la propriété DoubleClickDetect, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété DoubleClickDetect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd771614a80d909e0e7a748ab7256a5310084deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105868"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a><span data-ttu-id="73d68-120">IMsRdpClientAdvancedSettings ::D propriété oubleClickDetect</span><span class="sxs-lookup"><span data-stu-id="73d68-120">IMsRdpClientAdvancedSettings::DoubleClickDetect property</span></span>

<span data-ttu-id="73d68-121">Spécifie si le client identifie les double-clics pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="73d68-121">Specifies if the client identifies double-clicks for the server.</span></span>

<span data-ttu-id="73d68-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="73d68-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d68-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73d68-123">Syntax</span></span>


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a><span data-ttu-id="73d68-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="73d68-124">Property value</span></span>

<span data-ttu-id="73d68-125">Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="73d68-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73d68-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="73d68-126">Error codes</span></span>

<span data-ttu-id="73d68-127">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="73d68-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="73d68-128">Notes</span><span class="sxs-lookup"><span data-stu-id="73d68-128">Remarks</span></span>

<span data-ttu-id="73d68-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="73d68-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73d68-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73d68-130">Requirements</span></span>



| <span data-ttu-id="73d68-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73d68-131">Requirement</span></span> | <span data-ttu-id="73d68-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="73d68-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73d68-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73d68-133">Minimum supported client</span></span><br/> | <span data-ttu-id="73d68-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73d68-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="73d68-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73d68-135">Minimum supported server</span></span><br/> | <span data-ttu-id="73d68-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73d68-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="73d68-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="73d68-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="73d68-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73d68-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="73d68-139">DLL</span><span class="sxs-lookup"><span data-stu-id="73d68-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73d68-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73d68-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="73d68-141">IID</span><span class="sxs-lookup"><span data-stu-id="73d68-141">IID</span></span><br/>                      | <span data-ttu-id="73d68-142">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="73d68-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73d68-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73d68-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d68-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="73d68-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="73d68-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="73d68-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="73d68-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="73d68-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="73d68-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="73d68-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="73d68-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="73d68-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="73d68-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="73d68-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="73d68-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="73d68-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="73d68-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="73d68-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





