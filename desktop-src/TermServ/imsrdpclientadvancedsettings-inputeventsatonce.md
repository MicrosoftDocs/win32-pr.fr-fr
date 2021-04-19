---
title: IMsRdpClientAdvancedSettings propriété InputEventsAtOnce
description: Cette propriété n'est pas prise en charge. | IMsRdpClientAdvancedSettings propriété InputEventsAtOnce
ms.assetid: 2f24b2cd-136d-4bde-9808-e5cb02bd7ce8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété InputEventsAtOnce
- Services Bureau à distance de la propriété InputEventsAtOnce, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété InputEventsAtOnce
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.InputEventsAtOnce
- IMsRdpClientAdvancedSettings.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.put_InputEventsAtOnce
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999d00cb706e4fdd4cf0c9ed606c33de4a81e8d6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538045"
---
# <a name="imsrdpclientadvancedsettingsinputeventsatonce-property"></a><span data-ttu-id="ed08f-121">IMsRdpClientAdvancedSettings :: InputEventsAtOnce, propriété</span><span class="sxs-lookup"><span data-stu-id="ed08f-121">IMsRdpClientAdvancedSettings::InputEventsAtOnce property</span></span>

<span data-ttu-id="ed08f-122">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ed08f-122">This property is not supported.</span></span>

<span data-ttu-id="ed08f-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ed08f-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed08f-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed08f-124">Syntax</span></span>


```C++
HRESULT put_InputEventsAtOnce(
  [in]  LONG inputEventsAtOnce
);

HRESULT get_InputEventsAtOnce(
  [out] LONG *pinputEventsAtOnce
);
```



## <a name="property-value"></a><span data-ttu-id="ed08f-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ed08f-125">Property value</span></span>

<span data-ttu-id="ed08f-126">Nouveau nombre d’événements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ed08f-126">The new number of input events.</span></span> <span data-ttu-id="ed08f-127">La valeur par défaut est de 10.</span><span class="sxs-lookup"><span data-stu-id="ed08f-127">The default is 10.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ed08f-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ed08f-128">Error codes</span></span>

<span data-ttu-id="ed08f-129">Retourne **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ed08f-129">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed08f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed08f-130">Requirements</span></span>



| <span data-ttu-id="ed08f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed08f-131">Requirement</span></span> | <span data-ttu-id="ed08f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed08f-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed08f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed08f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ed08f-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed08f-134">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ed08f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed08f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ed08f-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed08f-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ed08f-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ed08f-137">End of client support</span></span><br/>    | <span data-ttu-id="ed08f-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed08f-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ed08f-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ed08f-139">End of server support</span></span><br/>    | <span data-ttu-id="ed08f-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed08f-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ed08f-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ed08f-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed08f-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed08f-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ed08f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ed08f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed08f-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed08f-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ed08f-145">IID</span><span class="sxs-lookup"><span data-stu-id="ed08f-145">IID</span></span><br/>                      | <span data-ttu-id="ed08f-146">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ed08f-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed08f-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed08f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed08f-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ed08f-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ed08f-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ed08f-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ed08f-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ed08f-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ed08f-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ed08f-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ed08f-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ed08f-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ed08f-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ed08f-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ed08f-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ed08f-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ed08f-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ed08f-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





