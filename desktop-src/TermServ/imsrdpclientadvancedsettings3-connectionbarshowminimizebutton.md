---
title: IMsRdpClientAdvancedSettings3 propriété ConnectionBarShowMinimizeButton
description: Spécifie s’il faut afficher le bouton réduire sur la barre de connexion.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectionBarShowMinimizeButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740012"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a><span data-ttu-id="9eead-116">IMsRdpClientAdvancedSettings3 :: ConnectionBarShowMinimizeButton, propriété</span><span class="sxs-lookup"><span data-stu-id="9eead-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton property</span></span>

<span data-ttu-id="9eead-117">Spécifie s’il faut afficher le bouton **réduire** sur la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="9eead-117">Specifies whether to display the **Minimize** button on the connection bar.</span></span>

<span data-ttu-id="9eead-118">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9eead-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eead-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eead-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a><span data-ttu-id="9eead-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9eead-120">Property value</span></span>

<span data-ttu-id="9eead-121">Affectez à ce paramètre la **\_ valeur variant true** pour afficher le bouton **réduire** et la **\_ valeur false à false** pour désactiver l’affichage du bouton **réduire** .</span><span class="sxs-lookup"><span data-stu-id="9eead-121">Set this parameter to **VARIANT\_TRUE** to display the **Minimize** button, and to **VARIANT\_FALSE** to disable the display of the **Minimize** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9eead-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9eead-122">Error codes</span></span>

<span data-ttu-id="9eead-123">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9eead-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eead-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9eead-124">Remarks</span></span>

<span data-ttu-id="9eead-125">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="9eead-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="9eead-126">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9eead-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9eead-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eead-127">Requirements</span></span>



| <span data-ttu-id="9eead-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eead-128">Requirement</span></span> | <span data-ttu-id="9eead-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eead-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eead-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eead-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9eead-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9eead-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="9eead-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eead-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9eead-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eead-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="9eead-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9eead-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="9eead-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eead-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9eead-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9eead-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eead-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eead-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9eead-138">IID</span><span class="sxs-lookup"><span data-stu-id="9eead-138">IID</span></span><br/>                      | <span data-ttu-id="9eead-139">IID \_ IMsRdpClientAdvancedSettings3 est défini en tant que 19cd856b-c542-4c53-acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="9eead-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9eead-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eead-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eead-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9eead-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9eead-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9eead-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9eead-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9eead-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9eead-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9eead-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9eead-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9eead-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9eead-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9eead-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





