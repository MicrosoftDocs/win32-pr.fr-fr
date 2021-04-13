---
title: Méthode AddComputerGroupNames de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Ajoute les noms de groupes d’ordinateurs spécifiés à la propriété ComputerGroupNames.
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddComputerGroupNames
- Services Bureau à distance de la méthode AddComputerGroupNames, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode AddComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72647ef66b9e2eeaed824b3e77c404214786b615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104341"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="d5a04-106">Méthode AddComputerGroupNames de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a04-106">AddComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="d5a04-107">Ajoute les noms de groupes d’ordinateurs spécifiés à la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="d5a04-107">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a04-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5a04-108">Syntax</span></span>


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="d5a04-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5a04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a04-110">*ComputerGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5a04-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a04-111">Liste de noms de groupes d’ordinateurs séparés par des points-virgules à ajouter à la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="d5a04-111">Semicolon-separated list of computer group names to add to the **ComputerGroupNames** property.</span></span> <span data-ttu-id="d5a04-112">Les noms des groupes d’ordinateurs doivent être au format *domaine \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="d5a04-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a04-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5a04-113">Return value</span></span>

<span data-ttu-id="d5a04-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="d5a04-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d5a04-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d5a04-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d5a04-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d5a04-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5a04-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d5a04-117">Remarks</span></span>

<span data-ttu-id="d5a04-118">Si plusieurs noms de groupe d’ordinateurs se trouvent dans le paramètre *ComputerGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="d5a04-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="d5a04-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d5a04-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d5a04-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d5a04-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d5a04-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d5a04-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d5a04-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d5a04-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d5a04-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d5a04-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a04-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5a04-124">Requirements</span></span>



| <span data-ttu-id="d5a04-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5a04-125">Requirement</span></span> | <span data-ttu-id="d5a04-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5a04-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a04-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5a04-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a04-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5a04-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d5a04-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5a04-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a04-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5a04-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d5a04-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d5a04-131">Namespace</span></span><br/>                | <span data-ttu-id="d5a04-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d5a04-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d5a04-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d5a04-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5a04-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5a04-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5a04-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d5a04-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5a04-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5a04-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d5a04-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5a04-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a04-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="d5a04-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

