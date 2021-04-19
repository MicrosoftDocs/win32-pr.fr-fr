---
description: Définit un système virtuel.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Méthode DefineSystem de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529779"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="7fa14-103">Méthode DefineSystem de la \_ classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="7fa14-103">DefineSystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7fa14-104">Définit un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fa14-104">Defines a virtual system.</span></span>

<span data-ttu-id="7fa14-105">L’entrée qui n’est pas complètement spécifiée peut être remplie avec des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="7fa14-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa14-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fa14-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7fa14-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fa14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa14-108">*SystemSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fa14-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa14-109">Chaîne contenant une instance incorporée de la classe [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) qui est utilisée pour définir les attributs du système virtuel à créer.</span><span class="sxs-lookup"><span data-stu-id="7fa14-109">String containing an embedded instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to define attributes of the virtual system to be created.</span></span>

</dd> <dt>

<span data-ttu-id="7fa14-110">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fa14-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa14-111">Tableau de chaînes contenant chacune une instance incorporée de la classe [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) qui décrit les aspects virtuels d’une ressource virtuelle à créer dans l’étendue du nouveau système virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fa14-111">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be created in the scope of the new virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="7fa14-112">*ReferenceConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fa14-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa14-113">Référence à une instance d’objet [**\_ VirtualSystemSettingDat CIM**](cim-virtualsystemsettingdata.md) qui est l’objet de niveau supérieur d’une configuration de système virtuel de référence.</span><span class="sxs-lookup"><span data-stu-id="7fa14-113">Reference to a [**CIM\_VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) object instance that is the top level object of a reference virtual system configuration.</span></span> <span data-ttu-id="7fa14-114">La configuration de référence est utilisée pour compléter la configuration du nouveau système virtuel si les paramètres *SystemSettings* et *ResourceSettings* n’ont pas fourni les informations correspondantes.</span><span class="sxs-lookup"><span data-stu-id="7fa14-114">The reference configuration is used to complement the configuration of the new virtual system if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="7fa14-115">*ResultingSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7fa14-115">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa14-116">Si un système d’ordinateur virtuel est correctement défini, une référence à une instance de la classe [**CIM CIM \_**](cim-computersystem.md) qui représente le système d’ordinateur virtuel nouvellement défini est retournée.</span><span class="sxs-lookup"><span data-stu-id="7fa14-116">If a virtual computer system is successfully defined, a reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the newly defined virtual computer system is returned.</span></span>

</dd> <dt>

<span data-ttu-id="7fa14-117">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7fa14-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa14-118">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="7fa14-118">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="7fa14-119">Dans ce cas, l’instance de la [**classe \_ CIM CIM**](cim-computersystem.md) qui représente le nouveau système virtuel est présentée par le biais de l’Association [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) avec la propriété **AffectedElement** qui fait référence à la nouvelle instance de la classe **CIM CIM \_** et à la propriété **ElementEffects** définie sur 5 (créer).</span><span class="sxs-lookup"><span data-stu-id="7fa14-119">In this case, the instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the new virtual system is presented via association [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) with the property **AffectedElement** referring to the new instance of class **CIM\_ComputerSystem** and property **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa14-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fa14-120">Return value</span></span>

<span data-ttu-id="7fa14-121">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="7fa14-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7fa14-122">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="7fa14-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-123">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="7fa14-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-124">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="7fa14-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-125">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="7fa14-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-126">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="7fa14-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-127">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7fa14-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-128">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="7fa14-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-129">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7fa14-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7fa14-130">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7fa14-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7fa14-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fa14-131">Requirements</span></span>



| <span data-ttu-id="7fa14-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fa14-132">Requirement</span></span> | <span data-ttu-id="7fa14-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fa14-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa14-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fa14-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa14-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7fa14-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7fa14-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fa14-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa14-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7fa14-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7fa14-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7fa14-138">Namespace</span></span><br/>                | <span data-ttu-id="7fa14-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7fa14-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7fa14-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7fa14-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fa14-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fa14-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fa14-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7fa14-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fa14-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fa14-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7fa14-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fa14-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa14-145">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7fa14-145">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




