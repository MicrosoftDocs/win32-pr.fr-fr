---
title: IMsRdpClientAdvancedSettings propriété SmoothScroll
description: Cette propriété n'est pas prise en charge. | IMsRdpClientAdvancedSettings propriété SmoothScroll
ms.assetid: 7f1ce439-0b6e-4426-8dd6-3748509130e1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété SmoothScroll
- Services Bureau à distance de la propriété SmoothScroll, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété SmoothScroll
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmoothScroll
- IMsRdpClientAdvancedSettings.get_SmoothScroll
- IMsRdpClientAdvancedSettings.put_SmoothScroll
- IMsRdpClientAdvancedSettings2.SmoothScroll
- IMsRdpClientAdvancedSettings2.get_SmoothScroll
- IMsRdpClientAdvancedSettings2.put_SmoothScroll
- IMsRdpClientAdvancedSettings3.SmoothScroll
- IMsRdpClientAdvancedSettings3.get_SmoothScroll
- IMsRdpClientAdvancedSettings3.put_SmoothScroll
- IMsRdpClientAdvancedSettings4.SmoothScroll
- IMsRdpClientAdvancedSettings4.get_SmoothScroll
- IMsRdpClientAdvancedSettings4.put_SmoothScroll
- IMsRdpClientAdvancedSettings5.SmoothScroll
- IMsRdpClientAdvancedSettings5.get_SmoothScroll
- IMsRdpClientAdvancedSettings5.put_SmoothScroll
- IMsRdpClientAdvancedSettings6.SmoothScroll
- IMsRdpClientAdvancedSettings6.get_SmoothScroll
- IMsRdpClientAdvancedSettings6.put_SmoothScroll
- IMsRdpClientAdvancedSettings7.SmoothScroll
- IMsRdpClientAdvancedSettings7.get_SmoothScroll
- IMsRdpClientAdvancedSettings7.put_SmoothScroll
- IMsRdpClientAdvancedSettings8.SmoothScroll
- IMsRdpClientAdvancedSettings8.get_SmoothScroll
- IMsRdpClientAdvancedSettings8.put_SmoothScroll
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62be8fe85415792116c23b4e12d9ab56fb89e0f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106520286"
---
# <a name="imsrdpclientadvancedsettingssmoothscroll-property"></a><span data-ttu-id="9a973-121">IMsRdpClientAdvancedSettings :: SmoothScroll, propriété</span><span class="sxs-lookup"><span data-stu-id="9a973-121">IMsRdpClientAdvancedSettings::SmoothScroll property</span></span>

<span data-ttu-id="9a973-122">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9a973-122">This property is not supported.</span></span>

<span data-ttu-id="9a973-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9a973-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a973-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a973-124">Syntax</span></span>


```C++
HRESULT put_SmoothScroll(
  [in]  LONG smoothScroll
);

HRESULT get_SmoothScroll(
  [out] LONG *psmoothScroll
);
```



## <a name="property-value"></a><span data-ttu-id="9a973-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a973-125">Property value</span></span>

<span data-ttu-id="9a973-126">Affectez à ce paramètre la valeur 0 pour désactiver le défilement régulier ou une valeur différente de zéro pour permettre le défilement lissé.</span><span class="sxs-lookup"><span data-stu-id="9a973-126">Set this parameter to 0 to disable smooth scrolling or a nonzero value to enable smooth scrolling.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a973-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9a973-127">Error codes</span></span>

<span data-ttu-id="9a973-128">Retourne **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="9a973-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a973-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a973-129">Requirements</span></span>



| <span data-ttu-id="9a973-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a973-130">Requirement</span></span> | <span data-ttu-id="9a973-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a973-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a973-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a973-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9a973-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a973-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9a973-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a973-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9a973-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a973-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9a973-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9a973-136">End of client support</span></span><br/>    | <span data-ttu-id="9a973-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a973-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9a973-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9a973-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a973-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a973-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9a973-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9a973-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a973-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a973-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9a973-142">IID</span><span class="sxs-lookup"><span data-stu-id="9a973-142">IID</span></span><br/>                      | <span data-ttu-id="9a973-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9a973-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a973-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a973-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a973-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9a973-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9a973-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9a973-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9a973-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9a973-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9a973-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9a973-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9a973-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9a973-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9a973-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9a973-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9a973-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9a973-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9a973-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9a973-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





