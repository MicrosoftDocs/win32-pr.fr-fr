---
description: Injecte une interruption non masquable dans la machine virtuelle.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Msvm_ComputerSystem :: InjectNonMaskableInterrupt, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512938"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a><span data-ttu-id="69882-103">MSVM \_ ComputerSystem :: InjectNonMaskableInterrupt, méthode</span><span class="sxs-lookup"><span data-stu-id="69882-103">Msvm\_ComputerSystem::InjectNonMaskableInterrupt method</span></span>

<span data-ttu-id="69882-104">Injecte une interruption non masquable dans la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="69882-104">Injects a non-maskable interrupt into the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="69882-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69882-105">Syntax</span></span>


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a><span data-ttu-id="69882-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69882-107">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69882-107">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69882-108">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) pour suivre l’état de l’injection d’interruptions.</span><span class="sxs-lookup"><span data-stu-id="69882-108">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) to track the status of the interrupt injection.</span></span> <span data-ttu-id="69882-109">Cette référence peut être **null** si la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="69882-109">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69882-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69882-110">Return value</span></span>

<span data-ttu-id="69882-111">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="69882-111">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="69882-112">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="69882-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69882-113">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="69882-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="69882-114">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="69882-114">**Access Denied** (32769)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="69882-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69882-115">Requirements</span></span>



| <span data-ttu-id="69882-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69882-116">Requirement</span></span> | <span data-ttu-id="69882-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="69882-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69882-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69882-118">Minimum supported client</span></span><br/> | <span data-ttu-id="69882-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69882-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="69882-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69882-120">Minimum supported server</span></span><br/> | <span data-ttu-id="69882-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69882-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69882-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69882-122">Namespace</span></span><br/>                | <span data-ttu-id="69882-123">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="69882-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="69882-124">MOF</span><span class="sxs-lookup"><span data-stu-id="69882-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69882-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69882-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69882-126">DLL</span><span class="sxs-lookup"><span data-stu-id="69882-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69882-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69882-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69882-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69882-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69882-129">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="69882-129">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

