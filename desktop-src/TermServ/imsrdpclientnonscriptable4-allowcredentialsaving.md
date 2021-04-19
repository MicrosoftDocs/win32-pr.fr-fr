---
title: IMsRdpClientNonScriptable4 propriété AllowCredentialSaving
description: Spécifie si la boîte de dialogue informations d’identification affiche une case à cocher qui active l’enregistrement des informations d’identification.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AllowCredentialSaving
- Services Bureau à distance de la propriété AllowCredentialSaving, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété AllowCredentialSaving
- Services Bureau à distance de la propriété AllowCredentialSaving, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété AllowCredentialSaving
- Services Bureau à distance de la propriété AllowCredentialSaving, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété AllowCredentialSaving
- Services Bureau à distance de la propriété AllowCredentialSaving, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété AllowCredentialSaving
- Services Bureau à distance de la propriété AllowCredentialSaving, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété AllowCredentialSaving
- Services Bureau à distance de la propriété AllowCredentialSaving, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété AllowCredentialSaving
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513797"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a><span data-ttu-id="c7603-116">IMsRdpClientNonScriptable4 :: AllowCredentialSaving, propriété</span><span class="sxs-lookup"><span data-stu-id="c7603-116">IMsRdpClientNonScriptable4::AllowCredentialSaving property</span></span>

<span data-ttu-id="c7603-117">Spécifie si la boîte de dialogue informations d’identification affiche une case à cocher qui active l’enregistrement des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c7603-117">Specifies whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

<span data-ttu-id="c7603-118">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c7603-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7603-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7603-119">Syntax</span></span>


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a><span data-ttu-id="c7603-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c7603-120">Property value</span></span>

<span data-ttu-id="c7603-121">Définit si la boîte de dialogue informations d’identification affiche une case à cocher qui active l’enregistrement des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c7603-121">Sets whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c7603-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c7603-122">Error codes</span></span>

<span data-ttu-id="c7603-123">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="c7603-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7603-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7603-124">Requirements</span></span>



| <span data-ttu-id="c7603-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7603-125">Requirement</span></span> | <span data-ttu-id="c7603-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7603-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7603-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7603-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c7603-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7603-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c7603-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7603-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c7603-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7603-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c7603-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c7603-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7603-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7603-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="c7603-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c7603-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7603-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7603-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="c7603-135">IID</span><span class="sxs-lookup"><span data-stu-id="c7603-135">IID</span></span><br/>                      | <span data-ttu-id="c7603-136">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="c7603-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7603-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7603-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7603-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c7603-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c7603-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c7603-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





