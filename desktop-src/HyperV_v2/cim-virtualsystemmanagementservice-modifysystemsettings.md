---
description: Modifie les paramètres du système virtuel.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Méthode ModifySystemSettings de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951652"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="1f3cf-103">Méthode ModifySystemSettings de la \_ classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="1f3cf-103">ModifySystemSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1f3cf-104">Modifie les paramètres du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-104">Modifies virtual system settings.</span></span>

<span data-ttu-id="1f3cf-105">En cas d’application aux paramètres système d’une configuration de système virtuel « actuelle », l’instance de système virtuel peut être modifiée en tant qu’effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-105">When applied to the system settings of a "current" virtual system configuration, as a side effect the virtual system instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f3cf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f3cf-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1f3cf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f3cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f3cf-108">*SystemSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f3cf-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f3cf-109">Chaîne contenant une instance de la [**classe \_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) qui est utilisée pour modifier les paramètres du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-109">String containing an instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to modify the settings of the virtual system.</span></span> <span data-ttu-id="1f3cf-110">L’instance doit avoir un **InstanceID** valide pour permettre l’identification du paramètre du système virtuel à modifier.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-110">The instance must have a valid **InstanceID** in order to identify the virtual system setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="1f3cf-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f3cf-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f3cf-112">Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f3cf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f3cf-113">Return value</span></span>

<span data-ttu-id="1f3cf-114">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1f3cf-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-117">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-118">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-119">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-120">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-121">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1f3cf-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1f3cf-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1f3cf-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f3cf-126">Requirements</span></span>



| <span data-ttu-id="1f3cf-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f3cf-127">Requirement</span></span> | <span data-ttu-id="1f3cf-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f3cf-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3cf-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f3cf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1f3cf-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1f3cf-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1f3cf-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f3cf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1f3cf-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1f3cf-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1f3cf-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1f3cf-133">Namespace</span></span><br/>                | <span data-ttu-id="1f3cf-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1f3cf-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1f3cf-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1f3cf-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f3cf-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f3cf-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f3cf-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1f3cf-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f3cf-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f3cf-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1f3cf-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f3cf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f3cf-140">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1f3cf-140">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




