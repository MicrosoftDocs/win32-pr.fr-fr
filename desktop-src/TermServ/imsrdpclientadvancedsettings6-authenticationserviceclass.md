---
title: IMsRdpClientAdvancedSettings6 propriété AuthenticationServiceClass
description: Spécifie le nom de principal du service (SPN) à utiliser pour l’authentification auprès du serveur.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AuthenticationServiceClass
- Services Bureau à distance de la propriété AuthenticationServiceClass, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété AuthenticationServiceClass
- Services Bureau à distance de la propriété AuthenticationServiceClass, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AuthenticationServiceClass
- Services Bureau à distance de la propriété AuthenticationServiceClass, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AuthenticationServiceClass
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741517"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a><span data-ttu-id="6d912-110">IMsRdpClientAdvancedSettings6 :: AuthenticationServiceClass, propriété</span><span class="sxs-lookup"><span data-stu-id="6d912-110">IMsRdpClientAdvancedSettings6::AuthenticationServiceClass property</span></span>

<span data-ttu-id="6d912-111">Spécifie le nom de principal du service (SPN) à utiliser pour l’authentification auprès du serveur.</span><span class="sxs-lookup"><span data-stu-id="6d912-111">Specifies the service principal name (SPN) to use for authentication to the server.</span></span>

<span data-ttu-id="6d912-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6d912-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d912-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d912-113">Syntax</span></span>


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a><span data-ttu-id="6d912-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6d912-114">Property value</span></span>

<span data-ttu-id="6d912-115">Spécifie le nom de principal du service à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6d912-115">Specifies the service principal name to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d912-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6d912-116">Remarks</span></span>

<span data-ttu-id="6d912-117">Cette propriété est uniquement prise en charge par les clients Connexion Bureau à distance 6,1 et 7,0.</span><span class="sxs-lookup"><span data-stu-id="6d912-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="6d912-118">Les noms de principal du service (SPN) sont associés au principal de sécurité (utilisateur ou groupes) dans le contexte de sécurité que le service exécute.</span><span class="sxs-lookup"><span data-stu-id="6d912-118">Service principal names (SPNs) are associated with the security principal (user or groups) in whose security context the service executes.</span></span> <span data-ttu-id="6d912-119">Les noms de principal du service sont utilisés pour prendre en charge l’authentification mutuelle entre une application cliente et un service.</span><span class="sxs-lookup"><span data-stu-id="6d912-119">SPNs are used to support mutual authentication between a client application and a service.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d912-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d912-120">Requirements</span></span>



| <span data-ttu-id="6d912-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d912-121">Requirement</span></span> | <span data-ttu-id="6d912-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d912-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d912-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d912-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d912-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d912-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="6d912-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d912-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d912-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d912-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="6d912-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6d912-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d912-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d912-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6d912-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6d912-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d912-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d912-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6d912-131">IID</span><span class="sxs-lookup"><span data-stu-id="6d912-131">IID</span></span><br/>                      | <span data-ttu-id="6d912-132">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="6d912-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d912-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d912-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d912-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6d912-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6d912-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6d912-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6d912-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6d912-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





