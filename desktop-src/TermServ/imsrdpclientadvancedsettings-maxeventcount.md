---
title: IMsRdpClientAdvancedSettings propriété maxEventCount
description: Cette propriété n'est pas prise en charge. | IMsRdpClientAdvancedSettings propriété maxEventCount
ms.assetid: d7b5951d-8cc3-48b4-af1b-1f547afbc6ae
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété maxEventCount
- Services Bureau à distance de la propriété maxEventCount, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété maxEventCount
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.maxEventCount
- IMsRdpClientAdvancedSettings.get_maxEventCount
- IMsRdpClientAdvancedSettings.put_maxEventCount
- IMsRdpClientAdvancedSettings2.maxEventCount
- IMsRdpClientAdvancedSettings2.get_maxEventCount
- IMsRdpClientAdvancedSettings2.put_maxEventCount
- IMsRdpClientAdvancedSettings3.maxEventCount
- IMsRdpClientAdvancedSettings3.get_maxEventCount
- IMsRdpClientAdvancedSettings3.put_maxEventCount
- IMsRdpClientAdvancedSettings4.maxEventCount
- IMsRdpClientAdvancedSettings4.get_maxEventCount
- IMsRdpClientAdvancedSettings4.put_maxEventCount
- IMsRdpClientAdvancedSettings5.maxEventCount
- IMsRdpClientAdvancedSettings5.get_maxEventCount
- IMsRdpClientAdvancedSettings5.put_maxEventCount
- IMsRdpClientAdvancedSettings6.maxEventCount
- IMsRdpClientAdvancedSettings6.get_maxEventCount
- IMsRdpClientAdvancedSettings6.put_maxEventCount
- IMsRdpClientAdvancedSettings7.maxEventCount
- IMsRdpClientAdvancedSettings7.get_maxEventCount
- IMsRdpClientAdvancedSettings7.put_maxEventCount
- IMsRdpClientAdvancedSettings8.maxEventCount
- IMsRdpClientAdvancedSettings8.get_maxEventCount
- IMsRdpClientAdvancedSettings8.put_maxEventCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb305d4a81b3c4dd9eb53dceab5a4e685c57c060
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869777"
---
# <a name="imsrdpclientadvancedsettingsmaxeventcount-property"></a><span data-ttu-id="93142-121">IMsRdpClientAdvancedSettings :: maxEventCount, propriété</span><span class="sxs-lookup"><span data-stu-id="93142-121">IMsRdpClientAdvancedSettings::maxEventCount property</span></span>

<span data-ttu-id="93142-122">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="93142-122">This property is not supported.</span></span>

<span data-ttu-id="93142-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="93142-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="93142-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93142-124">Syntax</span></span>


```C++
HRESULT put_maxEventCount(
  [in]  LONG maxEventCount
);

HRESULT get_maxEventCount(
  [out] LONG pmaxEventCount
);
```



## <a name="property-value"></a><span data-ttu-id="93142-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="93142-125">Property value</span></span>

<span data-ttu-id="93142-126">Nouveau nombre d’événements.</span><span class="sxs-lookup"><span data-stu-id="93142-126">The new event count.</span></span> <span data-ttu-id="93142-127">La valeur par défaut est 100.</span><span class="sxs-lookup"><span data-stu-id="93142-127">The default is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="93142-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="93142-128">Error codes</span></span>

<span data-ttu-id="93142-129">Retourne **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="93142-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93142-130">Notes</span><span class="sxs-lookup"><span data-stu-id="93142-130">Remarks</span></span>

<span data-ttu-id="93142-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="93142-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93142-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93142-132">Requirements</span></span>



| <span data-ttu-id="93142-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93142-133">Requirement</span></span> | <span data-ttu-id="93142-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="93142-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93142-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93142-135">Minimum supported client</span></span><br/> | <span data-ttu-id="93142-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="93142-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="93142-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93142-137">Minimum supported server</span></span><br/> | <span data-ttu-id="93142-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="93142-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="93142-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="93142-139">End of client support</span></span><br/>    | <span data-ttu-id="93142-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="93142-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="93142-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="93142-141">End of server support</span></span><br/>    | <span data-ttu-id="93142-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="93142-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="93142-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="93142-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="93142-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93142-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="93142-145">DLL</span><span class="sxs-lookup"><span data-stu-id="93142-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93142-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93142-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="93142-147">IID</span><span class="sxs-lookup"><span data-stu-id="93142-147">IID</span></span><br/>                      | <span data-ttu-id="93142-148">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="93142-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93142-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93142-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93142-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="93142-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="93142-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="93142-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="93142-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="93142-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="93142-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="93142-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="93142-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="93142-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="93142-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="93142-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="93142-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="93142-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="93142-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="93142-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





