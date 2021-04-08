---
description: Importe les métadonnées de point de référence du système virtuel.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Méthode ImportReferencePointMetadata de la classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953450"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="da3fd-103">Méthode ImportReferencePointMetadata de la \_ classe VirtualSystemReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="da3fd-103">ImportReferencePointMetadata method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="da3fd-104">Importe les métadonnées de point de référence du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="da3fd-104">Imports reference point metadata of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="da3fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da3fd-105">Syntax</span></span>


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="da3fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da3fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da3fd-107">*AffectedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da3fd-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da3fd-108">Référence à un [**\_ ComputerSystem MSVM**](msvm-computersystem.md) décrivant le système affecté.</span><span class="sxs-lookup"><span data-stu-id="da3fd-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) describing the affected system.</span></span>

</dd> <dt>

<span data-ttu-id="da3fd-109">*ConfigFilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da3fd-109">*ConfigFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da3fd-110">Chemin d’accès complet du fichier de configuration à partir duquel les métadonnées de point de référence seront importées.</span><span class="sxs-lookup"><span data-stu-id="da3fd-110">The fully-qualified path of the config file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="da3fd-111">*RuntimeStateFilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da3fd-111">*RuntimeStateFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da3fd-112">Chemin d’accès qualifié complet du fichier d’état d’exécution à partir duquel les métadonnées de point de référence seront importées.</span><span class="sxs-lookup"><span data-stu-id="da3fd-112">The fully-qualified path of the runtime state file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="da3fd-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="da3fd-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da3fd-114">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="da3fd-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="da3fd-115">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="da3fd-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da3fd-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da3fd-116">Return value</span></span>

<span data-ttu-id="da3fd-117">Retourne 0 (aucune erreur) ou l’un des messages d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="da3fd-117">Returns either 0 (no error) or one of the following error messages:</span></span>

<dl> <dt>

<span data-ttu-id="da3fd-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="da3fd-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="da3fd-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="da3fd-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="da3fd-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="da3fd-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="da3fd-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="da3fd-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="da3fd-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="da3fd-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="da3fd-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="da3fd-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="da3fd-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="da3fd-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="da3fd-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="da3fd-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da3fd-131">Requirements</span></span>



| <span data-ttu-id="da3fd-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da3fd-132">Requirement</span></span> | <span data-ttu-id="da3fd-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="da3fd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da3fd-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da3fd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="da3fd-135">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da3fd-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="da3fd-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da3fd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="da3fd-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="da3fd-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="da3fd-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="da3fd-138">Namespace</span></span><br/>                | <span data-ttu-id="da3fd-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="da3fd-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="da3fd-140">MOF</span><span class="sxs-lookup"><span data-stu-id="da3fd-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da3fd-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da3fd-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da3fd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="da3fd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da3fd-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da3fd-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="da3fd-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da3fd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3fd-145">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="da3fd-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




