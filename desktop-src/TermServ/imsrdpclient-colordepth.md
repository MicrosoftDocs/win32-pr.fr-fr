---
title: IMsRdpClient ColorDepth, propriété
description: Profondeur de couleur (en bits par pixel) de la connexion du contrôle.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- ColorDepth, propriété Services Bureau à distance
- ColorDepth Property Services Bureau à distance, IMsRdpClient, interface
- Services Bureau à distance de l’interface IMsRdpClient, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient2, interface
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient3, interface
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient4, interface
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient5, interface
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient6, interface
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient7, interface
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient8, interface
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient9, interface
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient10, interface
- Services Bureau à distance de l’interface IMsRdpClient10, propriété ColorDepth
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105877"
---
# <a name="imsrdpclientcolordepth-property"></a><span data-ttu-id="59887-124">IMsRdpClient :: ColorDepth, propriété</span><span class="sxs-lookup"><span data-stu-id="59887-124">IMsRdpClient::ColorDepth property</span></span>

<span data-ttu-id="59887-125">Profondeur de couleur (en bits par pixel) de la connexion du contrôle.</span><span class="sxs-lookup"><span data-stu-id="59887-125">The color depth (in bits per pixel) for the control's connection.</span></span>

<span data-ttu-id="59887-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="59887-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59887-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59887-127">Syntax</span></span>


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a><span data-ttu-id="59887-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="59887-128">Property value</span></span>

<span data-ttu-id="59887-129">Profondeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="59887-129">The color depth.</span></span> <span data-ttu-id="59887-130">Les valeurs incluent 8, 15, 16, 24 et 32 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="59887-130">Values include 8, 15, 16, 24, and 32 bits per pixel.</span></span>

## <a name="error-codes"></a><span data-ttu-id="59887-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="59887-131">Error codes</span></span>

<span data-ttu-id="59887-132">Si les méthodes sont correctement exécutées, la méthode **S \_ OK** est retournée.</span><span class="sxs-lookup"><span data-stu-id="59887-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="59887-133">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="59887-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="59887-134">Notes</span><span class="sxs-lookup"><span data-stu-id="59887-134">Remarks</span></span>

<span data-ttu-id="59887-135">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="59887-135">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="59887-136">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="59887-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59887-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59887-137">Requirements</span></span>



| <span data-ttu-id="59887-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59887-138">Requirement</span></span> | <span data-ttu-id="59887-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="59887-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59887-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59887-140">Minimum supported client</span></span><br/> | <span data-ttu-id="59887-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59887-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="59887-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59887-142">Minimum supported server</span></span><br/> | <span data-ttu-id="59887-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59887-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="59887-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="59887-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="59887-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59887-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="59887-146">DLL</span><span class="sxs-lookup"><span data-stu-id="59887-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59887-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59887-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="59887-148">IID</span><span class="sxs-lookup"><span data-stu-id="59887-148">IID</span></span><br/>                      | <span data-ttu-id="59887-149">IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="59887-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="59887-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59887-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59887-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="59887-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="59887-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="59887-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="59887-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="59887-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="59887-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="59887-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="59887-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="59887-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="59887-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="59887-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="59887-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="59887-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="59887-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="59887-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="59887-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="59887-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="59887-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="59887-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





