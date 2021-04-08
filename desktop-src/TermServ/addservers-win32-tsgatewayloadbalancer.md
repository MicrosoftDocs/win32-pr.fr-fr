---
title: Méthode AddServers de la classe Win32_TSGatewayLoadBalancer
description: Ajoute des serveurs aux serveurs d’équilibrage de charge de la passerelle Bureau à distance (passerelle des services Bureau à distance) dans la propriété serveurs.
ms.assetid: ffcbe14b-5ada-4951-bf51-95db14af41d7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddServers
- Services Bureau à distance de la méthode AddServers, classe Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, méthode AddServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.AddServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a510fd6ecee12b5251ec84773327d6217463240f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103176"
---
# <a name="addservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="b5433-106">Méthode AddServers de la \_ classe Win32 TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b5433-106">AddServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="b5433-107">Ajoute des serveurs aux serveurs d’équilibrage de charge de la passerelle Bureau à distance (passerelle des services Bureau à distance) dans la propriété **serveurs** .</span><span class="sxs-lookup"><span data-stu-id="b5433-107">Adds servers to the Remote Desktop Gateway (RD Gateway) load-balancing servers in the **Servers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5433-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5433-108">Syntax</span></span>


```mof
uint32 AddServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="b5433-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5433-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5433-110">*Serveurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5433-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5433-111">Liste séparée par des points-virgules des serveurs d’équilibrage de charge de la passerelle des services Bureau à distance à ajouter à la propriété **serveurs** .</span><span class="sxs-lookup"><span data-stu-id="b5433-111">Semicolon-separated list of RD Gateway load-balancing servers to be added to the **Servers** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5433-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5433-112">Return value</span></span>

<span data-ttu-id="b5433-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="b5433-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b5433-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b5433-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b5433-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b5433-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5433-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b5433-116">Remarks</span></span>

<span data-ttu-id="b5433-117">Si plusieurs serveurs se trouvent dans le paramètre *serveurs* et que l’un des serveurs ne peut pas être traité, aucun des serveurs ne sera traité.</span><span class="sxs-lookup"><span data-stu-id="b5433-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="b5433-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b5433-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b5433-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b5433-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b5433-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b5433-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b5433-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b5433-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b5433-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b5433-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5433-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5433-123">Requirements</span></span>



| <span data-ttu-id="b5433-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5433-124">Requirement</span></span> | <span data-ttu-id="b5433-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5433-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5433-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5433-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b5433-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5433-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b5433-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5433-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b5433-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5433-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b5433-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5433-130">Namespace</span></span><br/>                | <span data-ttu-id="b5433-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="b5433-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b5433-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b5433-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5433-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5433-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5433-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b5433-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5433-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5433-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b5433-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5433-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5433-137">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="b5433-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

