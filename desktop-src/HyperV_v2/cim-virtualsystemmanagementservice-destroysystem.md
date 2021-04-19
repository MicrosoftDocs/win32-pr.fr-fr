---
description: Détruit un système virtuel.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Méthode DestroySystem de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527836"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="33198-103">Méthode DestroySystem de la \_ classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="33198-103">DestroySystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="33198-104">Détruit un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="33198-104">Destroys a virtual system.</span></span>

<span data-ttu-id="33198-105">Le système virtuel référencé est détruit, y compris les éléments dont il est limité.</span><span class="sxs-lookup"><span data-stu-id="33198-105">The referenced virtual system is destroyed, including any elements scoped by it.</span></span> <span data-ttu-id="33198-106">Les ressources virtuelles sont retournées à leurs pools de ressources, ce qui peut impliquer la destruction de ces ressources (dépendantes de l’implémentation).</span><span class="sxs-lookup"><span data-stu-id="33198-106">Virtual resources are returned to their resource pools, which may imply the destruction of those resources (implementation dependent).</span></span> <span data-ttu-id="33198-107">Si le système virtuel est actif lors de l’appel de l’opération, il est d’abord désactivé, puis détruit.</span><span class="sxs-lookup"><span data-stu-id="33198-107">If the virtual system is active when the operation is invoked, it is first deactivated and then destroyed.</span></span> <span data-ttu-id="33198-108">Si des captures instantanées ont été créées à partir du système virtuel, elles sont également détruites.</span><span class="sxs-lookup"><span data-stu-id="33198-108">If snapshots were created from the virtual system, these are destroyed as well.</span></span>

## <a name="syntax"></a><span data-ttu-id="33198-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33198-109">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="33198-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33198-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33198-111">*AffectedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33198-111">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33198-112">Référence à une instance de la classe [**CIM CIM \_ représentant**](cim-computersystem.md) le système d’ordinateur virtuel qui doit être détruit.</span><span class="sxs-lookup"><span data-stu-id="33198-112">Reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the virtual computer system that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="33198-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="33198-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33198-114">Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="33198-114">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33198-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33198-115">Return value</span></span>

<span data-ttu-id="33198-116">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="33198-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="33198-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="33198-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33198-118">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="33198-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="33198-119">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="33198-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="33198-120">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="33198-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="33198-121">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="33198-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="33198-122">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="33198-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="33198-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="33198-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="33198-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="33198-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="33198-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="33198-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="33198-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="33198-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="33198-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33198-127">Requirements</span></span>



| <span data-ttu-id="33198-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33198-128">Requirement</span></span> | <span data-ttu-id="33198-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="33198-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33198-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33198-130">Minimum supported client</span></span><br/> | <span data-ttu-id="33198-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33198-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="33198-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33198-132">Minimum supported server</span></span><br/> | <span data-ttu-id="33198-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="33198-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="33198-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33198-134">Namespace</span></span><br/>                | <span data-ttu-id="33198-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="33198-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="33198-136">MOF</span><span class="sxs-lookup"><span data-stu-id="33198-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33198-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33198-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33198-138">DLL</span><span class="sxs-lookup"><span data-stu-id="33198-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33198-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33198-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33198-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33198-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33198-141">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="33198-141">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




