---
title: IMsRdpClientAdvancedSettings3 propriété ConnectionBarShowRestoreButton
description: Spécifie s’il faut afficher le bouton restaurer sur la barre de connexion.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectionBarShowRestoreButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384039"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a><span data-ttu-id="62564-116">IMsRdpClientAdvancedSettings3 :: ConnectionBarShowRestoreButton, propriété</span><span class="sxs-lookup"><span data-stu-id="62564-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowRestoreButton property</span></span>

<span data-ttu-id="62564-117">Spécifie s’il faut afficher le bouton **restaurer** sur la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="62564-117">Specifies whether to display the **Restore** button on the connection bar.</span></span>

<span data-ttu-id="62564-118">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="62564-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="62564-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62564-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a><span data-ttu-id="62564-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="62564-120">Property value</span></span>

<span data-ttu-id="62564-121">Affectez la valeur **Variant \_ true** pour afficher le bouton **restaurer** et la valeur false à la valeur **\_ false** pour désactiver l’affichage du bouton **restaurer** .</span><span class="sxs-lookup"><span data-stu-id="62564-121">Set to **VARIANT\_TRUE** to display the **Restore** button, and to **VARIANT\_FALSE** to disable the display of the **Restore** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62564-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="62564-122">Error codes</span></span>

<span data-ttu-id="62564-123">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="62564-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="62564-124">Notes</span><span class="sxs-lookup"><span data-stu-id="62564-124">Remarks</span></span>

<span data-ttu-id="62564-125">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="62564-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="62564-126">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="62564-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62564-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62564-127">Requirements</span></span>



| <span data-ttu-id="62564-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62564-128">Requirement</span></span> | <span data-ttu-id="62564-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="62564-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62564-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62564-130">Minimum supported client</span></span><br/> | <span data-ttu-id="62564-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62564-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="62564-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62564-132">Minimum supported server</span></span><br/> | <span data-ttu-id="62564-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62564-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="62564-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="62564-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="62564-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62564-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="62564-136">DLL</span><span class="sxs-lookup"><span data-stu-id="62564-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62564-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62564-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="62564-138">IID</span><span class="sxs-lookup"><span data-stu-id="62564-138">IID</span></span><br/>                      | <span data-ttu-id="62564-139">IID \_ IMsRdpClientAdvancedSettings3 est défini en tant que 19cd856b-c542-4c53-acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="62564-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62564-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62564-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62564-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="62564-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="62564-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="62564-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="62564-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="62564-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="62564-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="62564-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="62564-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="62564-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="62564-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="62564-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





