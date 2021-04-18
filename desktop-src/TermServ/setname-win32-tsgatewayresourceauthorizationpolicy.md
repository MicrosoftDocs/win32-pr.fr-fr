---
title: Méthode SetName de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit la propriété de nom pour la stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP).
ms.assetid: 3a652ece-11fe-4aa7-913d-39ef96ab1633
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetName
- Services Bureau à distance de la méthode SetName, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7e595472302d97e91026b3a84dc466e248ef5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511764"
---
# <a name="setname-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="c90d8-106">Méthode SetName de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="c90d8-106">SetName method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="c90d8-107">Définit la propriété de **nom** pour la stratégie d’autorisation d’accès aux ressources Bureau À distance (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="c90d8-107">Sets the **Name** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="c90d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c90d8-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="c90d8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c90d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c90d8-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c90d8-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c90d8-111">Nom de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="c90d8-111">Name of the RD RAP.</span></span> <span data-ttu-id="c90d8-112">Le nom doit comporter 64 caractères ou moins, unique (la casse est ignorée) et ne peut pas contenir les caractères réservés suivants :</span><span class="sxs-lookup"><span data-stu-id="c90d8-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="c90d8-113"><>  :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="c90d8-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="c90d8-114">\*\[Onglet\]</span><span class="sxs-lookup"><span data-stu-id="c90d8-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c90d8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c90d8-115">Return value</span></span>

<span data-ttu-id="c90d8-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c90d8-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c90d8-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c90d8-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c90d8-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c90d8-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c90d8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c90d8-119">Remarks</span></span>

<span data-ttu-id="c90d8-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c90d8-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c90d8-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c90d8-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c90d8-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c90d8-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c90d8-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c90d8-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c90d8-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c90d8-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c90d8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c90d8-125">Requirements</span></span>



| <span data-ttu-id="c90d8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c90d8-126">Requirement</span></span> | <span data-ttu-id="c90d8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c90d8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c90d8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90d8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c90d8-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90d8-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c90d8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90d8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c90d8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c90d8-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c90d8-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c90d8-132">Namespace</span></span><br/>                | <span data-ttu-id="c90d8-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c90d8-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c90d8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c90d8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c90d8-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c90d8-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c90d8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c90d8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c90d8-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c90d8-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c90d8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c90d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90d8-139">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c90d8-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

