---
title: IMsRdpClientAdvancedSettings2 propriété EnableAutoReconnect
description: Spécifie s’il faut activer le contrôle client pour qu’il se reconnecte automatiquement à une session en cas de déconnexion d’un réseau.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EnableAutoReconnect
- Services Bureau à distance de la propriété EnableAutoReconnect, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété EnableAutoReconnect
- Services Bureau à distance de la propriété EnableAutoReconnect, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété EnableAutoReconnect
- Services Bureau à distance de la propriété EnableAutoReconnect, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété EnableAutoReconnect
- Services Bureau à distance de la propriété EnableAutoReconnect, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété EnableAutoReconnect
- Services Bureau à distance de la propriété EnableAutoReconnect, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété EnableAutoReconnect
- Services Bureau à distance de la propriété EnableAutoReconnect, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété EnableAutoReconnect
- Services Bureau à distance de la propriété EnableAutoReconnect, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété EnableAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510337"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a><span data-ttu-id="1447f-118">IMsRdpClientAdvancedSettings2 :: EnableAutoReconnect, propriété</span><span class="sxs-lookup"><span data-stu-id="1447f-118">IMsRdpClientAdvancedSettings2::EnableAutoReconnect property</span></span>

<span data-ttu-id="1447f-119">Spécifie s’il faut activer le contrôle client pour qu’il se reconnecte automatiquement à une session en cas de déconnexion d’un réseau.</span><span class="sxs-lookup"><span data-stu-id="1447f-119">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span>

<span data-ttu-id="1447f-120">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1447f-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1447f-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1447f-121">Syntax</span></span>


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="1447f-122">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1447f-122">Property value</span></span>

<span data-ttu-id="1447f-123">Affectez la valeur **Variant \_ true** pour activer la reconnexion automatique et la valeur **\_ false à false** pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="1447f-123">Set to **VARIANT\_TRUE** to enable automatic reconnection, and to **VARIANT\_FALSE** to disable it.</span></span> <span data-ttu-id="1447f-124">La valeur par défaut est **\_ true**.</span><span class="sxs-lookup"><span data-stu-id="1447f-124">The default is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1447f-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1447f-125">Error codes</span></span>

<span data-ttu-id="1447f-126">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="1447f-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1447f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1447f-127">Remarks</span></span>

<span data-ttu-id="1447f-128">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="1447f-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="1447f-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1447f-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1447f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1447f-130">Requirements</span></span>



| <span data-ttu-id="1447f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1447f-131">Requirement</span></span> | <span data-ttu-id="1447f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1447f-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1447f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1447f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1447f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1447f-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1447f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1447f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1447f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1447f-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1447f-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1447f-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="1447f-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1447f-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1447f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1447f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1447f-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1447f-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1447f-141">IID</span><span class="sxs-lookup"><span data-stu-id="1447f-141">IID</span></span><br/>                      | <span data-ttu-id="1447f-142">IID \_ IMsRdpClientAdvancedSettings2 est défini en tant que 9ac42117-2b76-4320-AA44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="1447f-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1447f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1447f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1447f-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1447f-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1447f-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1447f-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1447f-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1447f-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="1447f-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1447f-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1447f-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1447f-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1447f-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1447f-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1447f-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1447f-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





