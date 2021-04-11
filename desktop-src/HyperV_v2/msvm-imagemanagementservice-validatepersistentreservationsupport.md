---
description: Valide si un système de fichiers peut prendre en charge un disque dur virtuel pour lequel les réservations persistantes sont activées.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Méthode ValidatePersistentReservationSupport de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 596e5cf840ee65dc0b3ad5315462db4666c8b262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951286"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="53454-103">Méthode ValidatePersistentReservationSupport de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="53454-103">ValidatePersistentReservationSupport method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="53454-104">Valide si un système de fichiers peut prendre en charge un disque dur virtuel pour lequel les réservations persistantes sont activées.</span><span class="sxs-lookup"><span data-stu-id="53454-104">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="53454-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53454-105">Syntax</span></span>


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="53454-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53454-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53454-107">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53454-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53454-108">Chemin d’accès complet qui spécifie l’emplacement d’un fichier image de disque ou d’un répertoire dans lequel un fichier image de disque peut être placé.</span><span class="sxs-lookup"><span data-stu-id="53454-108">A fully-qualified path that specifies the location of a disk image file or a directory in which a disk image file might be placed.</span></span>

</dd> <dt>

<span data-ttu-id="53454-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="53454-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53454-110">Référence au travail (peut avoir la valeur null si la tâche est terminée avec succès).</span><span class="sxs-lookup"><span data-stu-id="53454-110">A reference to the job (can be null if the task is completed succesfully).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53454-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53454-111">Return value</span></span>

<span data-ttu-id="53454-112">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="53454-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="53454-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="53454-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53454-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="53454-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="53454-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="53454-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="53454-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="53454-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="53454-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="53454-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="53454-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="53454-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="53454-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="53454-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="53454-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="53454-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="53454-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="53454-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="53454-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="53454-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="53454-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="53454-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="53454-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="53454-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="53454-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="53454-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="53454-126">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="53454-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="53454-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53454-127">Requirements</span></span>



| <span data-ttu-id="53454-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53454-128">Requirement</span></span> | <span data-ttu-id="53454-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="53454-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53454-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53454-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53454-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="53454-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="53454-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53454-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53454-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="53454-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="53454-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53454-134">Namespace</span></span><br/>                | <span data-ttu-id="53454-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="53454-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53454-136">MOF</span><span class="sxs-lookup"><span data-stu-id="53454-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53454-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53454-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53454-138">DLL</span><span class="sxs-lookup"><span data-stu-id="53454-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53454-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53454-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53454-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53454-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53454-141">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="53454-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




