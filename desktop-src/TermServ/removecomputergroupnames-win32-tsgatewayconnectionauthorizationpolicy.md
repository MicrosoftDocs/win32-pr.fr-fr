---
title: Méthode RemoveComputerGroupNames de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Supprime les noms de groupes d’ordinateurs spécifiés de la propriété ComputerGroupNames.
ms.assetid: 5f4e566a-1a2e-459d-ab6c-53ffd42271d8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveComputerGroupNames
- Services Bureau à distance de la méthode RemoveComputerGroupNames, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode RemoveComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ec281798fba0257883eebfb60ac199b0f3c1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032635"
---
# <a name="removecomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="1d0e6-106">Méthode RemoveComputerGroupNames de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="1d0e6-106">RemoveComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="1d0e6-107">Supprime les noms de groupes d’ordinateurs spécifiés de la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="1d0e6-107">Removes specified computer group names from the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d0e6-108">Syntax</span></span>


```mof
uint32 RemoveComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="1d0e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d0e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0e6-110">*ComputerGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d0e6-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0e6-111">Liste de noms de groupes d’ordinateurs séparés par des points-virgules à supprimer de la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="1d0e6-111">Semicolon-separated list of computer group names to remove from the **ComputerGroupNames** property.</span></span> <span data-ttu-id="1d0e6-112">Les noms des groupes d’ordinateurs doivent être au format *domaine \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="1d0e6-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0e6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d0e6-113">Return value</span></span>

<span data-ttu-id="1d0e6-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="1d0e6-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1d0e6-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="1d0e6-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1d0e6-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1d0e6-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0e6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1d0e6-117">Remarks</span></span>

<span data-ttu-id="1d0e6-118">Si plusieurs noms de groupe d’ordinateurs se trouvent dans le paramètre *ComputerGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="1d0e6-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="1d0e6-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1d0e6-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1d0e6-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1d0e6-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1d0e6-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1d0e6-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1d0e6-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1d0e6-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1d0e6-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1d0e6-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0e6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d0e6-124">Requirements</span></span>



| <span data-ttu-id="1d0e6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d0e6-125">Requirement</span></span> | <span data-ttu-id="1d0e6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d0e6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0e6-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d0e6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0e6-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d0e6-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1d0e6-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d0e6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0e6-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d0e6-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1d0e6-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d0e6-131">Namespace</span></span><br/>                | <span data-ttu-id="1d0e6-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="1d0e6-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1d0e6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1d0e6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d0e6-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d0e6-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d0e6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1d0e6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d0e6-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d0e6-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1d0e6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d0e6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0e6-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0e6-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

