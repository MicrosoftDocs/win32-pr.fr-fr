---
description: Stratégie de métadonnées de la photo pour la propriété System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Stratégie de métadonnées de photo System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210282"
---
# <a name="systemdateacquired-photo-metadata-policy"></a><span data-ttu-id="d24c2-103">Stratégie de métadonnées de photo System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d24c2-103">System.DateAcquired Photo Metadata Policy</span></span>

<span data-ttu-id="d24c2-104">Stratégie de métadonnées de la photo pour la propriété [System. DateAcquired](../properties/props-system-dateacquired.md) .</span><span class="sxs-lookup"><span data-stu-id="d24c2-104">The photo metadata policy for the [System.DateAcquired](../properties/props-system-dateacquired.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d24c2-105">A-la</span><span class="sxs-lookup"><span data-stu-id="d24c2-105">PKEY</span></span>

<span data-ttu-id="d24c2-106">DateAcquired de la \_</span><span class="sxs-lookup"><span data-stu-id="d24c2-106">PKEY\_DateAcquired</span></span>

### <a name="containers"></a><span data-ttu-id="d24c2-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="d24c2-107">Containers</span></span>

<span data-ttu-id="d24c2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d24c2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d24c2-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d24c2-109">Read-Only</span></span>

<span data-ttu-id="d24c2-110">Non</span><span class="sxs-lookup"><span data-stu-id="d24c2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d24c2-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="d24c2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d24c2-112">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="d24c2-112">VT\_FILETIME</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="d24c2-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="d24c2-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="d24c2-114">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="d24c2-114">VT\_FILETIME</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d24c2-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="d24c2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d24c2-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="d24c2-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="d24c2-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="d24c2-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="d24c2-118">Si le fichier est au format JPEG, le gestionnaire recherche les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="d24c2-118">If the file is in JPEG format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="d24c2-119">Commande</span><span class="sxs-lookup"><span data-stu-id="d24c2-119">Order</span></span> | <span data-ttu-id="d24c2-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d24c2-120">Path</span></span>                             | <span data-ttu-id="d24c2-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d24c2-121">Disk Format</span></span>                        | <span data-ttu-id="d24c2-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d24c2-122">Required</span></span> |
|-------|----------------------------------|------------------------------------|----------|
| <span data-ttu-id="d24c2-123">1</span><span class="sxs-lookup"><span data-stu-id="d24c2-123">1</span></span>     | <span data-ttu-id="d24c2-124">/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d24c2-124">/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="d24c2-125">Chaîne Unicode au format de date XMP.</span><span class="sxs-lookup"><span data-stu-id="d24c2-125">Unicode string in XMP date format.</span></span> | <span data-ttu-id="d24c2-126">Oui</span><span class="sxs-lookup"><span data-stu-id="d24c2-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="d24c2-127">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="d24c2-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="d24c2-128">Si le fichier est au format TIFF, le gestionnaire recherche les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="d24c2-128">If the file is in TIFF format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="d24c2-129">Commande</span><span class="sxs-lookup"><span data-stu-id="d24c2-129">Order</span></span> | <span data-ttu-id="d24c2-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d24c2-130">Path</span></span>                                 | <span data-ttu-id="d24c2-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d24c2-131">Disk Format</span></span>                        | <span data-ttu-id="d24c2-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d24c2-132">Required</span></span> |
|-------|--------------------------------------|------------------------------------|----------|
| <span data-ttu-id="d24c2-133">1</span><span class="sxs-lookup"><span data-stu-id="d24c2-133">1</span></span>     | <span data-ttu-id="d24c2-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d24c2-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="d24c2-135">Chaîne Unicode au format de date XMP.</span><span class="sxs-lookup"><span data-stu-id="d24c2-135">Unicode string in XMP date format.</span></span> | <span data-ttu-id="d24c2-136">Oui</span><span class="sxs-lookup"><span data-stu-id="d24c2-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="d24c2-137">Notes</span><span class="sxs-lookup"><span data-stu-id="d24c2-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d24c2-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d24c2-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d24c2-139">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="d24c2-139">System.DateAcquired</span></span>](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
