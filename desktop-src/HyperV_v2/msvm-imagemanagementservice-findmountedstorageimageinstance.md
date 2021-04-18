---
description: Recherche un \_ objet MSVM MountedStorageImage pour un chemin d’accès d’image de disque donné.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Méthode FindMountedStorageImageInstance de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526835"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="d69c4-103">Méthode FindMountedStorageImageInstance de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="d69c4-103">FindMountedStorageImageInstance method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="d69c4-104">Recherche un objet [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) pour un chemin d’accès d’image de disque donné.</span><span class="sxs-lookup"><span data-stu-id="d69c4-104">Finds an [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) object for a given disk image path.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d69c4-105">Syntax</span></span>


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a><span data-ttu-id="d69c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d69c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d69c4-107">*SelectionCriterion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d69c4-107">*SelectionCriterion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c4-108">Chemin d’accès complet qui spécifie l’emplacement d’un fichier image de disque.</span><span class="sxs-lookup"><span data-stu-id="d69c4-108">A fully-qualified path that specifies the location of a disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="d69c4-109">*CriterionType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d69c4-109">*CriterionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c4-110">Type de critère à rechercher lors de la recherche de l’image de disque.</span><span class="sxs-lookup"><span data-stu-id="d69c4-110">The type of criterion to look for when finding the disk image.</span></span>

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d69c4-111">**inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d69c4-111">**unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

<span data-ttu-id="d69c4-112">**Chemin d’accès** (2)</span><span class="sxs-lookup"><span data-stu-id="d69c4-112">**Path** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d69c4-113">*Image* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d69c4-113">*Image* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c4-114">Référence au [**\_ MountedStorageImage MSVM**](msvm-mountedstorageimage.md) (peut avoir la valeur null si l’image n’est pas montée).</span><span class="sxs-lookup"><span data-stu-id="d69c4-114">A reference to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) (can be null if the image is not mounted).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d69c4-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d69c4-115">Return value</span></span>

<span data-ttu-id="d69c4-116">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d69c4-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d69c4-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="d69c4-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="d69c4-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="d69c4-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="d69c4-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="d69c4-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="d69c4-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="d69c4-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="d69c4-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="d69c4-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="d69c4-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="d69c4-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="d69c4-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="d69c4-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="d69c4-130">**Objet introuvable** (32789)</span><span class="sxs-lookup"><span data-stu-id="d69c4-130">**Object not found** (32789)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d69c4-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d69c4-131">Requirements</span></span>



| <span data-ttu-id="d69c4-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d69c4-132">Requirement</span></span> | <span data-ttu-id="d69c4-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d69c4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69c4-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d69c4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d69c4-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d69c4-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d69c4-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d69c4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d69c4-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d69c4-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d69c4-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d69c4-138">Namespace</span></span><br/>                | <span data-ttu-id="d69c4-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d69c4-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d69c4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d69c4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d69c4-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d69c4-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d69c4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d69c4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d69c4-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d69c4-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d69c4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d69c4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69c4-145">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="d69c4-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




