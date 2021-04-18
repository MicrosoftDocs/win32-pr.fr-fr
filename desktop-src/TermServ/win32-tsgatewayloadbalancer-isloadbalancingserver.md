---
title: Méthode IsLoadBalancingServer de la classe Win32_TSGatewayLoadBalancer
description: Détermine si le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) peut effectuer l’équilibrage de charge.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLoadBalancingServer
- Services Bureau à distance de la méthode IsLoadBalancingServer, classe Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, méthode IsLoadBalancingServer
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512818"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="3c0dd-106">Méthode IsLoadBalancingServer de la \_ classe Win32 TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3c0dd-106">IsLoadBalancingServer method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="3c0dd-107">Détermine si le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) peut effectuer l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="3c0dd-107">Determines whether the Remote Desktop Gateway (RD Gateway) server can perform load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0dd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c0dd-108">Syntax</span></span>


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a><span data-ttu-id="3c0dd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c0dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0dd-110">*LoadBalancing* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c0dd-110">*LoadBalancing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c0dd-111">**True** si le serveur peut effectuer l’équilibrage de charge et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3c0dd-111">**TRUE** if the server can perform load balancing, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0dd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c0dd-112">Return value</span></span>

<span data-ttu-id="3c0dd-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3c0dd-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3c0dd-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3c0dd-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3c0dd-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3c0dd-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c0dd-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3c0dd-116">Remarks</span></span>

<span data-ttu-id="3c0dd-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3c0dd-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3c0dd-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3c0dd-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c0dd-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3c0dd-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c0dd-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3c0dd-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c0dd-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3c0dd-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0dd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c0dd-122">Requirements</span></span>



| <span data-ttu-id="3c0dd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c0dd-123">Requirement</span></span> | <span data-ttu-id="3c0dd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c0dd-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0dd-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c0dd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0dd-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c0dd-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3c0dd-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c0dd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0dd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c0dd-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3c0dd-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c0dd-129">Namespace</span></span><br/>                | <span data-ttu-id="3c0dd-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="3c0dd-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3c0dd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3c0dd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c0dd-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c0dd-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c0dd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3c0dd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c0dd-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c0dd-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3c0dd-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c0dd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0dd-136">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="3c0dd-136">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

