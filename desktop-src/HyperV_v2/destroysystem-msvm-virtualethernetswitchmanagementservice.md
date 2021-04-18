---
description: Détruit un commutateur virtuel.
ms.assetid: f0b6b4cc-e9b7-4255-a9e1-a2a826b8f119
title: Méthode DestroySystem de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d8f01a3f72d15fba908c7891f76b4128a1ee8200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529194"
---
# <a name="destroysystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="a2cea-103">Méthode DestroySystem de la \_ classe VirtualEthernetSwitchManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="a2cea-103">DestroySystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="a2cea-104">Détruit un commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a2cea-104">Destroys a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2cea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2cea-105">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a2cea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2cea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2cea-107">*AffectedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2cea-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cea-108">Référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) qui représente le commutateur virtuel qui doit être détruit.</span><span class="sxs-lookup"><span data-stu-id="a2cea-108">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="a2cea-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a2cea-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cea-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2cea-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2cea-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2cea-111">Return value</span></span>

<span data-ttu-id="a2cea-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2cea-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a2cea-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a2cea-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-114">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a2cea-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-115">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="a2cea-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-116">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="a2cea-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-117">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="a2cea-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-118">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="a2cea-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-119">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a2cea-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-120">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="a2cea-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-121">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a2cea-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a2cea-122">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a2cea-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a2cea-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2cea-123">Requirements</span></span>



| <span data-ttu-id="a2cea-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2cea-124">Requirement</span></span> | <span data-ttu-id="a2cea-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2cea-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2cea-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2cea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a2cea-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2cea-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a2cea-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2cea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a2cea-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2cea-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2cea-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a2cea-130">Namespace</span></span><br/>                | <span data-ttu-id="a2cea-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2cea-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a2cea-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a2cea-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2cea-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2cea-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2cea-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a2cea-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2cea-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2cea-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2cea-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2cea-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2cea-137">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="a2cea-137">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

