---
title: Méthode SetLoadBalancingState de la classe Win32_TSSessionDirectory
description: Définit la valeur pour indiquer si le serveur doit participer à l’équilibrage de charge de Connexion Bureau à distance Broker (RD Connection Broker).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetLoadBalancingState
- Services Bureau à distance de la méthode SetLoadBalancingState, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512153"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="8ff66-106">Méthode SetLoadBalancingState de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="8ff66-106">SetLoadBalancingState method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="8ff66-107">Définit la valeur pour indiquer si le serveur doit participer à l’équilibrage de charge de Connexion Bureau à distance Broker (RD Connection Broker).</span><span class="sxs-lookup"><span data-stu-id="8ff66-107">Sets the value to indicate whether the server will participate in Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff66-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ff66-108">Syntax</span></span>


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a><span data-ttu-id="8ff66-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ff66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff66-110">*StateValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ff66-110">*StateValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff66-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ff66-111">Type: **uint32**</span></span>

<span data-ttu-id="8ff66-112">Indique si le serveur doit participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8ff66-112">Indicates whether the server will participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="8ff66-113">0</span><span class="sxs-lookup"><span data-stu-id="8ff66-113">0</span></span>
</dt> <dd>

<span data-ttu-id="8ff66-114">Le serveur ne participe pas à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8ff66-114">The server will not participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="8ff66-115">1</span><span class="sxs-lookup"><span data-stu-id="8ff66-115">1</span></span>
</dt> <dd>

<span data-ttu-id="8ff66-116">Le serveur fera partie de l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8ff66-116">The server will participate in RD Connection Broker load balancing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ff66-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8ff66-117">Remarks</span></span>

<span data-ttu-id="8ff66-118">Le serveur doit être joint à une batterie de serveurs du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8ff66-118">The server must be joined to a farm in RD Connection Broker.</span></span>

<span data-ttu-id="8ff66-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="8ff66-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8ff66-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8ff66-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8ff66-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="8ff66-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8ff66-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8ff66-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff66-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ff66-123">Requirements</span></span>



| <span data-ttu-id="8ff66-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ff66-124">Requirement</span></span> | <span data-ttu-id="8ff66-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ff66-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff66-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ff66-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff66-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ff66-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8ff66-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ff66-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff66-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ff66-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ff66-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8ff66-130">Namespace</span></span><br/>                | <span data-ttu-id="8ff66-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8ff66-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8ff66-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8ff66-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ff66-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ff66-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ff66-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8ff66-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ff66-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ff66-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff66-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ff66-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff66-137">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="8ff66-137">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

