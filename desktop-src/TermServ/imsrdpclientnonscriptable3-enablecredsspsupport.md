---
title: IMsRdpClientNonScriptable3 propriété EnableCredSspSupport
description: Spécifie ou récupère si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103533"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a><span data-ttu-id="8e5c5-120">IMsRdpClientNonScriptable3 :: EnableCredSspSupport, propriété</span><span class="sxs-lookup"><span data-stu-id="8e5c5-120">IMsRdpClientNonScriptable3::EnableCredSspSupport property</span></span>

<span data-ttu-id="8e5c5-121">Spécifie ou récupère si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="8e5c5-121">Specifies or retrieves whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="8e5c5-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8e5c5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5c5-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e5c5-123">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="8e5c5-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8e5c5-124">Property value</span></span>

<span data-ttu-id="8e5c5-125">Spécifie si CredSSP est activé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="8e5c5-125">Specifies whether CredSSP is enabled for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e5c5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e5c5-126">Requirements</span></span>



| <span data-ttu-id="8e5c5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e5c5-127">Requirement</span></span> | <span data-ttu-id="8e5c5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e5c5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5c5-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e5c5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5c5-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e5c5-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="8e5c5-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e5c5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5c5-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e5c5-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="8e5c5-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8e5c5-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="8e5c5-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e5c5-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8e5c5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8e5c5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e5c5-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e5c5-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8e5c5-137">IID</span><span class="sxs-lookup"><span data-stu-id="8e5c5-137">IID</span></span><br/>                      | <span data-ttu-id="8e5c5-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="8e5c5-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e5c5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e5c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5c5-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="8e5c5-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="8e5c5-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8e5c5-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="8e5c5-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="8e5c5-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





