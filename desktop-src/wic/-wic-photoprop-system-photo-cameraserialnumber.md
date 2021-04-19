---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. CameraSerialNumber.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Stratégie de métadonnées de photo System. photo. CameraSerialNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520722"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a><span data-ttu-id="66803-103">Stratégie de métadonnées de photo System. photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="66803-103">System.Photo.CameraSerialNumber Photo Metadata Policy</span></span>

<span data-ttu-id="66803-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="66803-104">The photo metadata policy for the [System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="66803-105">A-la</span><span class="sxs-lookup"><span data-stu-id="66803-105">PKEY</span></span>

<span data-ttu-id="66803-106">\_Photo \_ CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="66803-106">PKEY\_Photo\_CameraSerialNumber</span></span>

### <a name="containers"></a><span data-ttu-id="66803-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="66803-107">Containers</span></span>

<span data-ttu-id="66803-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="66803-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="66803-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66803-109">Read-Only</span></span>

<span data-ttu-id="66803-110">Non</span><span class="sxs-lookup"><span data-stu-id="66803-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="66803-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="66803-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="66803-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="66803-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="66803-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="66803-113">Input Type</span></span>

<span data-ttu-id="66803-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="66803-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="66803-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="66803-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="66803-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="66803-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="66803-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="66803-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="66803-118">Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données du chemin d’accès suivant :</span><span class="sxs-lookup"><span data-stu-id="66803-118">If the file is in JPEG format, the handler will read, write, and remove the data from the following path:</span></span>



| <span data-ttu-id="66803-119">Commande</span><span class="sxs-lookup"><span data-stu-id="66803-119">Order</span></span> | <span data-ttu-id="66803-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66803-120">Path</span></span>                                   | <span data-ttu-id="66803-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="66803-121">Disk Format</span></span> | <span data-ttu-id="66803-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66803-122">Required</span></span> |
|-------|----------------------------------------|-------------|----------|
| <span data-ttu-id="66803-123">1</span><span class="sxs-lookup"><span data-stu-id="66803-123">1</span></span>     | <span data-ttu-id="66803-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="66803-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="66803-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="66803-125">Unicode</span></span>     | <span data-ttu-id="66803-126">Oui</span><span class="sxs-lookup"><span data-stu-id="66803-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="66803-127">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="66803-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="66803-128">Si le fichier est au format TIFF, le gestionnaire lira, écrira et supprime les données du chemin d’accès suivant</span><span class="sxs-lookup"><span data-stu-id="66803-128">If the file is in TIFF format, the handler will read, write, and remove the data from the following path</span></span>



| <span data-ttu-id="66803-129">Commande</span><span class="sxs-lookup"><span data-stu-id="66803-129">Order</span></span> | <span data-ttu-id="66803-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66803-130">Path</span></span>                                       | <span data-ttu-id="66803-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="66803-131">Disk Format</span></span> | <span data-ttu-id="66803-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66803-132">Required</span></span> |
|-------|--------------------------------------------|-------------|----------|
| <span data-ttu-id="66803-133">1</span><span class="sxs-lookup"><span data-stu-id="66803-133">1</span></span>     | <span data-ttu-id="66803-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="66803-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="66803-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="66803-135">Unicode</span></span>     | <span data-ttu-id="66803-136">Oui</span><span class="sxs-lookup"><span data-stu-id="66803-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="66803-137">Notes</span><span class="sxs-lookup"><span data-stu-id="66803-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="66803-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66803-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66803-139">System. photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="66803-139">System.Photo.CameraSerialNumber</span></span>](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
