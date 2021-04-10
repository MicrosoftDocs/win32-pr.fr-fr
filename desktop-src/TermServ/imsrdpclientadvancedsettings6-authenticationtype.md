---
title: IMsRdpClientAdvancedSettings6 AuthenticationType, propriété
description: Spécifie le type d’authentification utilisé pour cette connexion.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Propriété AuthenticationType Services Bureau à distance
- AuthenticationType, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings6, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété AuthenticationType
- AuthenticationType, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings7, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AuthenticationType
- AuthenticationType, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings8, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103690"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a><span data-ttu-id="31fbf-110">IMsRdpClientAdvancedSettings6 :: AuthenticationType, propriété</span><span class="sxs-lookup"><span data-stu-id="31fbf-110">IMsRdpClientAdvancedSettings6::AuthenticationType property</span></span>

<span data-ttu-id="31fbf-111">Spécifie le type d’authentification utilisé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="31fbf-111">Specifies the type of authentication used for this connection.</span></span>

<span data-ttu-id="31fbf-112">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="31fbf-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="31fbf-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31fbf-113">Syntax</span></span>


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a><span data-ttu-id="31fbf-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="31fbf-114">Property value</span></span>

<span data-ttu-id="31fbf-115">Reçoit une valeur qui spécifie le type d’authentification utilisé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="31fbf-115">Receives a value that specifies the type of authentication used for this connection.</span></span> <span data-ttu-id="31fbf-116">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="31fbf-116">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="31fbf-117">0</span><span class="sxs-lookup"><span data-stu-id="31fbf-117">0</span></span>
</dt> <dd>

<span data-ttu-id="31fbf-118">Aucune authentification n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="31fbf-118">No authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="31fbf-119">1</span><span class="sxs-lookup"><span data-stu-id="31fbf-119">1</span></span>
</dt> <dd>

<span data-ttu-id="31fbf-120">L’authentification par certificat est utilisée.</span><span class="sxs-lookup"><span data-stu-id="31fbf-120">Certificate authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="31fbf-121">2</span><span class="sxs-lookup"><span data-stu-id="31fbf-121">2</span></span>
</dt> <dd>

<span data-ttu-id="31fbf-122">L’authentification Kerberos est utilisée.</span><span class="sxs-lookup"><span data-stu-id="31fbf-122">Kerberos authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="31fbf-123">3</span><span class="sxs-lookup"><span data-stu-id="31fbf-123">3</span></span>
</dt> <dd>

<span data-ttu-id="31fbf-124">Le certificat et l’authentification Kerberos sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="31fbf-124">Both certificate and Kerberos authentication are used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31fbf-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31fbf-125">Requirements</span></span>



| <span data-ttu-id="31fbf-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31fbf-126">Requirement</span></span> | <span data-ttu-id="31fbf-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="31fbf-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31fbf-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31fbf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="31fbf-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31fbf-129">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="31fbf-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31fbf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="31fbf-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31fbf-131">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="31fbf-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="31fbf-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="31fbf-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31fbf-133"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="31fbf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="31fbf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31fbf-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31fbf-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="31fbf-136">IID</span><span class="sxs-lookup"><span data-stu-id="31fbf-136">IID</span></span><br/>                      | <span data-ttu-id="31fbf-137">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="31fbf-137">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31fbf-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31fbf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fbf-139">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="31fbf-139">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="31fbf-140">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="31fbf-140">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="31fbf-141">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="31fbf-141">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





