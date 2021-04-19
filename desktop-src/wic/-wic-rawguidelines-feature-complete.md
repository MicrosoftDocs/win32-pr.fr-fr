---
description: 'Exhaustivité des fonctionnalités : interfaces recommandées'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Exhaustivité des fonctionnalités : interfaces recommandées'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535500"
---
# <a name="feature-completeness-recommended-interfaces"></a><span data-ttu-id="38796-103">Exhaustivité des fonctionnalités : interfaces recommandées</span><span class="sxs-lookup"><span data-stu-id="38796-103">Feature Completeness: Recommended Interfaces</span></span>

<span data-ttu-id="38796-104">Le tableau suivant répertorie les codecs BRUTs des interfaces WIC (Windows Imaging Component) qui doivent être implémentés.</span><span class="sxs-lookup"><span data-stu-id="38796-104">The following table lists the Windows Imaging Component (WIC) interfaces RAW codecs should implement.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38796-105">Interface</span><span class="sxs-lookup"><span data-stu-id="38796-105">Interface</span></span></th>
<th><span data-ttu-id="38796-106">Obligatoire pour</span><span class="sxs-lookup"><span data-stu-id="38796-106">Required for</span></span></th>
<th><span data-ttu-id="38796-107">Description</span><span class="sxs-lookup"><span data-stu-id="38796-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38796-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span></span></td>
<td><span data-ttu-id="38796-109">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-109">Decoders</span></span></td>
<td><span data-ttu-id="38796-110">Représente le point de départ pour le décodage d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="38796-110">Represents the starting point for decoding an image file.</span></span> <span data-ttu-id="38796-111">Fournit l’accès aux propriétés au niveau du conteneur, telles que les miniatures, les frames et la palette.</span><span class="sxs-lookup"><span data-stu-id="38796-111">Provides access to container-level properties like thumbnails, frames, and palette.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38796-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span></span></td>
<td><span data-ttu-id="38796-113">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-113">Decoders</span></span></td>
<td><span data-ttu-id="38796-114">Représente un frame d’image spécifique dans le conteneur qui fournit l’accès aux propriétés de niveau image.</span><span class="sxs-lookup"><span data-stu-id="38796-114">Represents a specific image frame within the container that provides access to frame-level properties.</span></span> <span data-ttu-id="38796-115">Il s’agit de l’interface qui décode les bits d’image réels.</span><span class="sxs-lookup"><span data-stu-id="38796-115">This is the interface that decodes the actual image bits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38796-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span></span></td>
<td><span data-ttu-id="38796-117">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-117">Decoders</span></span></td>
<td><span data-ttu-id="38796-118">Requis pour énumérer et itérer au sein des blocs de métadonnées et appeler les lecteurs de métadonnées appropriés lors de la lecture à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="38796-118">Required for enumerating and iterating through metadata blocks and invoking the appropriate metadata readers when reading from an image file.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="38796-119">Si le format de conteneur brut est compatible TIFF ou utilise des IFD ou IRBs standard pour stocker les métadonnées EXIF ou XMP, les auteurs de codec peuvent choisir d’appeler les lecteurs de métadonnées intégrés plutôt que de les écrire.</span><span class="sxs-lookup"><span data-stu-id="38796-119">If the RAW container format is TIFF compatible or uses standard IFDs or IRBs to store EXIF or XMP metadata, codec authors can choose to invoke the built-in metadata readers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38796-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span></span></td>
<td><span data-ttu-id="38796-121">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-121">Decoders</span></span></td>
<td><span data-ttu-id="38796-122">Permet à l’appelant de spécifier la mise à l’échelle, le rognage, la rotation ou le format de pixel souhaités pour l’image décodée, ce qui peut améliorer considérablement les performances du décodeur.</span><span class="sxs-lookup"><span data-stu-id="38796-122">Allows the caller to specify desired scaling, cropping, rotation, or pixel format for the decoded image, which can significantly improve decoder performance.</span></span> <span data-ttu-id="38796-123">Par exemple, les décodeurs Microsoft JPEG et le protocole de datagramme sans fil (WDP) utilisent un schéma d’optimisation pyramidal pour accélérer le décodage lorsque la bitmap cible est plus petite que la bitmap source.</span><span class="sxs-lookup"><span data-stu-id="38796-123">For example, Microsoft's JPEG and Wireless Datagram Protocol (WDP) decoders use a pyramid optimization scheme to achieve faster decoding when the target bitmap is smaller than the source bitmap.</span></span> <span data-ttu-id="38796-124">Windows Vista (et versions ultérieures) tentera d’utiliser cette interface pour extraire une version &quot; &quot; préliminaire rapide d’une image brute chaque fois que la version préliminaire incorporée est manquante ou inférieure à 1 024 pixels dans sa plus grande dimension.</span><span class="sxs-lookup"><span data-stu-id="38796-124">Windows Vista (and later) will attempt to use this interface to extract a &quot;fast&quot; preview from a RAW image whenever the embedded preview is missing or less than 1,024 pixels in its largest dimension.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38796-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span></span></td>
<td><span data-ttu-id="38796-126">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-126">Decoders</span></span></td>
<td><span data-ttu-id="38796-127">Requis pour les formats BRUTs.</span><span class="sxs-lookup"><span data-stu-id="38796-127">Required for RAW formats.</span></span> <span data-ttu-id="38796-128">Expose les paramètres qui sont spécifiques au traitement des images BRUTes.</span><span class="sxs-lookup"><span data-stu-id="38796-128">Exposes parameters that are specific to RAW image processing.</span></span> <span data-ttu-id="38796-129">Les codecs BRUTs doivent prendre en charge autant de ces paramètres que s’appliquent au codec.</span><span class="sxs-lookup"><span data-stu-id="38796-129">RAW codecs should support as many of these parameters as apply to the codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38796-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span></span></td>
<td><span data-ttu-id="38796-131">Encodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-131">Encoders</span></span></td>
<td><span data-ttu-id="38796-132">Représente le point de départ pour l’encodage d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="38796-132">Represents the starting point for encoding an image file.</span></span> <span data-ttu-id="38796-133">Cette interface est utilisée pour définir les propriétés au niveau du conteneur, telles que les miniatures, les frames et la palette.</span><span class="sxs-lookup"><span data-stu-id="38796-133">This interface is used for setting container-level properties, such as thumbnails, frames, and palette.</span></span> <span data-ttu-id="38796-134">Il est également nécessaire d’appeler un enregistreur de métadonnées pour activer la persistance des métadonnées dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="38796-134">It is also required to invoke a metadata writer to enable metadata persistence to the image file.</span></span> <span data-ttu-id="38796-135">Pour ces raisons, cette interface est nécessaire même si l’encodage de la bitmap principale au format brut n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="38796-135">For these reasons, this interface is necessary even if encoding the primary bitmap to the RAW format is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38796-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span></span></td>
<td><span data-ttu-id="38796-137">Encodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-137">Encoders</span></span></td>
<td><span data-ttu-id="38796-138">Représente une image spécifique dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="38796-138">Represents a specific image frame within the container.</span></span> <span data-ttu-id="38796-139">Cette interface est utilisée pour encoder les bits d’image réels et pour définir des métadonnées et des propriétés par image.</span><span class="sxs-lookup"><span data-stu-id="38796-139">This interface is used to encode the actual image bits and to set per-frame metadata and properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38796-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span><span class="sxs-lookup"><span data-stu-id="38796-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span></span></td>
<td><span data-ttu-id="38796-141">Encodeurs</span><span class="sxs-lookup"><span data-stu-id="38796-141">Encoders</span></span></td>
<td><span data-ttu-id="38796-142">Requis pour itérer au sein des blocs de métadonnées et appeler les enregistreurs de métadonnées appropriés lors de la sérialisation d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="38796-142">Required for iterating through metadata blocks and invoking the appropriate metadata writers when serializing an image file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="38796-143">Si le format de conteneur brut est compatible TIFF, les auteurs de codec peuvent choisir d’appeler les enregistreurs de métadonnées intégrés plutôt que de les écrire.</span><span class="sxs-lookup"><span data-stu-id="38796-143">If the RAW container format is TIFF-compatible, codec authors can choose to invoke the built-in metadata writers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="38796-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38796-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="38796-145">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="38796-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38796-146">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="38796-146">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="38796-147">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="38796-147">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="38796-148">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="38796-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




