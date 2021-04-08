---
title: IMsRdpClientNonScriptable4 propriété PublisherCertificateChain
description: Contrôle la chaîne du certificat de l’éditeur. La chaîne est stockée dans un variant de type VT \_ ByRef qui contient un pointeur vers une \_ structure de contexte de chaîne du certificat \_ . Pour plus d’informations sur les structures de type de données VT \_ , consultez variant et VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843853"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a><span data-ttu-id="6fea7-118">IMsRdpClientNonScriptable4 ::P propriété ublisherCertificateChain</span><span class="sxs-lookup"><span data-stu-id="6fea7-118">IMsRdpClientNonScriptable4::PublisherCertificateChain property</span></span>

<span data-ttu-id="6fea7-119">Contrôle la chaîne du certificat de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="6fea7-119">Controls the publisher certificate chain.</span></span> <span data-ttu-id="6fea7-120">La chaîne est stockée dans un variant de type **VT \_ ByRef** qui contient un pointeur vers une structure de [**\_ \_ contexte de chaîne du certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="6fea7-120">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span> <span data-ttu-id="6fea7-121">Pour plus d’informations sur les structures de type de données **VT \_** , consultez [Variant et VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="6fea7-121">For information about **VT\_BYREF** structures, see [VARIANT and VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="6fea7-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6fea7-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fea7-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fea7-123">Syntax</span></span>


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a><span data-ttu-id="6fea7-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6fea7-124">Property value</span></span>

<span data-ttu-id="6fea7-125">Définit la chaîne du certificat de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="6fea7-125">Sets the publisher certificate chain.</span></span> <span data-ttu-id="6fea7-126">La chaîne est stockée dans un variant de type **VT \_ ByRef** qui contient un pointeur vers une structure de [**\_ \_ contexte de chaîne du certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="6fea7-126">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6fea7-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6fea7-127">Error codes</span></span>

<span data-ttu-id="6fea7-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="6fea7-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fea7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fea7-129">Requirements</span></span>



| <span data-ttu-id="6fea7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fea7-130">Requirement</span></span> | <span data-ttu-id="6fea7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fea7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fea7-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fea7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6fea7-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fea7-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6fea7-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fea7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6fea7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fea7-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6fea7-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6fea7-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="6fea7-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fea7-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="6fea7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6fea7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fea7-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fea7-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="6fea7-140">IID</span><span class="sxs-lookup"><span data-stu-id="6fea7-140">IID</span></span><br/>                      | <span data-ttu-id="6fea7-141">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="6fea7-141">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fea7-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fea7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fea7-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6fea7-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6fea7-144">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6fea7-144">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

