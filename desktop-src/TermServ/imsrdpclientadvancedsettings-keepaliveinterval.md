---
title: IMsRdpClientAdvancedSettings keepAliveInterval, propriété
description: Spécifie un intervalle, en millisecondes, auquel le client envoie des messages Keep-Alive au serveur.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- propriété keepAliveInterval Services Bureau à distance
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété keepAliveInterval
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété keepAliveInterval
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété keepAliveInterval
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété keepAliveInterval
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété keepAliveInterval
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété keepAliveInterval
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété keepAliveInterval
- propriété keepAliveInterval Services Bureau à distance, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété keepAliveInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d15412b5b1803aadcffa08a8617742e0c90b1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384311"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a><span data-ttu-id="6d4d7-120">IMsRdpClientAdvancedSettings :: keepAliveInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="6d4d7-120">IMsRdpClientAdvancedSettings::keepAliveInterval property</span></span>

<span data-ttu-id="6d4d7-121">Spécifie un intervalle, en millisecondes, auquel le client envoie des messages Keep-Alive au serveur.</span><span class="sxs-lookup"><span data-stu-id="6d4d7-121">Specifies an interval, in milliseconds, at which the client sends keep-alive messages to the server.</span></span>

<span data-ttu-id="6d4d7-122">Paramètre de stratégie de groupe qui spécifie si les connexions clientes persistantes au serveur sont autorisées peuvent remplacer ce paramètre de propriété.</span><span class="sxs-lookup"><span data-stu-id="6d4d7-122">A group policy setting that specifies whether persistent client connections to the server are allowed can override this property setting.</span></span>

<span data-ttu-id="6d4d7-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6d4d7-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4d7-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d4d7-124">Syntax</span></span>


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a><span data-ttu-id="6d4d7-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6d4d7-125">Property value</span></span>

<span data-ttu-id="6d4d7-126">Nouvel intervalle, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="6d4d7-126">The new interval, in milliseconds.</span></span> <span data-ttu-id="6d4d7-127">La valeur par défaut de la propriété est zéro, ce qui désactive les messages Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="6d4d7-127">The default value of the property is zero, which disables keep-alive messages.</span></span> <span data-ttu-id="6d4d7-128">La valeur minimale valide de cette propriété est 10 000, qui représente 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="6d4d7-128">The minimum valid value of this property is 10,000, which represents 10 seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d4d7-129">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6d4d7-129">Error codes</span></span>

<span data-ttu-id="6d4d7-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="6d4d7-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d4d7-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6d4d7-131">Remarks</span></span>

<span data-ttu-id="6d4d7-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6d4d7-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4d7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d4d7-133">Requirements</span></span>



| <span data-ttu-id="6d4d7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d4d7-134">Requirement</span></span> | <span data-ttu-id="6d4d7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d4d7-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4d7-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d4d7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4d7-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d4d7-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6d4d7-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d4d7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4d7-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d4d7-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6d4d7-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6d4d7-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d4d7-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d4d7-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6d4d7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6d4d7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d4d7-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d4d7-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6d4d7-144">IID</span><span class="sxs-lookup"><span data-stu-id="6d4d7-144">IID</span></span><br/>                      | <span data-ttu-id="6d4d7-145">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6d4d7-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d4d7-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d4d7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4d7-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6d4d7-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6d4d7-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6d4d7-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6d4d7-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6d4d7-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6d4d7-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6d4d7-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6d4d7-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





