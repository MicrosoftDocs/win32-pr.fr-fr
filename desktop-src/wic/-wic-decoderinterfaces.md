---
description: Interfaces de décodeur
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces de décodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210285"
---
# <a name="decoder-interfaces"></a><span data-ttu-id="a7e57-103">Interfaces de décodeur</span><span class="sxs-lookup"><span data-stu-id="a7e57-103">Decoder Interfaces</span></span>

<span data-ttu-id="a7e57-104">Les tableaux suivants présentent les interfaces implémentées par les décodeurs WIC (Windows Imaging Component) et le diagramme de classes affiche la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="a7e57-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) decoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="a7e57-105">Interfaces de décodeur Container-Level</span><span class="sxs-lookup"><span data-stu-id="a7e57-105">Container-Level Decoder Interfaces</span></span>



| <span data-ttu-id="a7e57-106">Interface</span><span class="sxs-lookup"><span data-stu-id="a7e57-106">Interface</span></span>                                                                                       | <span data-ttu-id="a7e57-107">Responsabilités</span><span class="sxs-lookup"><span data-stu-id="a7e57-107">Responsibilities</span></span>                             | <span data-ttu-id="a7e57-108">Implémentation</span><span class="sxs-lookup"><span data-stu-id="a7e57-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="a7e57-109">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="a7e57-109">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)                                             | <span data-ttu-id="a7e57-110">Services au niveau du conteneur</span><span class="sxs-lookup"><span data-stu-id="a7e57-110">Container-level services</span></span>                     | <span data-ttu-id="a7e57-111">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a7e57-111">Required</span></span>                                                                   |
| [<span data-ttu-id="a7e57-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="a7e57-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | <span data-ttu-id="a7e57-113">Notification de progression & la prise en charge de l’annulation</span><span class="sxs-lookup"><span data-stu-id="a7e57-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="a7e57-114">Recommandé</span><span class="sxs-lookup"><span data-stu-id="a7e57-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="a7e57-115">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="a7e57-115">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)                                 | <span data-ttu-id="a7e57-116">Énumération des métadonnées</span><span class="sxs-lookup"><span data-stu-id="a7e57-116">Metadata enumeration</span></span>                         | <span data-ttu-id="a7e57-117">Facultatif (requis uniquement pour les formats qui prennent en charge les métadonnées au niveau du conteneur)</span><span class="sxs-lookup"><span data-stu-id="a7e57-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="a7e57-118">Interfaces de décodeur Frame-Level</span><span class="sxs-lookup"><span data-stu-id="a7e57-118">Frame-Level Decoder Interfaces</span></span>



| <span data-ttu-id="a7e57-119">Interface</span><span class="sxs-lookup"><span data-stu-id="a7e57-119">Interface</span></span>                                                           | <span data-ttu-id="a7e57-120">Responsabilités</span><span class="sxs-lookup"><span data-stu-id="a7e57-120">Responsibilities</span></span>          | <span data-ttu-id="a7e57-121">Implémentation</span><span class="sxs-lookup"><span data-stu-id="a7e57-121">Implementation</span></span>                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [<span data-ttu-id="a7e57-122">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="a7e57-122">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)         | <span data-ttu-id="a7e57-123">Services au niveau de la trame</span><span class="sxs-lookup"><span data-stu-id="a7e57-123">Frame-level services</span></span>      | <span data-ttu-id="a7e57-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a7e57-124">Required</span></span>                      |
| [<span data-ttu-id="a7e57-125">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="a7e57-125">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)     | <span data-ttu-id="a7e57-126">Énumération des métadonnées</span><span class="sxs-lookup"><span data-stu-id="a7e57-126">Metadata enumeration</span></span>      | <span data-ttu-id="a7e57-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a7e57-127">Required</span></span>                      |
| [<span data-ttu-id="a7e57-128">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="a7e57-128">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md) | <span data-ttu-id="a7e57-129">Transformations du décodeur natif</span><span class="sxs-lookup"><span data-stu-id="a7e57-129">Native decoder transforms</span></span> | <span data-ttu-id="a7e57-130">Recommandé</span><span class="sxs-lookup"><span data-stu-id="a7e57-130">Recommended</span></span>                   |
| [<span data-ttu-id="a7e57-131">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="a7e57-131">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)                       | <span data-ttu-id="a7e57-132">Services de traitement brut</span><span class="sxs-lookup"><span data-stu-id="a7e57-132">Raw processing services</span></span>   | <span data-ttu-id="a7e57-133">Obligatoire pour les formats bruts uniquement</span><span class="sxs-lookup"><span data-stu-id="a7e57-133">Required for Raw formats only</span></span> |



 

![hiérarchie d’héritage de l’interface WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a><span data-ttu-id="a7e57-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7e57-135">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a7e57-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a7e57-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7e57-137">Implémentation d’un décodeur WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="a7e57-137">Implementing a WIC-Enabled Decoder</span></span>](-wic-implementingwicdecoder.md)
</dt> <dt>

[<span data-ttu-id="a7e57-138">Implémentation de IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="a7e57-138">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="a7e57-139">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="a7e57-139">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="a7e57-140">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="a7e57-140">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



