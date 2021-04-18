---
title: Méthode RemoveUserGroupNames de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Supprime les noms de groupes d’utilisateurs spécifiés des groupes d’utilisateurs existants dans la propriété UserGroupNames.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveUserGroupNames
- Services Bureau à distance de la méthode RemoveUserGroupNames, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512573"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="7fd26-106">Méthode RemoveUserGroupNames de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd26-106">RemoveUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="7fd26-107">Supprime les noms de groupes d’utilisateurs spécifiés des groupes d’utilisateurs existants dans la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="7fd26-107">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd26-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fd26-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="7fd26-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fd26-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd26-110">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fd26-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd26-111">Liste de noms de groupes d’utilisateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="7fd26-111">Semicolon-separated list of user group names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd26-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fd26-112">Return value</span></span>

<span data-ttu-id="7fd26-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="7fd26-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7fd26-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7fd26-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7fd26-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7fd26-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd26-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7fd26-116">Remarks</span></span>

<span data-ttu-id="7fd26-117">Si plusieurs noms de groupes d’utilisateurs se trouvent dans le paramètre *UserGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="7fd26-117">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="7fd26-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7fd26-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7fd26-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7fd26-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fd26-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7fd26-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7fd26-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7fd26-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fd26-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7fd26-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd26-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fd26-123">Requirements</span></span>



| <span data-ttu-id="7fd26-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fd26-124">Requirement</span></span> | <span data-ttu-id="7fd26-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fd26-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd26-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd26-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd26-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd26-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7fd26-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd26-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd26-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fd26-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7fd26-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7fd26-130">Namespace</span></span><br/>                | <span data-ttu-id="7fd26-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7fd26-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7fd26-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7fd26-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fd26-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fd26-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fd26-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd26-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd26-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fd26-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7fd26-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fd26-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd26-137">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="7fd26-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

