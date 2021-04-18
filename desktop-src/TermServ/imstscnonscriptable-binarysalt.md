---
title: IMsTscNonScriptable propriété BinarySalt
description: Cette propriété ne peut plus être utilisée. | IMsTscNonScriptable propriété BinarySalt
ms.assetid: 7af2e5be-9ddb-46ab-947c-f79ab890d7bc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BinarySalt
- Services Bureau à distance de la propriété BinarySalt, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, propriété BinarySalt
- Propriété BinarySalt Services Bureau à distance, objet MsTscAx
- Objet MsTscAx Services Bureau à distance, propriété BinarySalt
- Services Bureau à distance de la propriété BinarySalt, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, propriété BinarySalt
- Services Bureau à distance de la propriété BinarySalt, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété BinarySalt
- Services Bureau à distance de la propriété BinarySalt, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété BinarySalt
- Services Bureau à distance de la propriété BinarySalt, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété BinarySalt
- Services Bureau à distance de la propriété BinarySalt, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété BinarySalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinarySalt
- IMsTscNonScriptable.get_BinarySalt
- IMsTscNonScriptable.put_BinarySalt
- MsTscAx.BinarySalt
- IMsRdpClientNonScriptable.BinarySalt
- IMsRdpClientNonScriptable.get_BinarySalt
- IMsRdpClientNonScriptable.put_BinarySalt
- IMsRdpClientNonScriptable2.BinarySalt
- IMsRdpClientNonScriptable2.get_BinarySalt
- IMsRdpClientNonScriptable2.put_BinarySalt
- IMsRdpClientNonScriptable3.BinarySalt
- IMsRdpClientNonScriptable3.get_BinarySalt
- IMsRdpClientNonScriptable3.put_BinarySalt
- IMsRdpClientNonScriptable4.BinarySalt
- IMsRdpClientNonScriptable4.get_BinarySalt
- IMsRdpClientNonScriptable4.put_BinarySalt
- IMsRdpClientNonScriptable5.BinarySalt
- IMsRdpClientNonScriptable5.get_BinarySalt
- IMsRdpClientNonScriptable5.put_BinarySalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb13ccb79a9cf2c309a32772a73b393756c7bdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106527060"
---
# <a name="imstscnonscriptablebinarysalt-property"></a><span data-ttu-id="7a93d-119">IMsTscNonScriptable :: BinarySalt, propriété</span><span class="sxs-lookup"><span data-stu-id="7a93d-119">IMsTscNonScriptable::BinarySalt property</span></span>

<span data-ttu-id="7a93d-120">Cette propriété ne peut plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="7a93d-120">This property is no longer available for use.</span></span>

<span data-ttu-id="7a93d-121">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7a93d-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a93d-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a93d-122">Syntax</span></span>


```C++
HRESULT put_BinarySalt(
  [in]  BSTR newSalt
);

HRESULT get_BinarySalt(
  [out] BSTR *pSalt
);
```



## <a name="property-value"></a><span data-ttu-id="7a93d-123">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7a93d-123">Property value</span></span>

<span data-ttu-id="7a93d-124">Nouvelle partie Salt binaire pour un mot de passe encodé binaire.</span><span class="sxs-lookup"><span data-stu-id="7a93d-124">The new binary salt part for a binary encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a93d-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7a93d-125">Error codes</span></span>

<span data-ttu-id="7a93d-126">Retourne **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="7a93d-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a93d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a93d-127">Requirements</span></span>



| <span data-ttu-id="7a93d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a93d-128">Requirement</span></span> | <span data-ttu-id="7a93d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a93d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a93d-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a93d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a93d-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a93d-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7a93d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a93d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a93d-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a93d-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7a93d-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7a93d-134">End of client support</span></span><br/>    | <span data-ttu-id="7a93d-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a93d-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7a93d-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7a93d-136">End of server support</span></span><br/>    | <span data-ttu-id="7a93d-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a93d-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7a93d-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7a93d-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a93d-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a93d-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a93d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7a93d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a93d-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a93d-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a93d-142">IID</span><span class="sxs-lookup"><span data-stu-id="7a93d-142">IID</span></span><br/>                      | <span data-ttu-id="7a93d-143">IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="7a93d-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a93d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a93d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a93d-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="7a93d-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="7a93d-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="7a93d-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="7a93d-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="7a93d-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="7a93d-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="7a93d-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="7a93d-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="7a93d-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="7a93d-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="7a93d-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





