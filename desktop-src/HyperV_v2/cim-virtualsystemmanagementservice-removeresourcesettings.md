---
description: Supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Méthode RemoveResourceSettings de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1f5b3ac1cc53f23d0d899a4c6b5d17408bca3b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755437"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="4efb1-103">Méthode RemoveResourceSettings de la \_ classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="4efb1-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4efb1-104">Supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="4efb1-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="4efb1-105">En cas d’application à des parties d’une configuration de système virtuel « en cours », les ressources d’effets secondaires du système virtuel actif peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="4efb1-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4efb1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4efb1-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4efb1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4efb1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4efb1-108">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4efb1-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4efb1-109">Tableau de références aux instances de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) où chaque instance représente les paramètres d’une ressource virtuelle au sein d’une configuration de système virtuel qui doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="4efb1-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="4efb1-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4efb1-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4efb1-111">Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="4efb1-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4efb1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4efb1-112">Return value</span></span>

<span data-ttu-id="4efb1-113">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="4efb1-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4efb1-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="4efb1-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="4efb1-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="4efb1-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="4efb1-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="4efb1-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="4efb1-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4efb1-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="4efb1-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-122">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4efb1-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4efb1-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4efb1-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4efb1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4efb1-124">Requirements</span></span>



| <span data-ttu-id="4efb1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4efb1-125">Requirement</span></span> | <span data-ttu-id="4efb1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4efb1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4efb1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4efb1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4efb1-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4efb1-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4efb1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4efb1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4efb1-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4efb1-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4efb1-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4efb1-131">Namespace</span></span><br/>                | <span data-ttu-id="4efb1-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4efb1-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4efb1-133">MOF</span><span class="sxs-lookup"><span data-stu-id="4efb1-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4efb1-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4efb1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4efb1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4efb1-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4efb1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4efb1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4efb1-138">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4efb1-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




