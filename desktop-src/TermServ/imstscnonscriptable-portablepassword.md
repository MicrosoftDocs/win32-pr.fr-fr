---
title: IMsTscNonScriptable propriété PortablePassword
description: Cette propriété ne peut plus être utilisée. | IMsTscNonScriptable propriété PortablePassword
ms.assetid: 8d831ed3-1f4a-41a9-b283-507c5d9eea22
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PortablePassword
- Services Bureau à distance de la propriété PortablePassword, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, propriété PortablePassword
- Propriété PortablePassword Services Bureau à distance, objet MsTscAx
- Objet MsTscAx Services Bureau à distance, propriété PortablePassword
- Services Bureau à distance de la propriété PortablePassword, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, propriété PortablePassword
- Services Bureau à distance de la propriété PortablePassword, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété PortablePassword
- Services Bureau à distance de la propriété PortablePassword, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété PortablePassword
- Services Bureau à distance de la propriété PortablePassword, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PortablePassword
- Services Bureau à distance de la propriété PortablePassword, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PortablePassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortablePassword
- IMsTscNonScriptable.get_PortablePassword
- IMsTscNonScriptable.put_PortablePassword
- MsTscAx.PortablePassword
- IMsRdpClientNonScriptable.PortablePassword
- IMsRdpClientNonScriptable.get_PortablePassword
- IMsRdpClientNonScriptable.put_PortablePassword
- IMsRdpClientNonScriptable2.PortablePassword
- IMsRdpClientNonScriptable2.get_PortablePassword
- IMsRdpClientNonScriptable2.put_PortablePassword
- IMsRdpClientNonScriptable3.PortablePassword
- IMsRdpClientNonScriptable3.get_PortablePassword
- IMsRdpClientNonScriptable3.put_PortablePassword
- IMsRdpClientNonScriptable4.PortablePassword
- IMsRdpClientNonScriptable4.get_PortablePassword
- IMsRdpClientNonScriptable4.put_PortablePassword
- IMsRdpClientNonScriptable5.PortablePassword
- IMsRdpClientNonScriptable5.get_PortablePassword
- IMsRdpClientNonScriptable5.put_PortablePassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5259e83087287395e6114bb8ffe3eb7e859ab52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106529561"
---
# <a name="imstscnonscriptableportablepassword-property"></a><span data-ttu-id="3d392-119">IMsTscNonScriptable ::P propriété ortablePassword</span><span class="sxs-lookup"><span data-stu-id="3d392-119">IMsTscNonScriptable::PortablePassword property</span></span>

<span data-ttu-id="3d392-120">Cette propriété ne peut plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="3d392-120">This property is no longer available for use.</span></span>

<span data-ttu-id="3d392-121">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d392-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d392-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d392-122">Syntax</span></span>


```C++
HRESULT put_PortablePassword(
  [in]  BSTR newPortablePassVal
);

HRESULT get_PortablePassword(
  [out] BSTR *pPortablePass
);
```



## <a name="property-value"></a><span data-ttu-id="3d392-123">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3d392-123">Property value</span></span>

<span data-ttu-id="3d392-124">Nouvelle partie du mot de passe, dans un format encodé portable.</span><span class="sxs-lookup"><span data-stu-id="3d392-124">The new password part, in portable encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d392-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3d392-125">Error codes</span></span>

<span data-ttu-id="3d392-126">Retourne **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="3d392-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d392-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d392-127">Requirements</span></span>



| <span data-ttu-id="3d392-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d392-128">Requirement</span></span> | <span data-ttu-id="3d392-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d392-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d392-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d392-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3d392-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d392-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3d392-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d392-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3d392-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d392-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3d392-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3d392-134">End of client support</span></span><br/>    | <span data-ttu-id="3d392-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d392-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3d392-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3d392-136">End of server support</span></span><br/>    | <span data-ttu-id="3d392-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d392-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3d392-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3d392-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d392-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d392-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3d392-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3d392-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d392-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d392-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3d392-142">IID</span><span class="sxs-lookup"><span data-stu-id="3d392-142">IID</span></span><br/>                      | <span data-ttu-id="3d392-143">IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="3d392-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d392-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d392-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d392-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="3d392-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="3d392-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="3d392-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="3d392-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="3d392-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="3d392-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="3d392-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="3d392-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="3d392-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="3d392-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="3d392-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





