---
title: IMsRdpClientNonScriptable4 propriété RedirectionWarningType
description: Contrôle la présence et l’apparence de la boîte de dialogue qui avertit l’utilisateur de la redirection.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectionWarningType
- Services Bureau à distance de la propriété RedirectionWarningType, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété RedirectionWarningType
- Services Bureau à distance de la propriété RedirectionWarningType, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété RedirectionWarningType
- Services Bureau à distance de la propriété RedirectionWarningType, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété RedirectionWarningType
- Services Bureau à distance de la propriété RedirectionWarningType, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété RedirectionWarningType
- Services Bureau à distance de la propriété RedirectionWarningType, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété RedirectionWarningType
- Services Bureau à distance de la propriété RedirectionWarningType, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété RedirectionWarningType
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511371"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a><span data-ttu-id="64ae6-116">IMsRdpClientNonScriptable4 :: RedirectionWarningType, propriété</span><span class="sxs-lookup"><span data-stu-id="64ae6-116">IMsRdpClientNonScriptable4::RedirectionWarningType property</span></span>

<span data-ttu-id="64ae6-117">Contrôle la présence et l’apparence de la boîte de dialogue qui avertit l’utilisateur de la redirection.</span><span class="sxs-lookup"><span data-stu-id="64ae6-117">Controls the presence and appearance of the dialog box that notifies the user about redirection.</span></span>

<span data-ttu-id="64ae6-118">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="64ae6-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ae6-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64ae6-119">Syntax</span></span>


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a><span data-ttu-id="64ae6-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="64ae6-120">Property value</span></span>

<span data-ttu-id="64ae6-121">Définit le type de la boîte de dialogue qui notifie l’utilisateur de la redirection.</span><span class="sxs-lookup"><span data-stu-id="64ae6-121">Sets the type of the dialog box that notifies the user of redirection.</span></span>

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span data-ttu-id="64ae6-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="64ae6-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="64ae6-123">La boîte de dialogue n’est pas spécifique de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="64ae6-123">The dialog box is not publisher specific.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span data-ttu-id="64ae6-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="64ae6-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="64ae6-125">La boîte de dialogue est pour les fichiers non signés.</span><span class="sxs-lookup"><span data-stu-id="64ae6-125">The dialog box is for unsigned files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span data-ttu-id="64ae6-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="64ae6-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="64ae6-127">La boîte de dialogue est destinée à un serveur de publication inconnu.</span><span class="sxs-lookup"><span data-stu-id="64ae6-127">The dialog box is for an unknown publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span data-ttu-id="64ae6-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span><span class="sxs-lookup"><span data-stu-id="64ae6-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span></span>


</dt> <dd>

<span data-ttu-id="64ae6-129">La boîte de dialogue est destinée aux fichiers de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64ae6-129">The dialog box is for the user's files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span data-ttu-id="64ae6-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="64ae6-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span></span>


</dt> <dd>

<span data-ttu-id="64ae6-131">La boîte de dialogue s’affiche pour les fichiers signés par des tiers.</span><span class="sxs-lookup"><span data-stu-id="64ae6-131">The dialog box is displayed for third-party-certified, signed files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span data-ttu-id="64ae6-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="64ae6-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="64ae6-133">La boîte de dialogue n’est pas affichée, car l’application est publiée par un éditeur approuvé.</span><span class="sxs-lookup"><span data-stu-id="64ae6-133">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span data-ttu-id="64ae6-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="64ae6-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="64ae6-135">La boîte de dialogue n’est pas affichée, car l’application est publiée par un éditeur approuvé.</span><span class="sxs-lookup"><span data-stu-id="64ae6-135">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="64ae6-136">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="64ae6-136">Error codes</span></span>

<span data-ttu-id="64ae6-137">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="64ae6-137">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ae6-138">Notes</span><span class="sxs-lookup"><span data-stu-id="64ae6-138">Remarks</span></span>

<span data-ttu-id="64ae6-139">La valeur **RedirectionWarningTypeDefault**, qui est la valeur par défaut de cette propriété, n’exerce aucun contrôle sur la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="64ae6-139">The value **RedirectionWarningTypeDefault**, which is the default value of this property, exerts no control over the dialog box.</span></span> <span data-ttu-id="64ae6-140">Dans ce cas, la propriété de contrôle est [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) dans [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span><span class="sxs-lookup"><span data-stu-id="64ae6-140">The controlling property in this case is [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64ae6-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64ae6-141">Requirements</span></span>



| <span data-ttu-id="64ae6-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64ae6-142">Requirement</span></span> | <span data-ttu-id="64ae6-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="64ae6-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64ae6-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64ae6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="64ae6-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64ae6-145">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="64ae6-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64ae6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="64ae6-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64ae6-147">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="64ae6-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="64ae6-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="64ae6-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64ae6-149"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="64ae6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="64ae6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64ae6-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64ae6-151"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="64ae6-152">IID</span><span class="sxs-lookup"><span data-stu-id="64ae6-152">IID</span></span><br/>                      | <span data-ttu-id="64ae6-153">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="64ae6-153">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64ae6-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64ae6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ae6-155">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="64ae6-155">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="64ae6-156">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="64ae6-156">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





