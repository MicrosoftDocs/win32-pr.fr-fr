---
description: Configure les paramètres IP des cartes réseau à appliquer à un ordinateur virtuel après un basculement.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Méthode SetFailoverNetworkAdapterSettings de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534504"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="33c1e-103">Méthode SetFailoverNetworkAdapterSettings de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="33c1e-103">SetFailoverNetworkAdapterSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="33c1e-104">Configure les paramètres IP de la carte réseau à appliquer à un ordinateur virtuel après un basculement.</span><span class="sxs-lookup"><span data-stu-id="33c1e-104">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span> <span data-ttu-id="33c1e-105">Ces paramètres de configuration sont appliqués après une opération de basculement, immédiatement après l’établissement de la communication avec le composant d’intégration KVP Exchange s’exécutant dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="33c1e-105">These configuration parameters are applied after a failover operation, immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c1e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33c1e-106">Syntax</span></span>


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="33c1e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33c1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c1e-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33c1e-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c1e-109">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel dont les cartes réseau doivent être configurées.</span><span class="sxs-lookup"><span data-stu-id="33c1e-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="33c1e-110">*NetworkSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33c1e-110">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c1e-111">Tableau d’instances incorporées d’objets [**MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="33c1e-111">An array of embedded instances of [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) objects.</span></span> <span data-ttu-id="33c1e-112">Chaque instance décrit les paramètres de configuration de l’une des cartes réseau de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="33c1e-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="33c1e-113">Les propriétés **adressesIP** et **DHCPEnabled** doivent être spécifiées sur chaque instance.</span><span class="sxs-lookup"><span data-stu-id="33c1e-113">The **IPAddresses** and **DHCPEnabled** properties must be specified on each instance.</span></span>

</dd> <dt>

<span data-ttu-id="33c1e-114">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="33c1e-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33c1e-115">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33c1e-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c1e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33c1e-116">Return value</span></span>

<span data-ttu-id="33c1e-117">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="33c1e-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="33c1e-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="33c1e-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="33c1e-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="33c1e-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="33c1e-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="33c1e-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="33c1e-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="33c1e-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="33c1e-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="33c1e-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="33c1e-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="33c1e-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="33c1e-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="33c1e-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="33c1e-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="33c1e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33c1e-131">Requirements</span></span>



| <span data-ttu-id="33c1e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33c1e-132">Requirement</span></span> | <span data-ttu-id="33c1e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="33c1e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c1e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33c1e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="33c1e-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33c1e-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="33c1e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33c1e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="33c1e-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33c1e-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33c1e-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33c1e-138">Namespace</span></span><br/>                | <span data-ttu-id="33c1e-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="33c1e-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="33c1e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="33c1e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33c1e-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33c1e-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33c1e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="33c1e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33c1e-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33c1e-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33c1e-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33c1e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c1e-145">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="33c1e-145">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="33c1e-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="33c1e-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="33c1e-147">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="33c1e-147">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

