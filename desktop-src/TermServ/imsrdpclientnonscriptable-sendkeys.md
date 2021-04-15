---
title: IMsRdpClientNonScriptable SendKeys, méthode
description: Envoie une série de séquences de touches au contrôle. Les séquences de touches sont sous forme de code d’analyse, c’est-à-dire les données de clavier des véritables clés physiques.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- SendKeys, méthode Services Bureau à distance
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable2, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable3, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable4, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable5, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, méthode SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466007"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a><span data-ttu-id="6c85e-115">IMsRdpClientNonScriptable :: SendKeys, méthode</span><span class="sxs-lookup"><span data-stu-id="6c85e-115">IMsRdpClientNonScriptable::SendKeys method</span></span>

<span data-ttu-id="6c85e-116">Envoie une série de séquences de touches au contrôle.</span><span class="sxs-lookup"><span data-stu-id="6c85e-116">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="6c85e-117">Les séquences de touches sont sous forme de code d’analyse, c’est-à-dire les données de clavier des véritables clés physiques.</span><span class="sxs-lookup"><span data-stu-id="6c85e-117">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c85e-118">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c85e-118">Syntax</span></span>


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="6c85e-119">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c85e-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c85e-120">*numKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c85e-120">*numKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c85e-121">Nombre de séquences de touches à envoyer.</span><span class="sxs-lookup"><span data-stu-id="6c85e-121">The number of keystrokes to send.</span></span> <span data-ttu-id="6c85e-122">Le nombre maximal de clés qui peuvent être envoyées en une seule opération est de 20.</span><span class="sxs-lookup"><span data-stu-id="6c85e-122">The maximum number of keys that can be sent in one operation is 20.</span></span> <span data-ttu-id="6c85e-123">La méthode retourne **E \_ INVALIDARG** si ce paramètre est supérieur à 20.</span><span class="sxs-lookup"><span data-stu-id="6c85e-123">The method returns **E\_INVALIDARG** if this parameter is greater than 20.</span></span> <span data-ttu-id="6c85e-124">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="6c85e-124">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="6c85e-125">*pbArrayKeyUp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c85e-125">*pbArrayKeyUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c85e-126">Tableau dont la taille est égale à *numKeys*.</span><span class="sxs-lookup"><span data-stu-id="6c85e-126">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="6c85e-127">Un élément a la **valeur true** si la touche correspondante est active et **false** si la touche correspondante est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="6c85e-127">An element is **TRUE** if the corresponding key is UP and **FALSE** if the corresponding key is DOWN.</span></span>

</dd> <dt>

<span data-ttu-id="6c85e-128">*plKeyData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c85e-128">*plKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c85e-129">Tableau dont la taille est égale à *numKeys*.</span><span class="sxs-lookup"><span data-stu-id="6c85e-129">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="6c85e-130">Le tableau contient des données de séquence de touches et correspond à la valeur du paramètre *lParam* du message [WM \_](../inputdev/wm-keydown.md) KeyOut.</span><span class="sxs-lookup"><span data-stu-id="6c85e-130">The array contains keystroke data and corresponds to the value of the *lParam* parameter of the [WM\_KEYDOWN](../inputdev/wm-keydown.md) message.</span></span> <span data-ttu-id="6c85e-131">Les données spécifient le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition.</span><span class="sxs-lookup"><span data-stu-id="6c85e-131">The data specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span> <span data-ttu-id="6c85e-132">Pour obtenir une description des bits de ce tableau, consultez [WM \_ keydescendant](../inputdev/wm-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="6c85e-132">For a description of the bits in this array, see [WM\_KEYDOWN](../inputdev/wm-keydown.md).</span></span>

<span data-ttu-id="6c85e-133">L’élément correspondant dans *pbArrayKeyUp* indique si la touche est vers le haut ou vers le haut.</span><span class="sxs-lookup"><span data-stu-id="6c85e-133">The corresponding element in *pbArrayKeyUp* indicates if the key is UP or DOWN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c85e-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c85e-134">Return value</span></span>

<span data-ttu-id="6c85e-135">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="6c85e-135">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c85e-136">Notes</span><span class="sxs-lookup"><span data-stu-id="6c85e-136">Remarks</span></span>

<span data-ttu-id="6c85e-137">La méthode **SendKeys** ne mélange pas les séquences de touches effectuées par l’utilisateur local avec les séquences de touches que la méthode envoie.</span><span class="sxs-lookup"><span data-stu-id="6c85e-137">The **SendKeys** method does not mix keystrokes made by the local user with keystrokes that the method is sending.</span></span> <span data-ttu-id="6c85e-138">Toutes les séquences de touches passées à la méthode sont envoyées à la session distante dans une seule séquence atomique.</span><span class="sxs-lookup"><span data-stu-id="6c85e-138">All keystrokes passed to the method are sent to the remote session in a single atomic sequence.</span></span>

<span data-ttu-id="6c85e-139">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6c85e-139">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c85e-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c85e-140">Requirements</span></span>



| <span data-ttu-id="6c85e-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c85e-141">Requirement</span></span> | <span data-ttu-id="6c85e-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c85e-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c85e-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c85e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6c85e-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c85e-144">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="6c85e-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c85e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6c85e-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c85e-146">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="6c85e-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6c85e-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c85e-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c85e-148"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="6c85e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6c85e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c85e-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c85e-150"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="6c85e-151">IID</span><span class="sxs-lookup"><span data-stu-id="6c85e-151">IID</span></span><br/>                      | <span data-ttu-id="6c85e-152">IID \_ IMsRdpClientNonScriptable est défini en tant que 2f079c4c-87B2-4AFD-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="6c85e-152">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c85e-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c85e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c85e-154">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="6c85e-154">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="6c85e-155">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="6c85e-155">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="6c85e-156">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6c85e-156">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="6c85e-157">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6c85e-157">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6c85e-158">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="6c85e-158">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="6c85e-159">WM- \_ touche</span><span class="sxs-lookup"><span data-stu-id="6c85e-159">WM\_KEYDOWN</span></span>](../inputdev/wm-keydown.md)
</dt> </dl>

 

