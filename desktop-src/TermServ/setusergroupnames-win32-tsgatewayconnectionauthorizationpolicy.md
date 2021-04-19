---
title: Méthode SetUserGroupNames de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété UserGroupNames pour cette stratégie d’autorisation de connexion Bureau à distance (RD \ 160 ; CAP).
ms.assetid: 03c9b2c5-8769-46f2-941f-302d798dd3a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetUserGroupNames
- Services Bureau à distance de la méthode SetUserGroupNames, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ca948b63cd106e7284b00c2c5f9e54c6dfa86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513635"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a9472-106">Méthode SetUserGroupNames de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="a9472-106">SetUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a9472-107">Définit la propriété **UserGroupNames** pour cette stratégie d’autorisation des connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="a9472-107">Sets the **UserGroupNames** property for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9472-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9472-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="a9472-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9472-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9472-110">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9472-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9472-111">Liste des noms de groupes d’utilisateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="a9472-111">List of semicolon-separated user group names.</span></span> <span data-ttu-id="a9472-112">Les noms sont au format *domaine \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="a9472-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="a9472-113">Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’utilisateur est autorisé à accéder au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="a9472-113">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9472-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9472-114">Return value</span></span>

<span data-ttu-id="a9472-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="a9472-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a9472-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a9472-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a9472-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a9472-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a9472-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a9472-118">Remarks</span></span>

<span data-ttu-id="a9472-119">Si plusieurs noms de groupes d’utilisateurs se trouvent dans le paramètre *UserGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="a9472-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="a9472-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a9472-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a9472-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="a9472-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a9472-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a9472-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a9472-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="a9472-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a9472-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a9472-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9472-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9472-125">Requirements</span></span>



| <span data-ttu-id="a9472-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9472-126">Requirement</span></span> | <span data-ttu-id="a9472-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9472-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9472-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9472-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a9472-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9472-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a9472-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9472-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a9472-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9472-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a9472-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a9472-132">Namespace</span></span><br/>                | <span data-ttu-id="a9472-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a9472-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a9472-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a9472-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9472-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9472-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9472-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a9472-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9472-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9472-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a9472-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9472-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9472-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="a9472-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

