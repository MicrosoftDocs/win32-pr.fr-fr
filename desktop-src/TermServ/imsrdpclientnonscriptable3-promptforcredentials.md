---
title: IMsRdpClientNonScriptable3, propriété PromptForCredentials (wuapi. h)
description: Spécifie ou récupère une valeur indiquant si la boîte de dialogue demander les informations d’identification est activée pour la connexion.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- Propriété PromptForCredentials Services Bureau à distance
- Propriété PromptForCredentials Services Bureau à distance, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient5
- Objet MsRdpClient5 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient6
- Objet MsRdpClient6 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient7
- Objet MsRdpClient7 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient8
- Objet MsRdpClient8 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient9
- Objet MsRdpClient9 Services Bureau à distance, propriété PromptForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317125"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a><span data-ttu-id="ebfe7-120">IMsRdpClientNonScriptable3 ::P propriété romptForCredentials</span><span class="sxs-lookup"><span data-stu-id="ebfe7-120">IMsRdpClientNonScriptable3::PromptForCredentials property</span></span>

<span data-ttu-id="ebfe7-121">Spécifie ou récupère une valeur indiquant si la boîte de dialogue demander les informations d’identification est activée pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="ebfe7-121">Specifies or retrieves whether the prompt for credentials dialog is enabled for the connection.</span></span>

<span data-ttu-id="ebfe7-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ebfe7-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfe7-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebfe7-123">Syntax</span></span>


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a><span data-ttu-id="ebfe7-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ebfe7-124">Property value</span></span>

<span data-ttu-id="ebfe7-125">Spécifie si la boîte de dialogue demander les informations d’identification est activée pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="ebfe7-125">Specifies whether the prompt for credentials dialog is enabled for the connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ebfe7-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ebfe7-126">Error codes</span></span>

## <a name="requirements"></a><span data-ttu-id="ebfe7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebfe7-127">Requirements</span></span>



| <span data-ttu-id="ebfe7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebfe7-128">Requirement</span></span> | <span data-ttu-id="ebfe7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebfe7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfe7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebfe7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ebfe7-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebfe7-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ebfe7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebfe7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ebfe7-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebfe7-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ebfe7-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebfe7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebfe7-135"><dt>Wuapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebfe7-135"><dt>Wuapi.h</dt></span></span> </dl>            |
| <span data-ttu-id="ebfe7-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ebfe7-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebfe7-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebfe7-137"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ebfe7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ebfe7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebfe7-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebfe7-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ebfe7-140">IID</span><span class="sxs-lookup"><span data-stu-id="ebfe7-140">IID</span></span><br/>                      | <span data-ttu-id="ebfe7-141">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="ebfe7-141">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebfe7-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebfe7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfe7-143">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ebfe7-143">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="ebfe7-144">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ebfe7-144">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ebfe7-145">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="ebfe7-145">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





