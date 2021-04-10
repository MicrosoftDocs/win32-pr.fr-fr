---
title: Méthode AddUserGroupNames de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Ajoute la liste de noms de groupes d’utilisateurs séparés par des points-virgules spécifiée aux groupes d’utilisateurs existants dans la propriété UserGroupNames.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddUserGroupNames
- Services Bureau à distance de la méthode AddUserGroupNames, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c5c3fcb57c60ff2ca4c14d2e42ff0acdc84f0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941819"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="baf8c-106">Méthode AddUserGroupNames de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="baf8c-106">AddUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="baf8c-107">Ajoute la liste de noms de groupes d’utilisateurs séparés par des points-virgules spécifiée aux groupes d’utilisateurs existants dans la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="baf8c-107">Adds the specified semicolon-separated list of user group names to the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf8c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baf8c-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="baf8c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="baf8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baf8c-110">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="baf8c-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baf8c-111">Liste de noms de groupes d’utilisateurs séparés par des points-virgules à ajouter à la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="baf8c-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="baf8c-112">Les noms des groupes d’utilisateurs doivent être au format *domaine \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="baf8c-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baf8c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="baf8c-113">Return value</span></span>

<span data-ttu-id="baf8c-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="baf8c-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="baf8c-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="baf8c-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="baf8c-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="baf8c-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="baf8c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="baf8c-117">Remarks</span></span>

<span data-ttu-id="baf8c-118">Si plusieurs noms de groupes d’utilisateurs se trouvent dans le paramètre *UserGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="baf8c-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="baf8c-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="baf8c-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="baf8c-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="baf8c-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="baf8c-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="baf8c-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="baf8c-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="baf8c-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="baf8c-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="baf8c-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="baf8c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="baf8c-124">Requirements</span></span>



| <span data-ttu-id="baf8c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="baf8c-125">Requirement</span></span> | <span data-ttu-id="baf8c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="baf8c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf8c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="baf8c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="baf8c-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="baf8c-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="baf8c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="baf8c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="baf8c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baf8c-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="baf8c-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="baf8c-131">Namespace</span></span><br/>                | <span data-ttu-id="baf8c-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="baf8c-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="baf8c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="baf8c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="baf8c-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="baf8c-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="baf8c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="baf8c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baf8c-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baf8c-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="baf8c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baf8c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf8c-138">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="baf8c-138">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

