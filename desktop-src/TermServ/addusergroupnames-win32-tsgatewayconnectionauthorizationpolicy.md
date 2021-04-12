---
title: Méthode AddUserGroupNames de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Ajoute les noms de groupes d’utilisateurs spécifiés à la propriété UserGroupNames.
ms.assetid: 01bbccc3-c2e4-46ad-8649-1a30e001c949
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddUserGroupNames
- Services Bureau à distance de la méthode AddUserGroupNames, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a4fe26b27f954e5ea9a0c7ac666592f74337a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384216"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="f06ac-106">Méthode AddUserGroupNames de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="f06ac-106">AddUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="f06ac-107">Ajoute les noms de groupes d’utilisateurs spécifiés à la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="f06ac-107">Adds the specified user group names to the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f06ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f06ac-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="f06ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f06ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f06ac-110">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f06ac-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f06ac-111">Liste de noms de groupes d’utilisateurs séparés par des points-virgules à ajouter à la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="f06ac-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="f06ac-112">Les noms des groupes d’utilisateurs doivent être au format *domaine \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="f06ac-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f06ac-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f06ac-113">Return value</span></span>

<span data-ttu-id="f06ac-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="f06ac-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f06ac-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="f06ac-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f06ac-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f06ac-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f06ac-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f06ac-117">Remarks</span></span>

<span data-ttu-id="f06ac-118">Si plusieurs noms de groupes d’utilisateurs se trouvent dans le paramètre *UserGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="f06ac-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="f06ac-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f06ac-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f06ac-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f06ac-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f06ac-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f06ac-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f06ac-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f06ac-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f06ac-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f06ac-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f06ac-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f06ac-124">Requirements</span></span>



| <span data-ttu-id="f06ac-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f06ac-125">Requirement</span></span> | <span data-ttu-id="f06ac-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f06ac-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f06ac-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f06ac-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f06ac-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f06ac-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f06ac-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f06ac-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f06ac-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f06ac-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f06ac-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f06ac-131">Namespace</span></span><br/>                | <span data-ttu-id="f06ac-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f06ac-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f06ac-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f06ac-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f06ac-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f06ac-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f06ac-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f06ac-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f06ac-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f06ac-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f06ac-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f06ac-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f06ac-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="f06ac-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

