---
title: IMsRdpClientAdvancedSettings2 propriété MaxReconnectAttempts
description: Spécifie le nombre de tentatives de connexion lors de la reconnexion automatique.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété MaxReconnectAttempts
- Services Bureau à distance de la propriété MaxReconnectAttempts, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété MaxReconnectAttempts
- Services Bureau à distance de la propriété MaxReconnectAttempts, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété MaxReconnectAttempts
- Services Bureau à distance de la propriété MaxReconnectAttempts, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété MaxReconnectAttempts
- Services Bureau à distance de la propriété MaxReconnectAttempts, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété MaxReconnectAttempts
- Services Bureau à distance de la propriété MaxReconnectAttempts, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété MaxReconnectAttempts
- Services Bureau à distance de la propriété MaxReconnectAttempts, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété MaxReconnectAttempts
- Services Bureau à distance de la propriété MaxReconnectAttempts, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété MaxReconnectAttempts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536294"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a><span data-ttu-id="bc3fb-118">IMsRdpClientAdvancedSettings2 :: MaxReconnectAttempts, propriété</span><span class="sxs-lookup"><span data-stu-id="bc3fb-118">IMsRdpClientAdvancedSettings2::MaxReconnectAttempts property</span></span>

<span data-ttu-id="bc3fb-119">Spécifie le nombre de tentatives de connexion lors de la reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-119">Specifies the number of times to try to reconnect during automatic reconnection.</span></span>

<span data-ttu-id="bc3fb-120">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3fb-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc3fb-121">Syntax</span></span>


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a><span data-ttu-id="bc3fb-122">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bc3fb-122">Property value</span></span>

<span data-ttu-id="bc3fb-123">Nouveau nombre de nouvelles tentatives.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-123">The new number of retries.</span></span> <span data-ttu-id="bc3fb-124">Les valeurs valides sont comprises entre 0 et 200 inclus.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-124">The valid values are 0 to 200, inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc3fb-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="bc3fb-125">Error codes</span></span>

<span data-ttu-id="bc3fb-126">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc3fb-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bc3fb-127">Remarks</span></span>

<span data-ttu-id="bc3fb-128">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="bc3fb-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bc3fb-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc3fb-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc3fb-130">Requirements</span></span>



| <span data-ttu-id="bc3fb-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc3fb-131">Requirement</span></span> | <span data-ttu-id="bc3fb-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc3fb-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3fb-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc3fb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3fb-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc3fb-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bc3fb-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc3fb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3fb-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc3fb-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bc3fb-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bc3fb-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc3fb-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc3fb-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bc3fb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bc3fb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc3fb-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc3fb-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bc3fb-141">IID</span><span class="sxs-lookup"><span data-stu-id="bc3fb-141">IID</span></span><br/>                      | <span data-ttu-id="bc3fb-142">IID \_ IMsRdpClientAdvancedSettings2 est défini en tant que 9ac42117-2b76-4320-AA44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="bc3fb-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc3fb-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc3fb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3fb-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





