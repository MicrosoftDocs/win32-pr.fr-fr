---
title: Méthode SetName de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit un nouveau nom pour cette stratégie d’autorisation des connexions Bureau à distance (RD \ 160 ; CAP).
ms.assetid: 4a3b71d4-9b1c-46ea-b14a-fcbe32af37b5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetName
- Services Bureau à distance de la méthode SetName, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15fa4c374f5686f8cddbe99b5a464e6f84b4a12a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741284"
---
# <a name="setname-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="63b50-106">Méthode SetName de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="63b50-106">SetName method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="63b50-107">Définit un nouveau nom pour cette stratégie d’autorisation des connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="63b50-107">Sets a new name for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="63b50-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63b50-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="63b50-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63b50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b50-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63b50-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63b50-111">Nom de la stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="63b50-111">Name of the RD CAP.</span></span> <span data-ttu-id="63b50-112">Le nom doit comporter 64 caractères ou moins, unique (la casse est ignorée) et ne peut pas contenir les caractères réservés suivants :</span><span class="sxs-lookup"><span data-stu-id="63b50-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="63b50-113"><>  :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="63b50-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="63b50-114">\*\[Onglet\]</span><span class="sxs-lookup"><span data-stu-id="63b50-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b50-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63b50-115">Return value</span></span>

<span data-ttu-id="63b50-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="63b50-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="63b50-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="63b50-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="63b50-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="63b50-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="63b50-119">Notes</span><span class="sxs-lookup"><span data-stu-id="63b50-119">Remarks</span></span>

<span data-ttu-id="63b50-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="63b50-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="63b50-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="63b50-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="63b50-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="63b50-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="63b50-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="63b50-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="63b50-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="63b50-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="63b50-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63b50-125">Requirements</span></span>



| <span data-ttu-id="63b50-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63b50-126">Requirement</span></span> | <span data-ttu-id="63b50-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="63b50-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b50-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63b50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63b50-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="63b50-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="63b50-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63b50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63b50-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63b50-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="63b50-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63b50-132">Namespace</span></span><br/>                | <span data-ttu-id="63b50-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="63b50-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="63b50-134">MOF</span><span class="sxs-lookup"><span data-stu-id="63b50-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63b50-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63b50-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="63b50-136">DLL</span><span class="sxs-lookup"><span data-stu-id="63b50-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63b50-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63b50-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="63b50-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63b50-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b50-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="63b50-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

