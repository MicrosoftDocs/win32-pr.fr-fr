---
title: Méthode SetComputerGroupNames de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété ComputerGroupNames.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetComputerGroupNames
- Services Bureau à distance de la méthode SetComputerGroupNames, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384564"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="559e3-106">Méthode SetComputerGroupNames de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="559e3-106">SetComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="559e3-107">Définit la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="559e3-107">Sets the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="559e3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="559e3-108">Syntax</span></span>


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="559e3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="559e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="559e3-110">*ComputerGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="559e3-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="559e3-111">Liste des noms de groupes d’ordinateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="559e3-111">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="559e3-112">Cette valeur peut être vide.</span><span class="sxs-lookup"><span data-stu-id="559e3-112">This value can be empty.</span></span> <span data-ttu-id="559e3-113">Les noms sont au format *domaine \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="559e3-113">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="559e3-114">Si une valeur est spécifiée, l’ordinateur client doit appartenir à l’un de ces groupes d’ordinateurs pour que l’utilisateur accède au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="559e3-114">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="559e3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="559e3-115">Return value</span></span>

<span data-ttu-id="559e3-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="559e3-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="559e3-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="559e3-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="559e3-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="559e3-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="559e3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="559e3-119">Remarks</span></span>

<span data-ttu-id="559e3-120">Si plusieurs noms de groupe d’ordinateurs se trouvent dans le paramètre *ComputerGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="559e3-120">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="559e3-121">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="559e3-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="559e3-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="559e3-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="559e3-123">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="559e3-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="559e3-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="559e3-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="559e3-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="559e3-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="559e3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="559e3-126">Requirements</span></span>



| <span data-ttu-id="559e3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="559e3-127">Requirement</span></span> | <span data-ttu-id="559e3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="559e3-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="559e3-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="559e3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="559e3-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="559e3-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="559e3-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="559e3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="559e3-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="559e3-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="559e3-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="559e3-133">Namespace</span></span><br/>                | <span data-ttu-id="559e3-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="559e3-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="559e3-135">MOF</span><span class="sxs-lookup"><span data-stu-id="559e3-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="559e3-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="559e3-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="559e3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="559e3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="559e3-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="559e3-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="559e3-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="559e3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="559e3-140">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="559e3-140">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

