---
description: Interfaces d’encodeur
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203656"
---
# <a name="encoder-interfaces"></a><span data-ttu-id="c53bd-103">Interfaces d’encodeur</span><span class="sxs-lookup"><span data-stu-id="c53bd-103">Encoder Interfaces</span></span>


<span data-ttu-id="c53bd-104">Les tableaux suivants présentent les interfaces implémentées par les encodeurs WIC (Windows Imaging Component) et le diagramme de classes affiche la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="c53bd-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) encoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="c53bd-105">Interfaces d’encodeur Container-Level</span><span class="sxs-lookup"><span data-stu-id="c53bd-105">Container-Level Encoder Interfaces</span></span>



| <span data-ttu-id="c53bd-106">Interface</span><span class="sxs-lookup"><span data-stu-id="c53bd-106">Interface</span></span>                                                                                       | <span data-ttu-id="c53bd-107">Responsabilités</span><span class="sxs-lookup"><span data-stu-id="c53bd-107">Responsibilities</span></span>                             | <span data-ttu-id="c53bd-108">Implémentation</span><span class="sxs-lookup"><span data-stu-id="c53bd-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="c53bd-109">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="c53bd-109">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)                                             | <span data-ttu-id="c53bd-110">Services au niveau du conteneur</span><span class="sxs-lookup"><span data-stu-id="c53bd-110">Container-level services</span></span>                     | <span data-ttu-id="c53bd-111">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c53bd-111">Required</span></span>                                                                   |
| [<span data-ttu-id="c53bd-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="c53bd-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | <span data-ttu-id="c53bd-113">Notification de progression & la prise en charge de l’annulation</span><span class="sxs-lookup"><span data-stu-id="c53bd-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="c53bd-114">Recommandé</span><span class="sxs-lookup"><span data-stu-id="c53bd-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="c53bd-115">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="c53bd-115">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)                                 | <span data-ttu-id="c53bd-116">Services de sérialisation des métadonnées</span><span class="sxs-lookup"><span data-stu-id="c53bd-116">Metadata serialization services</span></span>              | <span data-ttu-id="c53bd-117">Facultatif (requis uniquement pour les formats qui prennent en charge les métadonnées au niveau du conteneur)</span><span class="sxs-lookup"><span data-stu-id="c53bd-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="c53bd-118">Interfaces d’encodeur Frame-Level</span><span class="sxs-lookup"><span data-stu-id="c53bd-118">Frame-Level Encoder Interfaces</span></span>



| <span data-ttu-id="c53bd-119">Interface</span><span class="sxs-lookup"><span data-stu-id="c53bd-119">Interface</span></span>                                                       | <span data-ttu-id="c53bd-120">Responsabilités</span><span class="sxs-lookup"><span data-stu-id="c53bd-120">Responsibilities</span></span>                | <span data-ttu-id="c53bd-121">Implémentation</span><span class="sxs-lookup"><span data-stu-id="c53bd-121">Implementation</span></span> |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [<span data-ttu-id="c53bd-122">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="c53bd-122">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)     | <span data-ttu-id="c53bd-123">Services au niveau de la trame</span><span class="sxs-lookup"><span data-stu-id="c53bd-123">Frame-level services</span></span>            | <span data-ttu-id="c53bd-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c53bd-124">Required</span></span>       |
| [<span data-ttu-id="c53bd-125">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="c53bd-125">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md) | <span data-ttu-id="c53bd-126">Services de sérialisation des métadonnées</span><span class="sxs-lookup"><span data-stu-id="c53bd-126">Metadata serialization services</span></span> | <span data-ttu-id="c53bd-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c53bd-127">Required</span></span>       |



 

![hiérarchie d’héritage de l’interface d’encodeur WIC](graphics/wicencoderinterfaces.png)

<span data-ttu-id="c53bd-129">Vous remarquerez que les interfaces de codeur sont presque des images miroir des interfaces de décodeur et que la plupart des méthodes sur ces interfaces correspondent à des méthodes sur les interfaces de décodeur associées.</span><span class="sxs-lookup"><span data-stu-id="c53bd-129">You'll notice that the encoder interfaces are almost mirror images of the decoder interfaces, and that most of the methods on these interfaces correspond to methods on the related decoder interfaces.</span></span> <span data-ttu-id="c53bd-130">Maintenant que vous êtes familiarisé avec l’implémentation d’un décodeur avec WIC activé, l’implémentation d’un encodeur prenant en charge WIC vous paraîtra également familière.</span><span class="sxs-lookup"><span data-stu-id="c53bd-130">Now that you're familiar with the implementation of a WIC-enabled decoder, the implementation of a WIC-enabled encoder will seem familiar as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c53bd-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c53bd-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c53bd-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c53bd-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c53bd-133">Implémentation d’un encodeur WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c53bd-133">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="c53bd-134">Implémentation de IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="c53bd-134">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="c53bd-135">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c53bd-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c53bd-136">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c53bd-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



