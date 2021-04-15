---
title: Méthode DeleteAllServers de la classe Win32_TSGatewayLoadBalancer
description: Supprime tous les serveurs d’équilibrage de charge de la passerelle des services Bureau à distance de Bureau à distance qui participent à la batterie d’équilibrage de charge.
ms.assetid: 091ed866-8f2b-47b8-990b-e9a6d7e1194c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteAllServers
- Services Bureau à distance de la méthode DeleteAllServers, classe Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, méthode DeleteAllServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteAllServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8004b4cfe811394acb328938775fcc9947bbbd19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508358"
---
# <a name="deleteallservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="5b5f7-106">Méthode DeleteAllServers de la \_ classe Win32 TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b5f7-106">DeleteAllServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="5b5f7-107">Supprime tous les serveurs d’équilibrage de charge de la passerelle des services Bureau à distance de Bureau à distance qui participent à la batterie d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-107">Deletes all Remote Desktop Gateway (RD Gateway) load-balancing servers that are participating in the load-balancing farm.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5f7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b5f7-108">Syntax</span></span>


```mof
uint32 DeleteAllServers();
```



## <a name="parameters"></a><span data-ttu-id="5b5f7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b5f7-109">Parameters</span></span>

<span data-ttu-id="5b5f7-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b5f7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b5f7-111">Return value</span></span>

<span data-ttu-id="5b5f7-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5b5f7-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5b5f7-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5b5f7-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5f7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5b5f7-115">Remarks</span></span>

<span data-ttu-id="5b5f7-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5b5f7-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5b5f7-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5b5f7-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5b5f7-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5b5f7-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5b5f7-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5f7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b5f7-121">Requirements</span></span>



| <span data-ttu-id="5b5f7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b5f7-122">Requirement</span></span> | <span data-ttu-id="5b5f7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b5f7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5f7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5f7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5f7-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5f7-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5b5f7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5f7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5f7-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b5f7-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5b5f7-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b5f7-128">Namespace</span></span><br/>                | <span data-ttu-id="5b5f7-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5b5f7-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5b5f7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5b5f7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b5f7-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b5f7-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b5f7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5b5f7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b5f7-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b5f7-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5b5f7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b5f7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5f7-135">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-135">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

