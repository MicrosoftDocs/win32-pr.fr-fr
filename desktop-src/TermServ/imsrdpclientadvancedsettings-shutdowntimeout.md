---
title: IMsRdpClientAdvancedSettings shutdownTimeout, propriété
description: Spécifie la durée, en secondes, à attendre que le serveur réponde à une demande de déconnexion.
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- shutdownTimeout, propriété Services Bureau à distance
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings2, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings3, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings4, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings5, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings6, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings7, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings8, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété shutdownTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383895"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a><span data-ttu-id="fb594-120">IMsRdpClientAdvancedSettings :: shutdownTimeout, propriété</span><span class="sxs-lookup"><span data-stu-id="fb594-120">IMsRdpClientAdvancedSettings::shutdownTimeout property</span></span>

<span data-ttu-id="fb594-121">Spécifie la durée, en secondes, à attendre que le serveur réponde à une demande de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="fb594-121">Specifies the length of time, in seconds, to wait for the server to respond to a disconnection request.</span></span>

<span data-ttu-id="fb594-122">Si le serveur ne répond pas dans le délai spécifié, le contrôle client se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="fb594-122">If the server does not reply within the specified time, the client control disconnects.</span></span>

<span data-ttu-id="fb594-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fb594-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb594-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb594-124">Syntax</span></span>


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="fb594-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fb594-125">Property value</span></span>

<span data-ttu-id="fb594-126">Nouvelle durée, en secondes.</span><span class="sxs-lookup"><span data-stu-id="fb594-126">The new time, in seconds.</span></span> <span data-ttu-id="fb594-127">La valeur par défaut de la propriété est 10.</span><span class="sxs-lookup"><span data-stu-id="fb594-127">The default value of the property is 10.</span></span> <span data-ttu-id="fb594-128">La valeur maximale est 600, qui représente 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="fb594-128">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb594-129">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fb594-129">Error codes</span></span>

<span data-ttu-id="fb594-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="fb594-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb594-131">Notes</span><span class="sxs-lookup"><span data-stu-id="fb594-131">Remarks</span></span>

<span data-ttu-id="fb594-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fb594-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb594-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb594-133">Requirements</span></span>



| <span data-ttu-id="fb594-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb594-134">Requirement</span></span> | <span data-ttu-id="fb594-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb594-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb594-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb594-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fb594-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb594-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fb594-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb594-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fb594-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb594-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fb594-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fb594-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb594-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb594-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fb594-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fb594-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb594-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb594-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fb594-144">IID</span><span class="sxs-lookup"><span data-stu-id="fb594-144">IID</span></span><br/>                      | <span data-ttu-id="fb594-145">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="fb594-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb594-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb594-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb594-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fb594-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fb594-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fb594-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fb594-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fb594-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fb594-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fb594-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fb594-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fb594-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fb594-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fb594-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fb594-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fb594-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fb594-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fb594-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





