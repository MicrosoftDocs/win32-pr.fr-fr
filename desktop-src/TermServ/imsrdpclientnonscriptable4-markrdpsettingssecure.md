---
title: IMsRdpClientNonScriptable4 propriété MarkRdpSettingsSecure
description: Spécifie si les paramètres de protocole RDP (Remote Desktop Protocol) (RDP) sont marqués comme sécurisés.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété MarkRdpSettingsSecure
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508766"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a><span data-ttu-id="87c1b-116">IMsRdpClientNonScriptable4 :: MarkRdpSettingsSecure, propriété</span><span class="sxs-lookup"><span data-stu-id="87c1b-116">IMsRdpClientNonScriptable4::MarkRdpSettingsSecure property</span></span>

<span data-ttu-id="87c1b-117">Spécifie si les paramètres de [protocole RDP (Remote Desktop Protocol)](remote-desktop-protocol.md) (RDP) sont marqués comme sécurisés.</span><span class="sxs-lookup"><span data-stu-id="87c1b-117">Specifies whether [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) settings are marked as secure.</span></span> <span data-ttu-id="87c1b-118">Cela indique que les paramètres appliqués au contrôle ont été signés par un éditeur tiers ou approuvé.</span><span class="sxs-lookup"><span data-stu-id="87c1b-118">This indicates that the settings applied to the control have been signed by a third-party or trusted publisher.</span></span>

<span data-ttu-id="87c1b-119">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="87c1b-119">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c1b-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87c1b-120">Syntax</span></span>


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a><span data-ttu-id="87c1b-121">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="87c1b-121">Property value</span></span>

<span data-ttu-id="87c1b-122">Définit si les paramètres RDP sont marqués comme sécurisés.</span><span class="sxs-lookup"><span data-stu-id="87c1b-122">Sets whether RDP settings are marked as secure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="87c1b-123">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="87c1b-123">Error codes</span></span>

<span data-ttu-id="87c1b-124">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="87c1b-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="87c1b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87c1b-125">Requirements</span></span>



| <span data-ttu-id="87c1b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87c1b-126">Requirement</span></span> | <span data-ttu-id="87c1b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="87c1b-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87c1b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c1b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87c1b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87c1b-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="87c1b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c1b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87c1b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87c1b-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="87c1b-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="87c1b-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="87c1b-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87c1b-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="87c1b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="87c1b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87c1b-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87c1b-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="87c1b-136">IID</span><span class="sxs-lookup"><span data-stu-id="87c1b-136">IID</span></span><br/>                      | <span data-ttu-id="87c1b-137">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="87c1b-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87c1b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c1b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c1b-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="87c1b-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="87c1b-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="87c1b-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





