---
title: IMsRdpClientNonScriptable4 propriété PromptForCredsOnClient
description: Spécifie si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384895"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a><span data-ttu-id="bb9da-116">IMsRdpClientNonScriptable4 ::P propriété romptForCredsOnClient</span><span class="sxs-lookup"><span data-stu-id="bb9da-116">IMsRdpClientNonScriptable4::PromptForCredsOnClient property</span></span>

<span data-ttu-id="bb9da-117">Spécifie si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="bb9da-117">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span>

<span data-ttu-id="bb9da-118">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bb9da-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9da-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb9da-119">Syntax</span></span>


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a><span data-ttu-id="bb9da-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bb9da-120">Property value</span></span>

<span data-ttu-id="bb9da-121">Définit si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="bb9da-121">Sets whether the client control displays a dialog box that prompts for credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb9da-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="bb9da-122">Error codes</span></span>

<span data-ttu-id="bb9da-123">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="bb9da-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb9da-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb9da-124">Requirements</span></span>



| <span data-ttu-id="bb9da-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb9da-125">Requirement</span></span> | <span data-ttu-id="bb9da-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb9da-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9da-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb9da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bb9da-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb9da-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bb9da-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb9da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bb9da-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb9da-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bb9da-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bb9da-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb9da-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb9da-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bb9da-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bb9da-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb9da-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb9da-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bb9da-135">IID</span><span class="sxs-lookup"><span data-stu-id="bb9da-135">IID</span></span><br/>                      | <span data-ttu-id="bb9da-136">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="bb9da-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb9da-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb9da-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9da-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="bb9da-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="bb9da-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="bb9da-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





