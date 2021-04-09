---
title: IMsRdpClientAdvancedSettings propriété RDPPort
description: Spécifie le port de connexion.
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RDPPort
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106174"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a><span data-ttu-id="f7b9d-120">IMsRdpClientAdvancedSettings :: RDPPort, propriété</span><span class="sxs-lookup"><span data-stu-id="f7b9d-120">IMsRdpClientAdvancedSettings::RDPPort property</span></span>

<span data-ttu-id="f7b9d-121">Spécifie le port de connexion.</span><span class="sxs-lookup"><span data-stu-id="f7b9d-121">Specifies the connection port.</span></span>

<span data-ttu-id="f7b9d-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f7b9d-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b9d-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7b9d-123">Syntax</span></span>


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a><span data-ttu-id="f7b9d-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f7b9d-124">Property value</span></span>

<span data-ttu-id="f7b9d-125">Le nouveau port.</span><span class="sxs-lookup"><span data-stu-id="f7b9d-125">The new port.</span></span> <span data-ttu-id="f7b9d-126">La valeur par défaut est 3389.</span><span class="sxs-lookup"><span data-stu-id="f7b9d-126">The default value is 3389.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7b9d-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f7b9d-127">Error codes</span></span>

<span data-ttu-id="f7b9d-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="f7b9d-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b9d-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f7b9d-129">Remarks</span></span>

<span data-ttu-id="f7b9d-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f7b9d-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b9d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7b9d-131">Requirements</span></span>



| <span data-ttu-id="f7b9d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7b9d-132">Requirement</span></span> | <span data-ttu-id="f7b9d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7b9d-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b9d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b9d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b9d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7b9d-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f7b9d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b9d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b9d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7b9d-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f7b9d-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f7b9d-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7b9d-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b9d-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7b9d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b9d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b9d-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b9d-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7b9d-142">IID</span><span class="sxs-lookup"><span data-stu-id="f7b9d-142">IID</span></span><br/>                      | <span data-ttu-id="f7b9d-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f7b9d-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7b9d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7b9d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b9d-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f7b9d-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f7b9d-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f7b9d-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f7b9d-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f7b9d-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f7b9d-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f7b9d-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f7b9d-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





