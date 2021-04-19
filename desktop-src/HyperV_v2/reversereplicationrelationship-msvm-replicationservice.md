---
description: Réplication d’une machine virtuelle basculée sur le serveur principal.
ms.assetid: 21806a66-85b4-4d9e-8a50-52d2b1933b67
title: Méthode ReverseReplicationRelationship de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ReverseReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 25ab0c754c5139b0b3419db74162a8ac0495cf1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530860"
---
# <a name="reversereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="1e41b-103">Méthode ReverseReplicationRelationship de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="1e41b-103">ReverseReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="1e41b-104">Réplication d’une machine virtuelle basculée sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="1e41b-104">Replicates a failed-over virtual machine back to the primary server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e41b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e41b-105">Syntax</span></span>


```mof
uint32 ReverseReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1e41b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e41b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e41b-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e41b-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41b-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la réplication doit être inversée.</span><span class="sxs-lookup"><span data-stu-id="1e41b-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be reversed.</span></span>

</dd> <dt>

<span data-ttu-id="1e41b-109">*ReplicationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e41b-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41b-110">Représentation sous forme de chaîne d’une instance de la classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) qui définit les paramètres de réplication.</span><span class="sxs-lookup"><span data-stu-id="1e41b-110">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="1e41b-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e41b-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41b-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1e41b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e41b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e41b-113">Return value</span></span>

<span data-ttu-id="1e41b-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e41b-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1e41b-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1e41b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1e41b-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1e41b-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1e41b-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1e41b-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1e41b-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1e41b-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1e41b-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1e41b-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1e41b-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1e41b-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1e41b-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1e41b-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="1e41b-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="1e41b-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1e41b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e41b-129">Requirements</span></span>



| <span data-ttu-id="1e41b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e41b-130">Requirement</span></span> | <span data-ttu-id="1e41b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e41b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e41b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e41b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1e41b-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e41b-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1e41b-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e41b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1e41b-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e41b-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e41b-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e41b-136">Namespace</span></span><br/>                | <span data-ttu-id="1e41b-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1e41b-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1e41b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1e41b-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e41b-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e41b-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e41b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1e41b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e41b-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e41b-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e41b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e41b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e41b-143">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="1e41b-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

