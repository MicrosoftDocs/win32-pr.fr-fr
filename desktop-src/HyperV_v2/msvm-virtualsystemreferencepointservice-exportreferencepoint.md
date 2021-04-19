---
description: Exporte le point de référence du système virtuel.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Méthode ExportReferencePoint de la classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538432"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="ea733-103">Méthode ExportReferencePoint de la \_ classe VirtualSystemReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="ea733-103">ExportReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="ea733-104">Exporte le point de référence du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ea733-104">Exports the reference point of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea733-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea733-105">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ea733-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea733-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea733-107">*ReferencePoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea733-107">*ReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea733-108">Référence à l’instance [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente le point de référence à exporter.</span><span class="sxs-lookup"><span data-stu-id="ea733-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="ea733-109">*ExportDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea733-109">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea733-110">Chemin d’accès complet du répertoire vers lequel le point de référence doit être exporté.</span><span class="sxs-lookup"><span data-stu-id="ea733-110">The fully-qualified path of the directory to which the reference point is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="ea733-111">*ExportSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea733-111">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea733-112">Instance de [**MSVM \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="ea733-112">An instance of [**Msvm\_VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="ea733-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea733-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea733-114">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="ea733-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="ea733-115">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="ea733-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea733-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea733-116">Return value</span></span>

<span data-ttu-id="ea733-117">En cas de réussite, retourne 0 (terminé sans erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="ea733-117">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="ea733-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="ea733-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="ea733-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="ea733-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="ea733-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="ea733-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="ea733-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="ea733-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="ea733-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="ea733-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="ea733-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="ea733-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ea733-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ea733-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="ea733-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ea733-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea733-131">Requirements</span></span>



| <span data-ttu-id="ea733-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea733-132">Requirement</span></span> | <span data-ttu-id="ea733-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea733-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea733-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea733-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ea733-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea733-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ea733-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea733-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ea733-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ea733-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ea733-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ea733-138">Namespace</span></span><br/>                | <span data-ttu-id="ea733-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ea733-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ea733-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ea733-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea733-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea733-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea733-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ea733-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea733-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea733-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea733-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea733-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea733-145">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="ea733-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




