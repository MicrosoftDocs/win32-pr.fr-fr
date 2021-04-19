---
title: IMsRdpClientNonScriptable3 propriété NegotiateSecurityLayer
description: Spécifie ou récupère si la couche de sécurité de négociation est activée pour la connexion.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540776"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a><span data-ttu-id="a7ac4-120">IMsRdpClientNonScriptable3 :: NegotiateSecurityLayer, propriété</span><span class="sxs-lookup"><span data-stu-id="a7ac4-120">IMsRdpClientNonScriptable3::NegotiateSecurityLayer property</span></span>

<span data-ttu-id="a7ac4-121">Spécifie ou récupère si la couche de sécurité de négociation est activée pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="a7ac4-121">Specifies or retrieves whether the negotiation security layer is enabled for the connection.</span></span>

<span data-ttu-id="a7ac4-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a7ac4-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ac4-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7ac4-123">Syntax</span></span>


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a><span data-ttu-id="a7ac4-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a7ac4-124">Property value</span></span>

<span data-ttu-id="a7ac4-125">Spécifie s’il faut activer la négociation de la couche de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a7ac4-125">Specifies whether to enable negotiation of the security layer.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7ac4-126">Notes</span><span class="sxs-lookup"><span data-stu-id="a7ac4-126">Remarks</span></span>

<span data-ttu-id="a7ac4-127">Si cette propriété est définie sur **\_ false** et que authentification au niveau du réseau (NLA) est activé sur le système d’exploitation client, le client ne négociera pas la couche de sécurité et utilisera NLA pour sécuriser la connexion RDP.</span><span class="sxs-lookup"><span data-stu-id="a7ac4-127">If this property is set to **VARIANT\_FALSE** and Network Level Authentication (NLA) is enabled on the client operating system, the client will not negotiate the security layer and instead, it will use NLA to secure the RDP connection.</span></span> <span data-ttu-id="a7ac4-128">Si cette propriété a la valeur **Variant \_ true**, le client négocie entre NLA et la sécurité RDP de base.</span><span class="sxs-lookup"><span data-stu-id="a7ac4-128">If this property is set to **VARIANT\_TRUE**, then the client will negotiate between NLA and basic RDP security.</span></span>

> [!Note]  
> <span data-ttu-id="a7ac4-129">La désactivation de la négociation de la couche de sécurité est possible uniquement lors de la connexion à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) exécutant Windows Vista ou des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="a7ac4-129">Disabling security layer negotiation is only possible when connecting to a Remote Desktop Session Host (RD Session Host) server running Windows Vista or later operating systems.</span></span> <span data-ttu-id="a7ac4-130">Si cette propriété est activée et que le client tente de se connecter à un serveur hôte de session Bureau à distance exécutant un système d’exploitation antérieur, la connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="a7ac4-130">If this property is enabled and the client attempts to connect to an RD Session Host server running an earlier operating system, the connection will fail.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7ac4-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7ac4-131">Requirements</span></span>



| <span data-ttu-id="a7ac4-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7ac4-132">Requirement</span></span> | <span data-ttu-id="a7ac4-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7ac4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ac4-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7ac4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ac4-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7ac4-135">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a7ac4-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7ac4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ac4-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7ac4-137">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a7ac4-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a7ac4-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7ac4-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7ac4-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a7ac4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ac4-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7ac4-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7ac4-141"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a7ac4-142">IID</span><span class="sxs-lookup"><span data-stu-id="a7ac4-142">IID</span></span><br/>                      | <span data-ttu-id="a7ac4-143">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="a7ac4-143">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7ac4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7ac4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ac4-145">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a7ac4-145">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="a7ac4-146">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a7ac4-146">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a7ac4-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="a7ac4-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





