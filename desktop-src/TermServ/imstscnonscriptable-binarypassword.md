---
title: IMsTscNonScriptable propriété BinaryPassword
description: Cette propriété ne peut plus être utilisée. | IMsTscNonScriptable propriété BinaryPassword
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BinaryPassword
- Services Bureau à distance de la propriété BinaryPassword, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, propriété BinaryPassword
- Propriété BinaryPassword Services Bureau à distance, objet MsTscAx
- Objet MsTscAx Services Bureau à distance, propriété BinaryPassword
- Services Bureau à distance de la propriété BinaryPassword, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, propriété BinaryPassword
- Services Bureau à distance de la propriété BinaryPassword, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété BinaryPassword
- Services Bureau à distance de la propriété BinaryPassword, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété BinaryPassword
- Services Bureau à distance de la propriété BinaryPassword, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété BinaryPassword
- Services Bureau à distance de la propriété BinaryPassword, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété BinaryPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d6eab2a3902968ef4d4c953a8da8b9c884a497
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537205"
---
# <a name="imstscnonscriptablebinarypassword-property"></a><span data-ttu-id="be74f-119">IMsTscNonScriptable :: BinaryPassword, propriété</span><span class="sxs-lookup"><span data-stu-id="be74f-119">IMsTscNonScriptable::BinaryPassword property</span></span>

<span data-ttu-id="be74f-120">Cette propriété ne peut plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="be74f-120">This property is no longer available for use.</span></span>

<span data-ttu-id="be74f-121">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="be74f-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="be74f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be74f-122">Syntax</span></span>


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a><span data-ttu-id="be74f-123">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="be74f-123">Property value</span></span>

<span data-ttu-id="be74f-124">Nouvelle partie du mot de passe, au format binaire encodé.</span><span class="sxs-lookup"><span data-stu-id="be74f-124">The new password part, in binary encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="be74f-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="be74f-125">Error codes</span></span>

<span data-ttu-id="be74f-126">Retourne **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="be74f-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="be74f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be74f-127">Requirements</span></span>



| <span data-ttu-id="be74f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be74f-128">Requirement</span></span> | <span data-ttu-id="be74f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="be74f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be74f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be74f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="be74f-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be74f-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be74f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be74f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="be74f-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be74f-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be74f-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="be74f-134">End of client support</span></span><br/>    | <span data-ttu-id="be74f-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be74f-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be74f-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="be74f-136">End of server support</span></span><br/>    | <span data-ttu-id="be74f-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be74f-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be74f-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="be74f-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="be74f-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be74f-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="be74f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="be74f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be74f-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be74f-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="be74f-142">IID</span><span class="sxs-lookup"><span data-stu-id="be74f-142">IID</span></span><br/>                      | <span data-ttu-id="be74f-143">IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="be74f-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be74f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be74f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be74f-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="be74f-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="be74f-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="be74f-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="be74f-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="be74f-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="be74f-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="be74f-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="be74f-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="be74f-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="be74f-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="be74f-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





