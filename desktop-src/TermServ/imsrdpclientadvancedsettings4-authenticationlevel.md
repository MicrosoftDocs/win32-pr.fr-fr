---
title: IMsRdpClientAdvancedSettings4 propriété AuthenticationLevel
description: Spécifie le niveau d’authentification à utiliser pour la connexion.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AuthenticationLevel
- Services Bureau à distance de la propriété AuthenticationLevel, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété AuthenticationLevel
- Services Bureau à distance de la propriété AuthenticationLevel, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété AuthenticationLevel
- Services Bureau à distance de la propriété AuthenticationLevel, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété AuthenticationLevel
- Services Bureau à distance de la propriété AuthenticationLevel, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AuthenticationLevel
- Services Bureau à distance de la propriété AuthenticationLevel, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AuthenticationLevel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843469"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a><span data-ttu-id="31c1b-114">IMsRdpClientAdvancedSettings4 :: AuthenticationLevel, propriété</span><span class="sxs-lookup"><span data-stu-id="31c1b-114">IMsRdpClientAdvancedSettings4::AuthenticationLevel property</span></span>

<span data-ttu-id="31c1b-115">Spécifie le niveau d’authentification à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="31c1b-115">Specifies the authentication level to use for the connection.</span></span>

<span data-ttu-id="31c1b-116">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="31c1b-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c1b-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31c1b-117">Syntax</span></span>


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a><span data-ttu-id="31c1b-118">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="31c1b-118">Property value</span></span>

<span data-ttu-id="31c1b-119">Valeur de la propriété **AuthenticationLevel** .</span><span class="sxs-lookup"><span data-stu-id="31c1b-119">The value of the **AuthenticationLevel** property.</span></span>

<dt>

<span data-ttu-id="31c1b-120">0</span><span class="sxs-lookup"><span data-stu-id="31c1b-120">0</span></span>
</dt> <dd>

<span data-ttu-id="31c1b-121">Aucune authentification du serveur.</span><span class="sxs-lookup"><span data-stu-id="31c1b-121">No authentication of the server.</span></span>

</dd> <dt>

<span data-ttu-id="31c1b-122">1</span><span class="sxs-lookup"><span data-stu-id="31c1b-122">1</span></span>
</dt> <dd>

<span data-ttu-id="31c1b-123">L’authentification du serveur est requise et doit se terminer avec succès pour que la connexion continue.</span><span class="sxs-lookup"><span data-stu-id="31c1b-123">Server authentication is required and must complete successfully for the connection to proceed.</span></span>

</dd> <dt>

<span data-ttu-id="31c1b-124">2</span><span class="sxs-lookup"><span data-stu-id="31c1b-124">2</span></span>
</dt> <dd>

<span data-ttu-id="31c1b-125">Tente d’authentifier le serveur.</span><span class="sxs-lookup"><span data-stu-id="31c1b-125">Attempt authentication of the server.</span></span> <span data-ttu-id="31c1b-126">Si l’authentification échoue, l’utilisateur est invité à annuler la connexion ou à continuer sans l’authentification du serveur.</span><span class="sxs-lookup"><span data-stu-id="31c1b-126">If authentication fails, the user will be prompted with the option to cancel the connection or to proceed without server authentication.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="31c1b-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="31c1b-127">Error codes</span></span>

<span data-ttu-id="31c1b-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="31c1b-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="31c1b-129">Notes</span><span class="sxs-lookup"><span data-stu-id="31c1b-129">Remarks</span></span>

<span data-ttu-id="31c1b-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="31c1b-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31c1b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31c1b-131">Requirements</span></span>



| <span data-ttu-id="31c1b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31c1b-132">Requirement</span></span> | <span data-ttu-id="31c1b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="31c1b-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c1b-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31c1b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="31c1b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31c1b-135">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="31c1b-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31c1b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="31c1b-137">Windows Server 2008, Windows Server 2008 avec SP1</span><span class="sxs-lookup"><span data-stu-id="31c1b-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="31c1b-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="31c1b-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="31c1b-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31c1b-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="31c1b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="31c1b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31c1b-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31c1b-141"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="31c1b-142">IID</span><span class="sxs-lookup"><span data-stu-id="31c1b-142">IID</span></span><br/>                      | <span data-ttu-id="31c1b-143">IID \_ IMsRdpClientAdvancedSettings4 est défini en tant que FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="31c1b-143">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31c1b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31c1b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c1b-145">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="31c1b-145">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="31c1b-146">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="31c1b-146">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="31c1b-147">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="31c1b-147">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="31c1b-148">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="31c1b-148">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="31c1b-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="31c1b-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





