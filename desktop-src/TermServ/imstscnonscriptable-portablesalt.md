---
title: IMsTscNonScriptable propriété PortableSalt
description: Cette propriété n'est plus prise en charge.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, propriété PortableSalt
- Propriété PortableSalt Services Bureau à distance, objet MsTscAx
- Objet MsTscAx Services Bureau à distance, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PortableSalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742388"
---
# <a name="imstscnonscriptableportablesalt-property"></a><span data-ttu-id="a22cd-118">IMsTscNonScriptable ::P propriété ortableSalt</span><span class="sxs-lookup"><span data-stu-id="a22cd-118">IMsTscNonScriptable::PortableSalt property</span></span>

<span data-ttu-id="a22cd-119">Cette propriété n'est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a22cd-119">This property is no longer supported.</span></span>

<span data-ttu-id="a22cd-120">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a22cd-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22cd-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a22cd-121">Syntax</span></span>


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a><span data-ttu-id="a22cd-122">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a22cd-122">Property value</span></span>

<span data-ttu-id="a22cd-123">Nouvelle partie Salt portable pour un mot de passe encodé portable.</span><span class="sxs-lookup"><span data-stu-id="a22cd-123">The new portable salt part for a portable encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a22cd-124">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a22cd-124">Error codes</span></span>

<span data-ttu-id="a22cd-125">Retourne **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="a22cd-125">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a22cd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a22cd-126">Requirements</span></span>



| <span data-ttu-id="a22cd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a22cd-127">Requirement</span></span> | <span data-ttu-id="a22cd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a22cd-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a22cd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a22cd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a22cd-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a22cd-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a22cd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a22cd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a22cd-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a22cd-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a22cd-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a22cd-133">End of client support</span></span><br/>    | <span data-ttu-id="a22cd-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a22cd-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a22cd-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a22cd-135">End of server support</span></span><br/>    | <span data-ttu-id="a22cd-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a22cd-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a22cd-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a22cd-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a22cd-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22cd-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a22cd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a22cd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22cd-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22cd-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a22cd-141">IID</span><span class="sxs-lookup"><span data-stu-id="a22cd-141">IID</span></span><br/>                      | <span data-ttu-id="a22cd-142">IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="a22cd-142">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a22cd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a22cd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22cd-144">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a22cd-144">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="a22cd-145">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="a22cd-145">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="a22cd-146">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="a22cd-146">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="a22cd-147">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a22cd-147">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="a22cd-148">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a22cd-148">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a22cd-149">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a22cd-149">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="a22cd-150">**PortablePassword**</span><span class="sxs-lookup"><span data-stu-id="a22cd-150">**PortablePassword**</span></span>](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





