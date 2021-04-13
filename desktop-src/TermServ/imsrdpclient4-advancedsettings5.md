---
title: IMsRdpClient4 propriété AdvancedSettings5
description: Récupère un pointeur vers une interface IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509402"
---
# <a name="imsrdpclient4advancedsettings5-property"></a><span data-ttu-id="d20c3-118">IMsRdpClient4 :: AdvancedSettings5, propriété</span><span class="sxs-lookup"><span data-stu-id="d20c3-118">IMsRdpClient4::AdvancedSettings5 property</span></span>

<span data-ttu-id="d20c3-119">Récupère un pointeur vers une interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="d20c3-119">Retrieves a pointer to an [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="d20c3-120">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d20c3-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d20c3-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d20c3-121">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="d20c3-122">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d20c3-122">Property value</span></span>

<span data-ttu-id="d20c3-123">Pointeur vers l’interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="d20c3-123">A pointer to the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span> <span data-ttu-id="d20c3-124">L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.</span><span class="sxs-lookup"><span data-stu-id="d20c3-124">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d20c3-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d20c3-125">Error codes</span></span>

<span data-ttu-id="d20c3-126">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="d20c3-126">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="d20c3-127">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="d20c3-127">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d20c3-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d20c3-128">Remarks</span></span>

<span data-ttu-id="d20c3-129">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="d20c3-129">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="d20c3-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d20c3-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d20c3-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d20c3-131">Requirements</span></span>



| <span data-ttu-id="d20c3-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d20c3-132">Requirement</span></span> | <span data-ttu-id="d20c3-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d20c3-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d20c3-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d20c3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d20c3-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d20c3-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d20c3-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d20c3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d20c3-137">Windows Server 2008, Windows Server 2008 avec SP1</span><span class="sxs-lookup"><span data-stu-id="d20c3-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="d20c3-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d20c3-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="d20c3-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d20c3-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d20c3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d20c3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d20c3-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d20c3-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d20c3-142">IID</span><span class="sxs-lookup"><span data-stu-id="d20c3-142">IID</span></span><br/>                      | <span data-ttu-id="d20c3-143">IMsRdpClient4 est défini en tant que 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span><span class="sxs-lookup"><span data-stu-id="d20c3-143">IMsRdpClient4 is defined as 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d20c3-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d20c3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d20c3-145">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="d20c3-145">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="d20c3-146">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="d20c3-146">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="d20c3-147">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d20c3-147">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d20c3-148">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d20c3-148">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d20c3-149">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d20c3-149">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d20c3-150">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d20c3-150">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d20c3-151">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d20c3-151">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





