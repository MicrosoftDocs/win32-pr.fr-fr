---
description: Crée un commutateur virtuel.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Méthode DefineSystem de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867077"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="c6751-103">Méthode DefineSystem de la \_ classe VirtualEthernetSwitchManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="c6751-103">DefineSystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="c6751-104">Crée un commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c6751-104">Creates a new virtual switch.</span></span> <span data-ttu-id="c6751-105">Les propriétés qui ne sont pas spécifiées sont remplies avec les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="c6751-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6751-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6751-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c6751-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6751-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6751-108">*SystemSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6751-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6751-109">Une instance incorporée de la classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) utilisée pour définir les attributs du commutateur virtuel à créer.</span><span class="sxs-lookup"><span data-stu-id="c6751-109">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that is used to define the attributes of the virtual switch to be created.</span></span> <span data-ttu-id="c6751-110">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c6751-110">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="c6751-111">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6751-111">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6751-112">Tableau d’instances incorporées de la classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) qui décrit les paramètres des ports de commutateur à créer dans l’étendue du nouveau commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c6751-112">An array of embedded instances of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that describes the settings of the switch ports to be created in the scope of the new virtual switch.</span></span> <span data-ttu-id="c6751-113">Si la **valeur null** est spécifiée, le commutateur virtuel est créé sans aucune ressource (c’est-à-dire aucun port de commutateur).</span><span class="sxs-lookup"><span data-stu-id="c6751-113">If **Null** is specified, the virtual switch will be created with no resources (i.e. no switch ports).</span></span>

</dd> <dt>

<span data-ttu-id="c6751-114">*ReferenceConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6751-114">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6751-115">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c6751-115">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6751-116">*ResultingSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c6751-116">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6751-117">Si un commutateur virtuel est créé avec succès, référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) qui représente le commutateur virtuel nouvellement défini.</span><span class="sxs-lookup"><span data-stu-id="c6751-117">If a virtual switch is successfully created, a reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the newly defined virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="c6751-118">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c6751-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6751-119">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c6751-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6751-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6751-120">Return value</span></span>

<span data-ttu-id="c6751-121">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c6751-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c6751-122">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c6751-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-123">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="c6751-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-124">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="c6751-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-125">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="c6751-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-126">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="c6751-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-127">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c6751-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-128">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c6751-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-129">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c6751-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c6751-130">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c6751-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c6751-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6751-131">Requirements</span></span>



| <span data-ttu-id="c6751-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6751-132">Requirement</span></span> | <span data-ttu-id="c6751-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6751-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6751-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6751-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c6751-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6751-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c6751-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6751-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c6751-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6751-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6751-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c6751-138">Namespace</span></span><br/>                | <span data-ttu-id="c6751-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c6751-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c6751-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c6751-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6751-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6751-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6751-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c6751-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6751-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c6751-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c6751-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6751-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6751-145">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="c6751-145">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

