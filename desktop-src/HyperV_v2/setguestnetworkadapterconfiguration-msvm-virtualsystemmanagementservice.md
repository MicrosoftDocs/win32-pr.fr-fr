---
description: Configure les cartes réseau dans le système d’exploitation invité.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Méthode SetGuestNetworkAdapterConfiguration de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529043"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="5e5a7-103">Méthode SetGuestNetworkAdapterConfiguration de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="5e5a7-103">SetGuestNetworkAdapterConfiguration method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="5e5a7-104">Configure les cartes réseau dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="5e5a7-104">Configures the network adapters within the guest operating system.</span></span> <span data-ttu-id="5e5a7-105">Ces paramètres de configuration sont appliqués immédiatement lors de l’établissement de la communication avec le composant d’intégration KVP Exchange s’exécutant dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="5e5a7-105">These configuration parameters are applied immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5a7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e5a7-106">Syntax</span></span>


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5e5a7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e5a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5a7-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e5a7-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5a7-109">Référence à l’instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) dont les cartes réseau doivent être configurées.</span><span class="sxs-lookup"><span data-stu-id="5e5a7-109">A reference to the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="5e5a7-110">*NetworkConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e5a7-110">*NetworkConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5a7-111">Tableau d’instances incorporées de la classe [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="5e5a7-111">An array of embedded instances of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span> <span data-ttu-id="5e5a7-112">Chaque instance décrit les paramètres de configuration de l’une des cartes réseau de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5e5a7-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="5e5a7-113">La propriété **DHCPEnabled** doit être spécifiée pour chaque instance.</span><span class="sxs-lookup"><span data-stu-id="5e5a7-113">The **DHCPEnabled** property must be specified for each instance.</span></span>

</dd> <dt>

<span data-ttu-id="5e5a7-114">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5e5a7-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5a7-115">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e5a7-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5a7-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e5a7-116">Return value</span></span>

<span data-ttu-id="5e5a7-117">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e5a7-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5e5a7-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5e5a7-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5e5a7-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e5a7-131">Requirements</span></span>



| <span data-ttu-id="5e5a7-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e5a7-132">Requirement</span></span> | <span data-ttu-id="5e5a7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e5a7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5a7-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e5a7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5a7-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e5a7-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e5a7-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e5a7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5a7-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e5a7-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e5a7-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5e5a7-138">Namespace</span></span><br/>                | <span data-ttu-id="5e5a7-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5e5a7-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e5a7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5e5a7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e5a7-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e5a7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5e5a7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5a7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e5a7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e5a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5a7-145">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="5e5a7-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

