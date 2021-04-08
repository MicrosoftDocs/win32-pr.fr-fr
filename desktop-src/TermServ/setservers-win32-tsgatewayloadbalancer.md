---
title: Méthode SetServers de la classe Win32_TSGatewayLoadBalancer
description: Définit la propriété serveurs à l’aide de la liste des serveurs d’équilibrage de charge de la passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetServers
- Services Bureau à distance de la méthode SetServers, classe Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, méthode SetServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d1123ce82844fb501f3562014b93337502b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742372"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="bcb0e-106">Méthode SetServers de la \_ classe Win32 TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bcb0e-106">SetServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="bcb0e-107">Définit la propriété **serveurs** à l’aide de la liste des serveurs d’équilibrage de charge de la passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="bcb0e-107">Sets the **Servers** property with the list of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb0e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcb0e-108">Syntax</span></span>


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="bcb0e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcb0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb0e-110">*Serveurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcb0e-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb0e-111">Liste séparée par des points-virgules des serveurs d’équilibrage de charge de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-111">Semicolon-separated list of RD Gateway load-balancing servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb0e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcb0e-112">Return value</span></span>

<span data-ttu-id="bcb0e-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bcb0e-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bcb0e-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bcb0e-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb0e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bcb0e-116">Remarks</span></span>

<span data-ttu-id="bcb0e-117">Si plusieurs serveurs se trouvent dans le paramètre *serveurs* et que l’un des serveurs ne peut pas être traité, aucun des serveurs ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="bcb0e-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bcb0e-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="bcb0e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bcb0e-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bcb0e-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bcb0e-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bcb0e-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb0e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcb0e-123">Requirements</span></span>



| <span data-ttu-id="bcb0e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcb0e-124">Requirement</span></span> | <span data-ttu-id="bcb0e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcb0e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb0e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcb0e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb0e-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcb0e-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bcb0e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcb0e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb0e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcb0e-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bcb0e-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bcb0e-130">Namespace</span></span><br/>                | <span data-ttu-id="bcb0e-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="bcb0e-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bcb0e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bcb0e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcb0e-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcb0e-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcb0e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bcb0e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcb0e-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcb0e-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bcb0e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcb0e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb0e-137">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="bcb0e-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

