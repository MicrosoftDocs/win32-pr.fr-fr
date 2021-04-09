---
description: Cette rubrique fournit des instructions pour l’implémentation d’un décodeur ou d’un encodeur en tant que transformation de Media Foundation (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implémentation d’une table MFT de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210492"
---
# <a name="implementing-a-codec-mft"></a><span data-ttu-id="c95a9-103">Implémentation d’une table MFT de codec</span><span class="sxs-lookup"><span data-stu-id="c95a9-103">Implementing a Codec MFT</span></span>

<span data-ttu-id="c95a9-104">Cette rubrique fournit des instructions pour l’implémentation d’un décodeur ou d’un encodeur en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="c95a9-104">This topic provides some guidelines for implementing a decoder or encoder as a Media Foundation Transform (MFT) .</span></span>

-   [<span data-ttu-id="c95a9-105">Encodeurs</span><span class="sxs-lookup"><span data-stu-id="c95a9-105">Encoders</span></span>](#encoders)
    -   [<span data-ttu-id="c95a9-106">Négociation du format d’encodeur</span><span class="sxs-lookup"><span data-stu-id="c95a9-106">Encoder Format Negotiation</span></span>](#encoder-format-negotiation)
-   [<span data-ttu-id="c95a9-107">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="c95a9-107">Decoders</span></span>](#decoders)
    -   [<span data-ttu-id="c95a9-108">Décodeurs de transcodage uniquement</span><span class="sxs-lookup"><span data-stu-id="c95a9-108">Transcode-Only Decoders</span></span>](#transcode-only-decoders)
    -   [<span data-ttu-id="c95a9-109">Attributs Telecine</span><span class="sxs-lookup"><span data-stu-id="c95a9-109">Telecine Attributes</span></span>](#telecine-attributes)
-   [<span data-ttu-id="c95a9-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c95a9-110">Related topics</span></span>](#related-topics)

## <a name="encoders"></a><span data-ttu-id="c95a9-111">Encodeurs</span><span class="sxs-lookup"><span data-stu-id="c95a9-111">Encoders</span></span>

### <a name="encoder-format-negotiation"></a><span data-ttu-id="c95a9-112">Négociation du format d’encodeur</span><span class="sxs-lookup"><span data-stu-id="c95a9-112">Encoder Format Negotiation</span></span>

<span data-ttu-id="c95a9-113">La procédure suivante est utilisée pour initialiser un encodeur :</span><span class="sxs-lookup"><span data-stu-id="c95a9-113">The following procedure is used to initialize an encoder:</span></span>

1.  <span data-ttu-id="c95a9-114">Interrogez la MFT pour l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="c95a9-114">Query the MFT for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
2.  <span data-ttu-id="c95a9-115">Appelez [**ICodecAPI :: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) pour définir les propriétés d’encodage.</span><span class="sxs-lookup"><span data-stu-id="c95a9-115">Call [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) to set encoding properties.</span></span>
3.  <span data-ttu-id="c95a9-116">Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le format d’encodage.</span><span class="sxs-lookup"><span data-stu-id="c95a9-116">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the encoding format.</span></span>
4.  <span data-ttu-id="c95a9-117">Appelez [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) pour obtenir la liste des types d’entrée compatibles.</span><span class="sxs-lookup"><span data-stu-id="c95a9-117">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to get a list of compatible input types.</span></span> <span data-ttu-id="c95a9-118">(Cette étape peut être ignorée.)</span><span class="sxs-lookup"><span data-stu-id="c95a9-118">(This step might be skipped.)</span></span>
5.  <span data-ttu-id="c95a9-119">Appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le format d’entrée non compressé.</span><span class="sxs-lookup"><span data-stu-id="c95a9-119">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed input format.</span></span>

<span data-ttu-id="c95a9-120">Une fois que le type de sortie est défini à l’étape 3, la méthode [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) doit retourner une liste de types d’entrée compatibles avec le type de sortie actuel.</span><span class="sxs-lookup"><span data-stu-id="c95a9-120">After the output type is set in step 3, the [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method must return a list of input types that are compatible with the current output type.</span></span> <span data-ttu-id="c95a9-121">En d’autres termes, tous les types retournés par **GetInputAvailableType** à ce stade doivent être valides pour [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="c95a9-121">In other words, any types returned by **GetInputAvailableType** at this point must be valid for [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="c95a9-122">Pour les décodeurs, l’ordre dans lequel les types sont définis est inversé : le type d’entrée est défini en premier, suivi du type de sortie.</span><span class="sxs-lookup"><span data-stu-id="c95a9-122">For decoders, the order in which types are set is reversed: The input type is set first, followed by the output type.</span></span> <span data-ttu-id="c95a9-123">Une fois le type d’entrée défini, la méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) doit retourner une liste de types qui peuvent être passés à la méthode [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="c95a9-123">After the input type is set, the [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method must return a list of types that can be passed to the [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method.</span></span>

<span data-ttu-id="c95a9-124">Les encodeurs et les décodeurs doivent prendre en charge NV12 comme format non compressé courant.</span><span class="sxs-lookup"><span data-stu-id="c95a9-124">Encoders and decoders should support NV12 as a common uncompressed format.</span></span> <span data-ttu-id="c95a9-125">Cela permet de s’assurer que les composants de pipeline peuvent interagir avec des conversions colorspace minimales.</span><span class="sxs-lookup"><span data-stu-id="c95a9-125">This ensures that pipeline components can interoperate with minimal colorspace conversions.</span></span> <span data-ttu-id="c95a9-126">Bien entendu, d’autres formats peuvent également être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c95a9-126">Of course, other formats can be supported as well.</span></span>

## <a name="decoders"></a><span data-ttu-id="c95a9-127">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="c95a9-127">Decoders</span></span>

### <a name="transcode-only-decoders"></a><span data-ttu-id="c95a9-128">Décodeurs Transcode-Only</span><span class="sxs-lookup"><span data-stu-id="c95a9-128">Transcode-Only Decoders</span></span>

<span data-ttu-id="c95a9-129">Certains décodeurs sont optimisés pour le transcodage (décodage et recodage d’un flux) et ne peuvent pas être utilisés pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="c95a9-129">Some decoders are optimized for transcoding (decoding and then re-encoding a stream) and are not suitable for use during playback.</span></span>

<span data-ttu-id="c95a9-130">Si une table MFT du décodeur est destinée uniquement au transcodage, définissez l’indicateur de l' **\_ indicateur d’énumération MFT \_ \_ \_ uniquement** lorsque vous inscrivez la table MFT.</span><span class="sxs-lookup"><span data-stu-id="c95a9-130">If a decoder MFT is intended only for transcoding, set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when you register the MFT.</span></span> <span data-ttu-id="c95a9-131">(Voir [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span><span class="sxs-lookup"><span data-stu-id="c95a9-131">(See [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span></span>

<span data-ttu-id="c95a9-132">Par défaut, les décodeurs de transcodage ne sont pas retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="c95a9-132">By default, transcode decoders are not returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="c95a9-133">Pour énumérer les décodeurs de transcodage, appelez **MFTEnumEx** et définissez l’indicateur **MFT \_ enum enum \_ \_ \_ only** dans le paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="c95a9-133">To enumerate transcode decoders, call **MFTEnumEx** and set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in *Flags* parameter.</span></span> <span data-ttu-id="c95a9-134">Lorsqu’il est utilisé dans la fonction **MFTEnumEx** , cet indicateur énumère à la fois les décodeurs de transcodage et les autres décodeurs.</span><span class="sxs-lookup"><span data-stu-id="c95a9-134">When used in the **MFTEnumEx** function, this flag enumerated both transcode decoders and other decoders.</span></span>



| <span data-ttu-id="c95a9-135">**Indicateur d' \_ énumération MFT MFTRegister \_ \_ \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="c95a9-135">MFTRegister **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="c95a9-136">**Indicateur d' \_ énumération MFT MFTEnumEx \_ \_ \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="c95a9-136">MFTEnumEx **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="c95a9-137">La table MFT est-elle énumérée ?</span><span class="sxs-lookup"><span data-stu-id="c95a9-137">Is MFT Enumerated?</span></span> |
|--------------------------------------------------|------------------------------------------------|--------------------|
| <span data-ttu-id="c95a9-138">1</span><span class="sxs-lookup"><span data-stu-id="c95a9-138">1</span></span>                                                | <span data-ttu-id="c95a9-139">1</span><span class="sxs-lookup"><span data-stu-id="c95a9-139">1</span></span>                                              | <span data-ttu-id="c95a9-140">Oui</span><span class="sxs-lookup"><span data-stu-id="c95a9-140">Yes</span></span>                |
| <span data-ttu-id="c95a9-141">1</span><span class="sxs-lookup"><span data-stu-id="c95a9-141">1</span></span>                                                | <span data-ttu-id="c95a9-142">0</span><span class="sxs-lookup"><span data-stu-id="c95a9-142">0</span></span>                                              | <span data-ttu-id="c95a9-143">Non</span><span class="sxs-lookup"><span data-stu-id="c95a9-143">No</span></span>                 |
| <span data-ttu-id="c95a9-144">0</span><span class="sxs-lookup"><span data-stu-id="c95a9-144">0</span></span>                                                | <span data-ttu-id="c95a9-145">1</span><span class="sxs-lookup"><span data-stu-id="c95a9-145">1</span></span>                                              | <span data-ttu-id="c95a9-146">Oui</span><span class="sxs-lookup"><span data-stu-id="c95a9-146">Yes</span></span>                |
| <span data-ttu-id="c95a9-147">0</span><span class="sxs-lookup"><span data-stu-id="c95a9-147">0</span></span>                                                | <span data-ttu-id="c95a9-148">0</span><span class="sxs-lookup"><span data-stu-id="c95a9-148">0</span></span>                                              | <span data-ttu-id="c95a9-149">Oui</span><span class="sxs-lookup"><span data-stu-id="c95a9-149">Yes</span></span>                |



 

### <a name="telecine-attributes"></a><span data-ttu-id="c95a9-150">Attributs Telecine</span><span class="sxs-lookup"><span data-stu-id="c95a9-150">Telecine Attributes</span></span>

<span data-ttu-id="c95a9-151">La source du média peut attacher les attributs de télécinéma suivants aux exemples de supports qu’elle remet.</span><span class="sxs-lookup"><span data-stu-id="c95a9-151">The media source might attach the following telecine attributes to the media samples that it delivers.</span></span>



| <span data-ttu-id="c95a9-152">Attribut</span><span class="sxs-lookup"><span data-stu-id="c95a9-152">Attribute</span></span>                                                                                   | <span data-ttu-id="c95a9-153">Description</span><span class="sxs-lookup"><span data-stu-id="c95a9-153">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="c95a9-154">**MFSampleExtension \_ RepeatFirstField**</span><span class="sxs-lookup"><span data-stu-id="c95a9-154">**MFSampleExtension\_RepeatFirstField**</span></span>](mfsampleextension-repeatfirstfield-attribute.md) | <span data-ttu-id="c95a9-155">Équivaut à l’indicateur « REPEAT First Field » (RFF).</span><span class="sxs-lookup"><span data-stu-id="c95a9-155">Equivalent to "repeat first field" (RFF) flag.</span></span> |
| [<span data-ttu-id="c95a9-156">**MFSampleExtension \_ BottomFieldFirst**</span><span class="sxs-lookup"><span data-stu-id="c95a9-156">**MFSampleExtension\_BottomFieldFirst**</span></span>](mfsampleextension-bottomfieldfirst-attribute.md) | <span data-ttu-id="c95a9-157">Inverse de l’indicateur « Top Field First » (TFF).</span><span class="sxs-lookup"><span data-stu-id="c95a9-157">Inverse of "top field first" (TFF) flag.</span></span>       |



 

<span data-ttu-id="c95a9-158">Ces indicateurs fournissent un indicateur au convertisseur vidéo amélioré (EVR) lorsqu’il effectue une désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="c95a9-158">These flags provide a hint to the enhanced video renderer (EVR) when it performs deinterlacing.</span></span> <span data-ttu-id="c95a9-159">Un décodeur doit propager ces indicateurs en aval en les copiant dans les exemples de sortie, afin qu’ils atteignent le EVR.</span><span class="sxs-lookup"><span data-stu-id="c95a9-159">A decoder should propagate these flags downstream by copying them to the output samples, so that they reach the EVR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c95a9-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c95a9-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c95a9-161">Écriture d’une table MFT personnalisée</span><span class="sxs-lookup"><span data-stu-id="c95a9-161">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
