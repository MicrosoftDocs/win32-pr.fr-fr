---
title: IMsTscAx propriété CipherStrength
description: Récupère la force de chiffrement maximale du contrôle actuel.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété CipherStrength
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384032"
---
# <a name="imstscaxcipherstrength-property"></a><span data-ttu-id="f7c94-124">IMsTscAx :: CipherStrength, propriété</span><span class="sxs-lookup"><span data-stu-id="f7c94-124">IMsTscAx::CipherStrength property</span></span>

<span data-ttu-id="f7c94-125">Récupère la force de chiffrement maximale du contrôle actuel.</span><span class="sxs-lookup"><span data-stu-id="f7c94-125">Retrieves the maximum encryption strength of the current control.</span></span>

<span data-ttu-id="f7c94-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f7c94-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c94-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7c94-127">Syntax</span></span>


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a><span data-ttu-id="f7c94-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f7c94-128">Property value</span></span>

<span data-ttu-id="f7c94-129">Force de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f7c94-129">The encryption strength.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7c94-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f7c94-130">Error codes</span></span>

<span data-ttu-id="f7c94-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="f7c94-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c94-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f7c94-132">Remarks</span></span>

<span data-ttu-id="f7c94-133">Par Connexion Bureau à distance par le Web, la puissance de chiffrement est toujours 128, car le contrôle ActiveX Bureau à distance prend en charge le chiffrement jusqu’à 128 bits inclus.</span><span class="sxs-lookup"><span data-stu-id="f7c94-133">For Remote Desktop Web Connection, the cipher strength is always 128 because the Remote Desktop ActiveX control supports encryption up to and including 128 bits.</span></span> <span data-ttu-id="f7c94-134">Le contrôle 128 bits peut toujours se connecter à des serveurs de chiffrement 56 bits Bureau à distance des serveurs hôtes de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f7c94-134">The 128-bit control can still connect to 56 bit encryption Remote Desktop Session Host (RD Session Host) servers.</span></span>

<span data-ttu-id="f7c94-135">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f7c94-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c94-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7c94-136">Requirements</span></span>



| <span data-ttu-id="f7c94-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7c94-137">Requirement</span></span> | <span data-ttu-id="f7c94-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7c94-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c94-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7c94-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c94-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7c94-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7c94-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7c94-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c94-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7c94-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7c94-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f7c94-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7c94-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c94-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7c94-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c94-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c94-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c94-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7c94-147">IID</span><span class="sxs-lookup"><span data-stu-id="f7c94-147">IID</span></span><br/>                      | <span data-ttu-id="f7c94-148">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="f7c94-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f7c94-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7c94-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c94-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f7c94-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f7c94-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f7c94-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f7c94-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f7c94-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f7c94-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f7c94-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f7c94-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f7c94-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f7c94-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f7c94-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f7c94-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f7c94-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f7c94-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f7c94-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f7c94-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f7c94-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f7c94-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="f7c94-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





