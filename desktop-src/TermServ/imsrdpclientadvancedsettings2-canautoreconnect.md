---
title: IMsRdpClientAdvancedSettings2 propriété CanAutoReconnect
description: Spécifie si le contrôle client peut se reconnecter automatiquement à la session active en cas de déconnexion réseau.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CanAutoReconnect
- Services Bureau à distance de la propriété CanAutoReconnect, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété CanAutoReconnect
- Services Bureau à distance de la propriété CanAutoReconnect, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété CanAutoReconnect
- Services Bureau à distance de la propriété CanAutoReconnect, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété CanAutoReconnect
- Services Bureau à distance de la propriété CanAutoReconnect, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété CanAutoReconnect
- Services Bureau à distance de la propriété CanAutoReconnect, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété CanAutoReconnect
- Services Bureau à distance de la propriété CanAutoReconnect, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété CanAutoReconnect
- Services Bureau à distance de la propriété CanAutoReconnect, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété CanAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843109"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a><span data-ttu-id="8bd13-118">IMsRdpClientAdvancedSettings2 :: CanAutoReconnect, propriété</span><span class="sxs-lookup"><span data-stu-id="8bd13-118">IMsRdpClientAdvancedSettings2::CanAutoReconnect property</span></span>

<span data-ttu-id="8bd13-119">Spécifie si le contrôle client peut se reconnecter automatiquement à la session active en cas de déconnexion réseau.</span><span class="sxs-lookup"><span data-stu-id="8bd13-119">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span>

<span data-ttu-id="8bd13-120">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8bd13-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd13-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bd13-121">Syntax</span></span>


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="8bd13-122">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8bd13-122">Property value</span></span>

<span data-ttu-id="8bd13-123">Reçoit **la \_ valeur variant true** si le contrôle est en mesure de se reconnecter automatiquement et la **\_ valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8bd13-123">Receives **VARIANT\_TRUE** if the control is able to automatically reconnect, and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8bd13-124">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8bd13-124">Error codes</span></span>

<span data-ttu-id="8bd13-125">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="8bd13-125">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bd13-126">Notes</span><span class="sxs-lookup"><span data-stu-id="8bd13-126">Remarks</span></span>

<span data-ttu-id="8bd13-127">Les situations dans lesquelles la reconnexion automatique n’est peut-être pas activée incluent celles dans lesquelles un administrateur utilise une stratégie de groupe pour désactiver les reconnexion automatique et les environnements hérités qui ne prennent pas en charge la reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="8bd13-127">Situations in which automatic reconnection might not be enabled include those in which an administrator uses group policy to disable autoreconnection, and legacy environments that do not support automatic reconnection.</span></span>

<span data-ttu-id="8bd13-128">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="8bd13-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="8bd13-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8bd13-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd13-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bd13-130">Requirements</span></span>



| <span data-ttu-id="8bd13-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bd13-131">Requirement</span></span> | <span data-ttu-id="8bd13-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bd13-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd13-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bd13-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd13-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bd13-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="8bd13-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bd13-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd13-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bd13-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="8bd13-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8bd13-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="8bd13-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bd13-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8bd13-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8bd13-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bd13-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bd13-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8bd13-141">IID</span><span class="sxs-lookup"><span data-stu-id="8bd13-141">IID</span></span><br/>                      | <span data-ttu-id="8bd13-142">IID \_ IMsRdpClientAdvancedSettings2 est défini en tant que 9ac42117-2b76-4320-AA44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="8bd13-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bd13-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bd13-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd13-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="8bd13-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8bd13-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="8bd13-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="8bd13-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="8bd13-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="8bd13-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8bd13-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="8bd13-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8bd13-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8bd13-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8bd13-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8bd13-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="8bd13-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





