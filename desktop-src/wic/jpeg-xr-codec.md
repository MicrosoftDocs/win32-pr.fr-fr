---
description: Le codec XR JPEG natif est disponible via le composant WIC (Windows Imaging Component). Le format JPEG XR, que le codec prend en charge, est conçu pour la photographie numérique des consommateurs et des professionnels.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Vue d’ensemble du codec XR JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520695"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="265b9-104">Vue d’ensemble du codec XR JPEG</span><span class="sxs-lookup"><span data-stu-id="265b9-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="265b9-105">Le codec XR JPEG natif est disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="265b9-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="265b9-106">Le format JPEG XR, que le codec prend en charge, est conçu pour la photographie numérique des consommateurs et des professionnels.</span><span class="sxs-lookup"><span data-stu-id="265b9-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="265b9-107">Le format JPEG XR peut atteindre jusqu’à deux fois l’efficacité de la compression du format JPEG d’origine, avec des artefacts de compression moins perceptibles.</span><span class="sxs-lookup"><span data-stu-id="265b9-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="265b9-108">Les fonctionnalités des XR JPEG sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="265b9-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="265b9-109">Prise en charge des images monochrome, RVB, CMJN et n-Channel</span><span class="sxs-lookup"><span data-stu-id="265b9-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="265b9-110">formats d’entier 8, 16 et 32 bits</span><span class="sxs-lookup"><span data-stu-id="265b9-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="265b9-111">Des formats à plage dynamique élevée, à large gamme, utilisant des valeurs de couleur à virgule fixe ou à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="265b9-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="265b9-112">Décodage progressif</span><span class="sxs-lookup"><span data-stu-id="265b9-112">Progressive decoding</span></span>
-   <span data-ttu-id="265b9-113">Encodage avec ou sans perte utilisant le même algorithme de compression</span><span class="sxs-lookup"><span data-stu-id="265b9-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="265b9-114">Prise en charge du décodage des régions d’intérêt dans les grandes images</span><span class="sxs-lookup"><span data-stu-id="265b9-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="265b9-115">Le format JPEG XR est défini dans les documents standard suivants :</span><span class="sxs-lookup"><span data-stu-id="265b9-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="265b9-116">ITU-T T. 832 : *Information Technology – système de codage d’images JPEG XR-spécification de codage d’image*</span><span class="sxs-lookup"><span data-stu-id="265b9-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="265b9-117">ISO/IEC 29199-2:2010 : *technologies de l’information : système de codage d’image XR JPEG, partie 2 : spécification de codage d’image*</span><span class="sxs-lookup"><span data-stu-id="265b9-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="265b9-118">La norme JPEG XR est en grande partie basée sur le format de [photo HD](hdphoto-format-overview.md) , mais il existe des différences entre les deux formats.</span><span class="sxs-lookup"><span data-stu-id="265b9-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="265b9-119">Dans Windows 8, le codec de photo HD a été mis à jour pour prendre en charge les XR JPEG.</span><span class="sxs-lookup"><span data-stu-id="265b9-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="265b9-120">Désormais, l’encodeur génère toujours un flux de bits conforme XR JPEG.</span><span class="sxs-lookup"><span data-stu-id="265b9-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="265b9-121">Le décodeur peut décoder des images JPEG XR et HD.</span><span class="sxs-lookup"><span data-stu-id="265b9-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="265b9-122">Des améliorations significatives des performances, par rapport au codec photo HD, ont été apportées au codec XR JPEG.</span><span class="sxs-lookup"><span data-stu-id="265b9-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="265b9-123">Par exemple, le décodage d’image de sous-résolution, tel que la génération de miniatures, a été amélioré, ainsi que le décodage d’image de faible résolution.</span><span class="sxs-lookup"><span data-stu-id="265b9-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="265b9-124">Nous vous recommandons d’utiliser le format JPEG XR au lieu du format HD photo.</span><span class="sxs-lookup"><span data-stu-id="265b9-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="265b9-125">Informations sur le codec</span><span class="sxs-lookup"><span data-stu-id="265b9-125">Codec Information</span></span>



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="265b9-126">Extension de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="265b9-126">File name extension</span></span> | <span data-ttu-id="265b9-127">« JXR » et « WDP »</span><span class="sxs-lookup"><span data-stu-id="265b9-127">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="265b9-128">GUID du conteneur</span><span class="sxs-lookup"><span data-stu-id="265b9-128">Container GUID</span></span>      | <span data-ttu-id="265b9-129">**GUID \_ ContainerFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="265b9-129">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="265b9-130">GUID du décodeur</span><span class="sxs-lookup"><span data-stu-id="265b9-130">Decoder GUID</span></span>        | <span data-ttu-id="265b9-131">**CLSID \_ WICWmpDecoder**</span><span class="sxs-lookup"><span data-stu-id="265b9-131">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="265b9-132">GUID de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="265b9-132">Encoder GUID</span></span>        | <span data-ttu-id="265b9-133">**CLSID \_ WICWmpEncoder**</span><span class="sxs-lookup"><span data-stu-id="265b9-133">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="265b9-134">Prise en charge des profils</span><span class="sxs-lookup"><span data-stu-id="265b9-134">Profile Support</span></span>     | <span data-ttu-id="265b9-135">L’encodeur et le décodeur prennent en charge jusqu’au profil principal et jusqu’au niveau 128.</span><span class="sxs-lookup"><span data-stu-id="265b9-135">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="265b9-136">Fonctionnalités du codec</span><span class="sxs-lookup"><span data-stu-id="265b9-136">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="265b9-137">Plage dynamique élevée</span><span class="sxs-lookup"><span data-stu-id="265b9-137">High Dynamic Range</span></span>

<span data-ttu-id="265b9-138">Le XR JPEG prend en charge les images de plage haute dynamique, à l’aide de couleurs à virgule flottante ou à virgule fixe.</span><span class="sxs-lookup"><span data-stu-id="265b9-138">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="265b9-139">Dans ces formats de couleurs, la plage numérique d’un pixel est supérieure à la plage visible. vous pouvez donc ajuster les couleurs au-dessus ou en dessous de la plage visible pendant les phases de traitement intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="265b9-139">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="265b9-140">Fixed-point : dans une représentation à virgule fixe, 0 représente le noir et 1,0 représente la saturation maximale.</span><span class="sxs-lookup"><span data-stu-id="265b9-140">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="265b9-141">Le codec XR JPEG prend en charge les formats à virgule fixe 16 bits et 32 bits.</span><span class="sxs-lookup"><span data-stu-id="265b9-141">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="265b9-142">Pour 16 bits, 1,0 = 0x2000h, qui donne 13 bits pour la plage visible \[ 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="265b9-142">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="265b9-143">La plage totale est comprise entre – 4,0 et + 3,999, et est mappée de manière linéaire.</span><span class="sxs-lookup"><span data-stu-id="265b9-143">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="265b9-144">Pour 32 bits, 1,0 = 0x01000000h, la plage visible est de 24 bits, tandis que la plage totale est comprise entre – 128 et + 127,999.</span><span class="sxs-lookup"><span data-stu-id="265b9-144">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="265b9-145">Virgule flottante : dans une représentation à virgule flottante, 0 représente le noir et 1,0 représente la saturation maximale.</span><span class="sxs-lookup"><span data-stu-id="265b9-145">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="265b9-146">Le codec XR JPEG prend en charge les formats à virgule flottante 16 bits et 32 bits.</span><span class="sxs-lookup"><span data-stu-id="265b9-146">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="265b9-147">Vignettes</span><span class="sxs-lookup"><span data-stu-id="265b9-147">Tiles</span></span>

<span data-ttu-id="265b9-148">Un frame peut être partitionné en sous-régions rectangulaires appelées *vignettes*.</span><span class="sxs-lookup"><span data-stu-id="265b9-148">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="265b9-149">Une vignette est une zone d’une image qui contient des tableaux rectangulaires de blocs macros.</span><span class="sxs-lookup"><span data-stu-id="265b9-149">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="265b9-150">Les vignettes permettent de décoder les zones de l’image sans traiter l’intégralité de l’image.</span><span class="sxs-lookup"><span data-stu-id="265b9-150">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="265b9-151">Pendant l’encodage, sélectionnez le nombre de vignettes en définissant les propriétés **HorizontalTileSlices** et **VerticalTileSlices** .</span><span class="sxs-lookup"><span data-stu-id="265b9-151">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="265b9-152">La taille minimale de la vignette est 16 × 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="265b9-152">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="265b9-153">L’encodeur ajuste le nombre de vignettes pour maintenir cette restriction.</span><span class="sxs-lookup"><span data-stu-id="265b9-153">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="265b9-154">Il existe une surcharge de stockage et de traitement associée à chaque vignette. vous devez donc prendre en compte le nombre de vignettes nécessaires pour des scénarios particuliers.</span><span class="sxs-lookup"><span data-stu-id="265b9-154">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="265b9-155">Sortie de flux d’image</span><span class="sxs-lookup"><span data-stu-id="265b9-155">Image Stream Output</span></span>

<span data-ttu-id="265b9-156">La norme JPEG-XR définit deux parties d’un fichier JPEG-XR :</span><span class="sxs-lookup"><span data-stu-id="265b9-156">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="265b9-157">Flux de bits d’image, défini dans le corps de la norme.</span><span class="sxs-lookup"><span data-stu-id="265b9-157">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="265b9-158">Conteneur d’images.</span><span class="sxs-lookup"><span data-stu-id="265b9-158">The image container.</span></span> <span data-ttu-id="265b9-159">Le fichier contient des métadonnées EXIF et XMP, et est défini dans l’annexe A de la norme.</span><span class="sxs-lookup"><span data-stu-id="265b9-159">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="265b9-160">Il est possible, et autorisé par la norme, d’incorporer le flux d’image à l’intérieur d’un autre type de conteneur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="265b9-160">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="265b9-161">L’encodeur prend en charge un mode de diffusion en continu, qui génère le flux binaire d’image brut sans conteneur d’images.</span><span class="sxs-lookup"><span data-stu-id="265b9-161">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="265b9-162">Une application peut stocker le flux binaire dans un autre format de conteneur.</span><span class="sxs-lookup"><span data-stu-id="265b9-162">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="265b9-163">Pour activer le mode de diffusion en continu uniquement, définissez la propriété **StreamOnly** .</span><span class="sxs-lookup"><span data-stu-id="265b9-163">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="265b9-164">Paramètres de qualité de l’image</span><span class="sxs-lookup"><span data-stu-id="265b9-164">Image Quality Settings</span></span>

<span data-ttu-id="265b9-165">Plusieurs propriétés de codec contrôlent la qualité de l’image de sortie à partir de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="265b9-165">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="265b9-166">[ImageQuality](#imagequality) est une propriété commune aux codecs WIC.</span><span class="sxs-lookup"><span data-stu-id="265b9-166">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="265b9-167">Elle spécifie la qualité de l’image en tant que valeur à virgule flottante unique comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="265b9-167">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="265b9-168">Les propriétés [Quality](#image-quality-settings), [chevauchement](#overlap)et [subéchantillonner](#subsampling) permettent de mieux contrôler les paramètres de qualité.</span><span class="sxs-lookup"><span data-stu-id="265b9-168">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="265b9-169">Pour utiliser les propriétés [Quality](#image-quality-settings), [chevauchement](#overlap)et [subéchantillonner](#subsampling) , affectez à la propriété [UseCodecOptions](#usecodecoptions) la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="265b9-169">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="265b9-170">Si [UseCodecOptions](#usecodecoptions) a la valeur **Variant \_ false** (la valeur de **type Variant \_ false** est la valeur par défaut), l’encodeur utilise la propriété [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="265b9-170">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="265b9-171">L’encodeur mappe la valeur de ImageQuality à la [qualité](#image-quality-settings), au [chevauchement](#overlap)et à l' [échantillonnage](#subsampling) par le biais d’une table de recherche.</span><span class="sxs-lookup"><span data-stu-id="265b9-171">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="265b9-172">L’encodeur ne prend pas en charge la propriété **CompressionQuality** .</span><span class="sxs-lookup"><span data-stu-id="265b9-172">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="265b9-173">Transcodage de domaine compressé</span><span class="sxs-lookup"><span data-stu-id="265b9-173">Compressed Domain Transcode</span></span>

<span data-ttu-id="265b9-174">Le codec XR JPEG peut effectuer certaines transformations d’image sans décoder les données compressées et les encoder.</span><span class="sxs-lookup"><span data-stu-id="265b9-174">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="265b9-175">Les opérations de domaine compressées sont très efficaces et évitent toute perte de qualité supplémentaire courante lorsque vous décodez et recodez une image compressée avec perte.</span><span class="sxs-lookup"><span data-stu-id="265b9-175">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="265b9-176">Les opérations de domaine compressées suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="265b9-176">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="265b9-177">Rogner une zone de l’image.</span><span class="sxs-lookup"><span data-stu-id="265b9-177">Crop a region of the image.</span></span>
-   <span data-ttu-id="265b9-178">Faire pivoter ou retourner l’image.</span><span class="sxs-lookup"><span data-stu-id="265b9-178">Rotate or flip the image.</span></span>
-   <span data-ttu-id="265b9-179">Ignorez les données de fréquence pour créer un fichier image plus petit.</span><span class="sxs-lookup"><span data-stu-id="265b9-179">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="265b9-180">Réorganisez l’image entre l’ordre spatial et l’ordre des fréquences.</span><span class="sxs-lookup"><span data-stu-id="265b9-180">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="265b9-181">L’encodeur XR JPEG utilise le transcodage de domaine compressé, si possible, lorsque l’image source est une image JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="265b9-181">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="265b9-182">Lorsque l’encodeur effectue une opération de domaine compressé, il ignore les propriétés de codec suivantes : [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), disposant d’un[chevauchement](#overlap) [sans perte](#lossless)et [qualité](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="265b9-182">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="265b9-183">Si les propriétés [HorizontalTileSlices](/windows) et [VerticalTileSlices](/windows) sont présentes, vous devez les affecter à zéro.</span><span class="sxs-lookup"><span data-stu-id="265b9-183">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="265b9-184">Vous ne pouvez pas modifier la taille des vignettes d’une image dans le cadre d’un transcodage de domaine compressé.</span><span class="sxs-lookup"><span data-stu-id="265b9-184">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="265b9-185">La liste de suivi décrit comment effectuer les transformations d’image.</span><span class="sxs-lookup"><span data-stu-id="265b9-185">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="265b9-186">Pour rogner l’image, définissez la région souhaitée dans le paramètre [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) de la méthode **WriteSource** .</span><span class="sxs-lookup"><span data-stu-id="265b9-186">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="265b9-187">Pour faire pivoter ou retourner l’image, définissez la propriété [BitmapTransform](#bitmaptransform) .</span><span class="sxs-lookup"><span data-stu-id="265b9-187">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="265b9-188">Pour ignorer les données de fréquence dans l’image, définissez la propriété [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="265b9-188">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="265b9-189">Pour ignorer les données de fréquence dans le canal alpha, définissez la propriété [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="265b9-189">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="265b9-190">L’abandon des données de fréquence réduit la taille des fichiers encodés et peut réduire la résolution.</span><span class="sxs-lookup"><span data-stu-id="265b9-190">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="265b9-191">Pour modifier l’organisation de l’image entre la fréquence et le classement spatial, définissez la propriété [FrequencyOrdering](/windows) .</span><span class="sxs-lookup"><span data-stu-id="265b9-191">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="265b9-192">Pour désactiver le transcodage de domaine compressé et forcer l’encodeur à recoder l’image, définissez [UseCodecOptions](#usecodecoptions) sur **Variant \_ true** et affectez à [CompressedDomainTranscode](#compresseddomaintranscode) la valeur **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="265b9-192">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="265b9-193">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="265b9-193">Encoder Options</span></span>

<span data-ttu-id="265b9-194">Pour définir les propriétés d’encodage, utilisez l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="265b9-194">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="265b9-195">Pour plus d’informations, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="265b9-195">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="265b9-196">La liste suivante spécifie les options de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="265b9-196">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="265b9-197">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="265b9-197">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="265b9-198">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="265b9-198">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="265b9-199">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="265b9-199">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="265b9-200">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="265b9-200">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="265b9-201">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="265b9-201">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="265b9-202">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="265b9-202">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="265b9-203">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="265b9-203">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="265b9-204">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="265b9-204">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="265b9-205">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="265b9-205">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="265b9-206">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-206">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="265b9-207">Lossless</span><span class="sxs-lookup"><span data-stu-id="265b9-207">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="265b9-208">Éviter</span><span class="sxs-lookup"><span data-stu-id="265b9-208">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="265b9-209">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="265b9-209">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="265b9-210">Qualité</span><span class="sxs-lookup"><span data-stu-id="265b9-210">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="265b9-211">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="265b9-211">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="265b9-212">Sous-échantillonnage</span><span class="sxs-lookup"><span data-stu-id="265b9-212">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="265b9-213">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="265b9-213">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="265b9-214">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="265b9-214">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="265b9-215">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="265b9-215">AlphaDataDiscard</span></span>

<span data-ttu-id="265b9-216">Définit la quantité de données de fréquence alpha à ignorer pendant un transcodage de domaine compressé.</span><span class="sxs-lookup"><span data-stu-id="265b9-216">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="265b9-217">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-217">Data type</span></span> | <span data-ttu-id="265b9-218">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-218">VARTYPE</span></span>     | <span data-ttu-id="265b9-219">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-219">Range</span></span> | <span data-ttu-id="265b9-220">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-220">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="265b9-221">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="265b9-221">**UCHAR**</span></span> | <span data-ttu-id="265b9-222">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-222">**VT\_UI1**</span></span> | <span data-ttu-id="265b9-223">0 – 4</span><span class="sxs-lookup"><span data-stu-id="265b9-223">0–4</span></span>   | <span data-ttu-id="265b9-224">Aucun</span><span class="sxs-lookup"><span data-stu-id="265b9-224">None</span></span>    |



 

<span data-ttu-id="265b9-225">Cette propriété s’applique uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode) a la valeur **Variant \_ true** et si l’image contient un canal alpha planaire ou un canal alpha entrelacé ; sinon, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="265b9-225">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="265b9-226">Pour les images qui contiennent un canal alpha planaire, les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="265b9-226">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="265b9-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="265b9-227">Value</span></span> | <span data-ttu-id="265b9-228">Description</span><span class="sxs-lookup"><span data-stu-id="265b9-228">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265b9-229">0</span><span class="sxs-lookup"><span data-stu-id="265b9-229">0</span></span>     | <span data-ttu-id="265b9-230">Aucune donnée de fréquence image n'est ignorée.</span><span class="sxs-lookup"><span data-stu-id="265b9-230">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="265b9-231">1</span><span class="sxs-lookup"><span data-stu-id="265b9-231">1</span></span>     | <span data-ttu-id="265b9-232">Les flexbits sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="265b9-232">The flexbits are discarded.</span></span> <span data-ttu-id="265b9-233">Cela réduit arbitrairement la qualité du canal alpha planaire pour l’image transcodée.</span><span class="sxs-lookup"><span data-stu-id="265b9-233">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="265b9-234">, sans modification de la résolution effective.</span><span class="sxs-lookup"><span data-stu-id="265b9-234">, without a change in the effective resolution.</span></span> <span data-ttu-id="265b9-235">La réduction exacte de la taille et de la qualité des fichiers dépend de nombreux facteurs et ne peut pas être spécifiée exactement.</span><span class="sxs-lookup"><span data-stu-id="265b9-235">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="265b9-236">2</span><span class="sxs-lookup"><span data-stu-id="265b9-236">2</span></span>     | <span data-ttu-id="265b9-237">La bande de données de fréquence à passage élevé est ignorée, y compris le flexbits.</span><span class="sxs-lookup"><span data-stu-id="265b9-237">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="265b9-238">Cela réduit efficacement la résolution du canal alpha planaire par un facteur de 4 dans les deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="265b9-238">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="265b9-239">Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque bloc 4x4 de pixels de canal alpha.</span><span class="sxs-lookup"><span data-stu-id="265b9-239">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="265b9-240">En règle générale, vous devez définir cette valeur uniquement lorsque la propriété [ImageDataDiscard](#imagedatadiscard) a la même valeur.</span><span class="sxs-lookup"><span data-stu-id="265b9-240">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="265b9-241">3</span><span class="sxs-lookup"><span data-stu-id="265b9-241">3</span></span>     | <span data-ttu-id="265b9-242">Les bandes de données de fréquence à passage rapide et à faible passage sont ignorées, y compris flexbits.</span><span class="sxs-lookup"><span data-stu-id="265b9-242">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="265b9-243">Ce ffectively réduit la résolution du canal alpha planaire par un facteur de 16 dans les deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="265b9-243">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="265b9-244">Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque 16x16 bloc macro de pixels de canal alpha.</span><span class="sxs-lookup"><span data-stu-id="265b9-244">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="265b9-245">En règle générale, vous devez définir cette valeur uniquement lorsque la propriété [ImageDataDiscard](#imagedatadiscard) a la même valeur.</span><span class="sxs-lookup"><span data-stu-id="265b9-245">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="265b9-246">4</span><span class="sxs-lookup"><span data-stu-id="265b9-246">4</span></span>     | <span data-ttu-id="265b9-247">Le canal alpha est complètement ignoré.</span><span class="sxs-lookup"><span data-stu-id="265b9-247">The alpha channel is completely discarded.</span></span> <span data-ttu-id="265b9-248">Le format de pixel de l’image transcodée est modifié pour refléter la suppression du canal alpha.</span><span class="sxs-lookup"><span data-stu-id="265b9-248">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="265b9-249">Pour les images qui contiennent un canal alpha entrelacé, la valeur suivante est valide.</span><span class="sxs-lookup"><span data-stu-id="265b9-249">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="265b9-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="265b9-250">Value</span></span> | <span data-ttu-id="265b9-251">Description</span><span class="sxs-lookup"><span data-stu-id="265b9-251">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265b9-252">4</span><span class="sxs-lookup"><span data-stu-id="265b9-252">4</span></span>     | <span data-ttu-id="265b9-253">Le canal alpha est complètement ignoré.</span><span class="sxs-lookup"><span data-stu-id="265b9-253">The alpha channel is completely discarded.</span></span> <span data-ttu-id="265b9-254">Le format de pixel de l’image transcodée est modifié pour refléter la suppression du canal alpha.</span><span class="sxs-lookup"><span data-stu-id="265b9-254">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="265b9-255">Pour Alpha entrelacé, sauf si cette propriété a la valeur 4, le canal alpha est traité de la même façon que les données de l’image, en fonction de la valeur de la propriété [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="265b9-255">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="265b9-256">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="265b9-256">AlphaQuality</span></span>

<span data-ttu-id="265b9-257">Définit la qualité de compression pour l’image de canal alpha planaire.</span><span class="sxs-lookup"><span data-stu-id="265b9-257">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="265b9-258">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-258">Data type</span></span> | <span data-ttu-id="265b9-259">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-259">VARTYPE</span></span>     | <span data-ttu-id="265b9-260">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-260">Range</span></span> | <span data-ttu-id="265b9-261">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-261">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="265b9-262">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="265b9-262">**UCHAR**</span></span> | <span data-ttu-id="265b9-263">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-263">**VT\_UI1**</span></span> | <span data-ttu-id="265b9-264">1 – 255</span><span class="sxs-lookup"><span data-stu-id="265b9-264">1–255</span></span> | <span data-ttu-id="265b9-265">1</span><span class="sxs-lookup"><span data-stu-id="265b9-265">1</span></span>       |



 

<span data-ttu-id="265b9-266">Cette propriété s’applique lorsque l’image a un canal alpha et que la propriété [InterleavedAlpha](#interleavedalpha) a la **\_ valeur false variant**.</span><span class="sxs-lookup"><span data-stu-id="265b9-266">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="265b9-267">La valeur 1 indique le mode sans perte.</span><span class="sxs-lookup"><span data-stu-id="265b9-267">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="265b9-268">L’augmentation des valeurs entraîne des taux de compression supérieurs et une qualité d’image inférieure.</span><span class="sxs-lookup"><span data-stu-id="265b9-268">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="265b9-269">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="265b9-269">BitmapTransform</span></span>

<span data-ttu-id="265b9-270">Spécifie si l’image est pivotée ou retournée quand elle est décodée.</span><span class="sxs-lookup"><span data-stu-id="265b9-270">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="265b9-271">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-271">Data type</span></span> | <span data-ttu-id="265b9-272">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-272">VARTYPE</span></span>     | <span data-ttu-id="265b9-273">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-273">Range</span></span>                                                                     | <span data-ttu-id="265b9-274">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-274">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="265b9-275">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="265b9-275">**UCHAR**</span></span> | <span data-ttu-id="265b9-276">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-276">**VT\_UI1**</span></span> | [<span data-ttu-id="265b9-277">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="265b9-277">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="265b9-278">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="265b9-278">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="265b9-279">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="265b9-279">CompressedDomainTranscode</span></span>

<span data-ttu-id="265b9-280">Active ou désactive le transcodage du domaine compressé.</span><span class="sxs-lookup"><span data-stu-id="265b9-280">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="265b9-281">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-281">Data type</span></span>         | <span data-ttu-id="265b9-282">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-282">VARTYPE</span></span>      | <span data-ttu-id="265b9-283">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-283">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="265b9-284">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-284">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-285">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-285">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-286">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="265b9-286">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="265b9-287">Pour désactiver les opérations de domaine compressé, affectez la valeur **\_ false** à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="265b9-287">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="265b9-288">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="265b9-288">FrequencyOrder</span></span>

<span data-ttu-id="265b9-289">Active l’encodage dans l’ordre des fréquences.</span><span class="sxs-lookup"><span data-stu-id="265b9-289">Enables encoding in frequency order.</span></span> <span data-ttu-id="265b9-290">Les implémentations d’appareils des encodeurs XR JPEG peuvent organiser un fichier dans l’ordre spatial pour réduire la mémoire requise lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="265b9-290">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="265b9-291">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-291">Data type</span></span>         | <span data-ttu-id="265b9-292">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-292">VARTYPE</span></span>      | <span data-ttu-id="265b9-293">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-293">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="265b9-294">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-294">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-295">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-295">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-296">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="265b9-296">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="265b9-297">**Variante \_ TRUE**: ordre des fréquences.</span><span class="sxs-lookup"><span data-stu-id="265b9-297">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="265b9-298">Les données de fréquence la plus basse apparaissent en premier dans le fichier, et le contenu de l’image est regroupé par sa fréquence plutôt que par son orientation spatiale.</span><span class="sxs-lookup"><span data-stu-id="265b9-298">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="265b9-299">L’organisation d’un fichier par ordre de fréquence offre les meilleures performances pour tout décodage basé sur les fréquences.</span><span class="sxs-lookup"><span data-stu-id="265b9-299">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="265b9-300">**Variante \_ FALSe**: ordre spatial.</span><span class="sxs-lookup"><span data-stu-id="265b9-300">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="265b9-301">L’ordre spatial réduit la mémoire requise pendant l’encodage</span><span class="sxs-lookup"><span data-stu-id="265b9-301">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="265b9-302">L’ordre des fréquences est recommandé, sauf si vous avez des raisons spécifiques aux performances ou à l’application d’utiliser l’ordre spatial.</span><span class="sxs-lookup"><span data-stu-id="265b9-302">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="265b9-303">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="265b9-303">HorizontalTileSlices</span></span>

<span data-ttu-id="265b9-304">Définit le nombre de mosaïques horizontales.</span><span class="sxs-lookup"><span data-stu-id="265b9-304">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="265b9-305">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-305">Data type</span></span>  | <span data-ttu-id="265b9-306">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-306">VARTYPE</span></span>     | <span data-ttu-id="265b9-307">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-307">Range</span></span>  | <span data-ttu-id="265b9-308">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-308">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="265b9-309">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="265b9-309">**USHORT**</span></span> | <span data-ttu-id="265b9-310">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-310">**VT\_UI2**</span></span> | <span data-ttu-id="265b9-311">de 0 à 4 095</span><span class="sxs-lookup"><span data-stu-id="265b9-311">0–4095</span></span> | <span data-ttu-id="265b9-312">(largeur d’image – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="265b9-312">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="265b9-313">La valeur est le nombre de sous-divisions horizontales ; autrement dit, le nombre de vignettes horizontales – 1.</span><span class="sxs-lookup"><span data-stu-id="265b9-313">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="265b9-314">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="265b9-314">IgnoreOverlap</span></span>

<span data-ttu-id="265b9-315">Spécifie comment l’encodeur gère les limites des vignettes pendant un transcodage de domaine compressé.</span><span class="sxs-lookup"><span data-stu-id="265b9-315">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="265b9-316">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-316">Data type</span></span>         | <span data-ttu-id="265b9-317">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-317">VARTYPE</span></span>      | <span data-ttu-id="265b9-318">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-318">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="265b9-319">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-319">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-320">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-320">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-321">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="265b9-321">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="265b9-322">Cette propriété est appliquée uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode) a la valeur **Variant \_ true** et qu’un transcodage de sous-région d’une ou plusieurs vignettes est effectué.</span><span class="sxs-lookup"><span data-stu-id="265b9-322">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="265b9-323">L’opération par défaut pour un transcodage de région consiste à développer la région demandée pour inclure les pixels environnants requis pour le décodage du chevauchement des bords de la région.</span><span class="sxs-lookup"><span data-stu-id="265b9-323">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="265b9-324">Si cette propriété a la valeur **Variant \_ true**, le codec ignore les pixels environnants, et seules les vignettes sélectionnées sont extraites.</span><span class="sxs-lookup"><span data-stu-id="265b9-324">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="265b9-325">Si l’image source n’est pas en mosaïque ou si la région demandée contient des vignettes partielles, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="265b9-325">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="265b9-326">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="265b9-326">ImageDataDiscard</span></span>

<span data-ttu-id="265b9-327">Définit la quantité de données de fréquence d’image à ignorer pendant un transcodage de domaine compressé.</span><span class="sxs-lookup"><span data-stu-id="265b9-327">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="265b9-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-328">Data type</span></span> | <span data-ttu-id="265b9-329">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-329">VARTYPE</span></span>     | <span data-ttu-id="265b9-330">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-330">Range</span></span> | <span data-ttu-id="265b9-331">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-331">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="265b9-332">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="265b9-332">**UCHAR**</span></span> | <span data-ttu-id="265b9-333">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-333">**VT\_UI1**</span></span> | <span data-ttu-id="265b9-334">0 – 3</span><span class="sxs-lookup"><span data-stu-id="265b9-334">0–3</span></span>   | <span data-ttu-id="265b9-335">0</span><span class="sxs-lookup"><span data-stu-id="265b9-335">0</span></span>       |



 

<span data-ttu-id="265b9-336">Cette propriété s’applique uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode) a la valeur **Variant \_ true**; sinon, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="265b9-336">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="265b9-337">Valeur</span><span class="sxs-lookup"><span data-stu-id="265b9-337">Value</span></span> | <span data-ttu-id="265b9-338">Description</span><span class="sxs-lookup"><span data-stu-id="265b9-338">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265b9-339">0</span><span class="sxs-lookup"><span data-stu-id="265b9-339">0</span></span>     | <span data-ttu-id="265b9-340">Aucune donnée de fréquence image n'est ignorée.</span><span class="sxs-lookup"><span data-stu-id="265b9-340">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="265b9-341">1</span><span class="sxs-lookup"><span data-stu-id="265b9-341">1</span></span>     | <span data-ttu-id="265b9-342">Les flexbits sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="265b9-342">The flexbits are discarded.</span></span> <span data-ttu-id="265b9-343">Cela réduit arbitrairement la qualité de l’image transcodée sans modifier la résolution effective de l’image.</span><span class="sxs-lookup"><span data-stu-id="265b9-343">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="265b9-344">La réduction exacte de la taille et de la qualité des fichiers dépend de nombreux facteurs et ne peut pas être spécifiée exactement.</span><span class="sxs-lookup"><span data-stu-id="265b9-344">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="265b9-345">Cette valeur retourne une erreur spécifiée pour un canal alpha entrelacé.</span><span class="sxs-lookup"><span data-stu-id="265b9-345">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="265b9-346">2</span><span class="sxs-lookup"><span data-stu-id="265b9-346">2</span></span>     | <span data-ttu-id="265b9-347">La bande de données de fréquence à passage élevé est ignorée, y compris le flexbits.</span><span class="sxs-lookup"><span data-stu-id="265b9-347">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="265b9-348">Cela réduit la résolution de l’image transcodée par un facteur de 4 dans les deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="265b9-348">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="265b9-349">Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque bloc 4x4 de pixels.</span><span class="sxs-lookup"><span data-stu-id="265b9-349">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="265b9-350">Par conséquent, l’image transcodée doit être sous-échantillonnée en conséquence chaque fois qu’elle est décodée.</span><span class="sxs-lookup"><span data-stu-id="265b9-350">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="265b9-351">3</span><span class="sxs-lookup"><span data-stu-id="265b9-351">3</span></span>     | <span data-ttu-id="265b9-352">Les bandes de données de fréquence à passage rapide et à faible passage sont ignorées, y compris flexbits.</span><span class="sxs-lookup"><span data-stu-id="265b9-352">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="265b9-353">Cela réduit la résolution de l’image transcodée par un facteur de 16 dans les deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="265b9-353">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="265b9-354">Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque bloc macro de 16 x 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="265b9-354">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="265b9-355">Par conséquent, l’image transcodée doit être sous-échantillonnée en conséquence chaque fois qu’elle est décodée.</span><span class="sxs-lookup"><span data-stu-id="265b9-355">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="265b9-356">Si l’image contient un canal alpha entrelacé, la valeur de [ImageDataDiscard](#imagedatadiscard) est appliquée au canal alpha, sauf si la propriété [AlphaDataDiscard](#alphadatadiscard) est définie sur 4, auquel cas le canal alpha est ignoré.</span><span class="sxs-lookup"><span data-stu-id="265b9-356">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="265b9-357">Pour une composante alpha planaire, les données de fréquence qui sont ignorées sont contrôlées par la propriété [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="265b9-357">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="265b9-358">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="265b9-358">ImageQuality</span></span>

<span data-ttu-id="265b9-359">Définit la qualité de l’image.</span><span class="sxs-lookup"><span data-stu-id="265b9-359">Sets the image quality.</span></span>



| <span data-ttu-id="265b9-360">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-360">Data type</span></span> | <span data-ttu-id="265b9-361">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-361">VARTYPE</span></span>    | <span data-ttu-id="265b9-362">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-362">Range</span></span> | <span data-ttu-id="265b9-363">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-363">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="265b9-364">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="265b9-364">**FLOAT**</span></span> | <span data-ttu-id="265b9-365">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="265b9-365">**VT\_R4**</span></span> | <span data-ttu-id="265b9-366">0 – 1.0</span><span class="sxs-lookup"><span data-stu-id="265b9-366">0–1.0</span></span> | <span data-ttu-id="265b9-367">0.9</span><span class="sxs-lookup"><span data-stu-id="265b9-367">0.9</span></span>     |



 

<span data-ttu-id="265b9-368">Le niveau 1,0 donne une compression mathématiquement sans perte.</span><span class="sxs-lookup"><span data-stu-id="265b9-368">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="265b9-369">Le niveau 0,0 est le paramètre de qualité le plus bas.</span><span class="sxs-lookup"><span data-stu-id="265b9-369">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="265b9-370">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-370">InterleavedAlpha</span></span>

<span data-ttu-id="265b9-371">Spécifie s’il faut encoder l’alpha entrelacé ou le plan alpha entrelacé.</span><span class="sxs-lookup"><span data-stu-id="265b9-371">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="265b9-372">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-372">Data type</span></span>         | <span data-ttu-id="265b9-373">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-373">VARTYPE</span></span>      | <span data-ttu-id="265b9-374">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-374">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="265b9-375">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-375">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-376">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-376">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-377">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="265b9-377">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="265b9-378">**Variante \_ TRUE**: alpha entrelacé.</span><span class="sxs-lookup"><span data-stu-id="265b9-378">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="265b9-379">Les informations de canal alpha sont encodées sous la forme d’un canal entrelacé supplémentaire, sans corrélation avec les canaux de contenu d’image.</span><span class="sxs-lookup"><span data-stu-id="265b9-379">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="265b9-380">Ce mode est utile pour décoder alpha simultanément avec l’image lorsque l’image est diffusée en continu.</span><span class="sxs-lookup"><span data-stu-id="265b9-380">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="265b9-381">VARIANTE \_ false : alpha planaire.</span><span class="sxs-lookup"><span data-stu-id="265b9-381">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="265b9-382">Un canal alpha planaire est encodé sous la forme d’une image distincte.</span><span class="sxs-lookup"><span data-stu-id="265b9-382">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="265b9-383">Les données d’image et le canal alpha sont décodés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="265b9-383">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="265b9-384">Si vous le souhaitez, vous pouvez définir le niveau de qualité du canal alpha en définissant la propriété [AlphaQuality](#alphaquality) .</span><span class="sxs-lookup"><span data-stu-id="265b9-384">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="265b9-385">L’alpha entrelacé est pris en charge uniquement pour certains formats de pixel RVB.</span><span class="sxs-lookup"><span data-stu-id="265b9-385">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="265b9-386">L’alpha planaire est pris en charge pour tout format d’image qui définit un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="265b9-386">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="265b9-387">Lossless</span><span class="sxs-lookup"><span data-stu-id="265b9-387">Lossless</span></span>

<span data-ttu-id="265b9-388">Active la compression des pertes.</span><span class="sxs-lookup"><span data-stu-id="265b9-388">Enables losses compression.</span></span>



| <span data-ttu-id="265b9-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-389">Data type</span></span>         | <span data-ttu-id="265b9-390">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-390">VARTYPE</span></span>      | <span data-ttu-id="265b9-391">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-391">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="265b9-392">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-392">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-393">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-393">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-394">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="265b9-394">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="265b9-395">Si la valeur est **\_ true**, l’encodeur utilise la compression sans perte.</span><span class="sxs-lookup"><span data-stu-id="265b9-395">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="265b9-396">Lorsque la valeur **Variant est \_ true**, cette propriété remplace la propriété [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="265b9-396">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="265b9-397">Chevauchement</span><span class="sxs-lookup"><span data-stu-id="265b9-397">Overlap</span></span>

<span data-ttu-id="265b9-398">Définit le niveau de filtrage de chevauchement.</span><span class="sxs-lookup"><span data-stu-id="265b9-398">Sets the level of overlap filtering.</span></span> <span data-ttu-id="265b9-399">Avec le filtrage de chevauchement, les coefficients de transformation sont appliqués entre les limites Block et bloc macro.</span><span class="sxs-lookup"><span data-stu-id="265b9-399">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="265b9-400">Cela peut réduire les artefacts de blocage.</span><span class="sxs-lookup"><span data-stu-id="265b9-400">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="265b9-401">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-401">Data type</span></span> | <span data-ttu-id="265b9-402">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-402">VARTYPE</span></span>     | <span data-ttu-id="265b9-403">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-403">Range</span></span> | <span data-ttu-id="265b9-404">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-404">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="265b9-405">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="265b9-405">**UCHAR**</span></span> | <span data-ttu-id="265b9-406">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-406">**VT\_UI1**</span></span> | <span data-ttu-id="265b9-407">0 – 4</span><span class="sxs-lookup"><span data-stu-id="265b9-407">0–4</span></span>   | <span data-ttu-id="265b9-408">1</span><span class="sxs-lookup"><span data-stu-id="265b9-408">1</span></span>       |



 



| <span data-ttu-id="265b9-409">Valeur</span><span class="sxs-lookup"><span data-stu-id="265b9-409">Value</span></span> | <span data-ttu-id="265b9-410">Description</span><span class="sxs-lookup"><span data-stu-id="265b9-410">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="265b9-411">0</span><span class="sxs-lookup"><span data-stu-id="265b9-411">0</span></span>     | <span data-ttu-id="265b9-412">Aucun chevauchement.</span><span class="sxs-lookup"><span data-stu-id="265b9-412">No overlap.</span></span>                                   |
| <span data-ttu-id="265b9-413">1</span><span class="sxs-lookup"><span data-stu-id="265b9-413">1</span></span>     | <span data-ttu-id="265b9-414">Un niveau de chevauchement, une mosaïque floue.</span><span class="sxs-lookup"><span data-stu-id="265b9-414">One level of overlap, soft tiling.</span></span> <span data-ttu-id="265b9-415">(valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="265b9-415">(Default.)</span></span> |
| <span data-ttu-id="265b9-416">2</span><span class="sxs-lookup"><span data-stu-id="265b9-416">2</span></span>     | <span data-ttu-id="265b9-417">Deux niveaux de chevauchement, mosaïques floues.</span><span class="sxs-lookup"><span data-stu-id="265b9-417">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="265b9-418">3</span><span class="sxs-lookup"><span data-stu-id="265b9-418">3</span></span>     | <span data-ttu-id="265b9-419">Un niveau de chevauchement, une mosaïque matérielle</span><span class="sxs-lookup"><span data-stu-id="265b9-419">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="265b9-420">4</span><span class="sxs-lookup"><span data-stu-id="265b9-420">4</span></span>     | <span data-ttu-id="265b9-421">Deux niveaux de chevauchement, en mosaïque matérielle.</span><span class="sxs-lookup"><span data-stu-id="265b9-421">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="265b9-422">Définitions :</span><span class="sxs-lookup"><span data-stu-id="265b9-422">Definitions:</span></span>

-   <span data-ttu-id="265b9-423">Un niveau de chevauchement : les valeurs encodées des blocs 4x4 sont modifiées en fonction des blocs voisins.</span><span class="sxs-lookup"><span data-stu-id="265b9-423">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="265b9-424">Deux niveaux de chevauchement : le premier niveau de chevauchement est appliqué.</span><span class="sxs-lookup"><span data-stu-id="265b9-424">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="265b9-425">En outre, les valeurs encodées de 16x16 blocs macros sont modifiées en fonction du blocs macros voisin.</span><span class="sxs-lookup"><span data-stu-id="265b9-425">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="265b9-426">Mosaïque douce : le filtrage de chevauchement est appliqué à travers les limites des vignettes.</span><span class="sxs-lookup"><span data-stu-id="265b9-426">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="265b9-427">Mosaïque matérielle : le filtrage de chevauchement n’est pas appliqué sur les limites de la vignette.</span><span class="sxs-lookup"><span data-stu-id="265b9-427">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="265b9-428">Les vignettes matérielles peuvent introduire des artefacts visuels avec les limites de la vignette.</span><span class="sxs-lookup"><span data-stu-id="265b9-428">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="265b9-429">Si vous définissez cette propriété, affectez également à [UseCodecOptions](#usecodecoptions) la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="265b9-429">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="265b9-430">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="265b9-430">ProgressiveMode</span></span>

<span data-ttu-id="265b9-431">Active ou désactive l’encodage progressif.</span><span class="sxs-lookup"><span data-stu-id="265b9-431">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="265b9-432">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-432">Data type</span></span>         | <span data-ttu-id="265b9-433">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-433">VARTYPE</span></span>      | <span data-ttu-id="265b9-434">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-434">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="265b9-435">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-435">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-436">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-436">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-437">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="265b9-437">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="265b9-438">Valeur</span><span class="sxs-lookup"><span data-stu-id="265b9-438">Value</span></span>              | <span data-ttu-id="265b9-439">Description</span><span class="sxs-lookup"><span data-stu-id="265b9-439">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="265b9-440">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="265b9-440">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="265b9-441">Mode séquentiel (par défaut).</span><span class="sxs-lookup"><span data-stu-id="265b9-441">Sequential mode (default).</span></span> |
| <span data-ttu-id="265b9-442">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="265b9-442">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="265b9-443">Mode progressive.</span><span class="sxs-lookup"><span data-stu-id="265b9-443">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="265b9-444">Qualité</span><span class="sxs-lookup"><span data-stu-id="265b9-444">Quality</span></span>

<span data-ttu-id="265b9-445">Définit la qualité de compression.</span><span class="sxs-lookup"><span data-stu-id="265b9-445">Sets the compression quality.</span></span>



| <span data-ttu-id="265b9-446">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-446">Data type</span></span> | <span data-ttu-id="265b9-447">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-447">VARTYPE</span></span>     | <span data-ttu-id="265b9-448">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-448">Range</span></span> | <span data-ttu-id="265b9-449">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-449">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="265b9-450">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="265b9-450">**UCHAR**</span></span> | <span data-ttu-id="265b9-451">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-451">**VT\_UI1**</span></span> | <span data-ttu-id="265b9-452">1 – 255</span><span class="sxs-lookup"><span data-stu-id="265b9-452">1–255</span></span> | <span data-ttu-id="265b9-453">1</span><span class="sxs-lookup"><span data-stu-id="265b9-453">1</span></span>       |



 

<span data-ttu-id="265b9-454">La valeur 1 indique le mode sans perte.</span><span class="sxs-lookup"><span data-stu-id="265b9-454">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="265b9-455">L’augmentation des valeurs entraîne des taux de compression supérieurs et une qualité d’image inférieure.</span><span class="sxs-lookup"><span data-stu-id="265b9-455">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="265b9-456">Si vous définissez cette propriété, affectez également à [UseCodecOptions](#usecodecoptions) la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="265b9-456">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="265b9-457">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="265b9-457">StreamOnly</span></span>

<span data-ttu-id="265b9-458">Active ou désactive le mode de diffusion en continu uniquement.</span><span class="sxs-lookup"><span data-stu-id="265b9-458">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="265b9-459">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-459">Data type</span></span>         | <span data-ttu-id="265b9-460">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-460">VARTYPE</span></span>      | <span data-ttu-id="265b9-461">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-461">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="265b9-462">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-462">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-463">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-463">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-464">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="265b9-464">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="265b9-465">Valeur</span><span class="sxs-lookup"><span data-stu-id="265b9-465">Value</span></span>              | <span data-ttu-id="265b9-466">Description</span><span class="sxs-lookup"><span data-stu-id="265b9-466">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="265b9-467">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="265b9-467">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="265b9-468">L’encodeur génère le flux d’images brutes sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="265b9-468">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="265b9-469">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="265b9-469">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="265b9-470">L’encodeur génère le format de conteneur (flux d’image et métadonnées).</span><span class="sxs-lookup"><span data-stu-id="265b9-470">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="265b9-471">Sous-échantillonnage</span><span class="sxs-lookup"><span data-stu-id="265b9-471">Subsampling</span></span>

<span data-ttu-id="265b9-472">Définit le sous-échantillonnage de chrominance.</span><span class="sxs-lookup"><span data-stu-id="265b9-472">Sets the chroma subsampling.</span></span> <span data-ttu-id="265b9-473">Cette propriété s’applique uniquement aux images RVB.</span><span class="sxs-lookup"><span data-stu-id="265b9-473">This property applies only to RGB images.</span></span>



| <span data-ttu-id="265b9-474">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-474">Data type</span></span> | <span data-ttu-id="265b9-475">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-475">VARTYPE</span></span>     | <span data-ttu-id="265b9-476">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-476">Range</span></span> | <span data-ttu-id="265b9-477">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-477">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="265b9-478">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="265b9-478">**UCHAR**</span></span> | <span data-ttu-id="265b9-479">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-479">**VT\_UI1**</span></span> | <span data-ttu-id="265b9-480">0 – 3</span><span class="sxs-lookup"><span data-stu-id="265b9-480">0–3</span></span>   | <span data-ttu-id="265b9-481">3 Si [ImageQuality](#imagequality) > 0,8 ; sinon 1</span><span class="sxs-lookup"><span data-stu-id="265b9-481">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="265b9-482">Valeur</span><span class="sxs-lookup"><span data-stu-id="265b9-482">Value</span></span></th>
<th><span data-ttu-id="265b9-483">Description</span><span class="sxs-lookup"><span data-stu-id="265b9-483">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="265b9-484">3</span><span class="sxs-lookup"><span data-stu-id="265b9-484">3</span></span></td>
<td><span data-ttu-id="265b9-485">encodage 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="265b9-485">4:4:4 encoding.</span></span> <span data-ttu-id="265b9-486">Préserve la résolution complète de Chroma.</span><span class="sxs-lookup"><span data-stu-id="265b9-486">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="265b9-487">2</span><span class="sxs-lookup"><span data-stu-id="265b9-487">2</span></span></td>
<td><span data-ttu-id="265b9-488">encodage 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="265b9-488">4:2:2 encoding.</span></span> <span data-ttu-id="265b9-489">La résolution Chroma est 1/2 de la résolution de luminance.</span><span class="sxs-lookup"><span data-stu-id="265b9-489">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="265b9-490">1</span><span class="sxs-lookup"><span data-stu-id="265b9-490">1</span></span></td>
<td><span data-ttu-id="265b9-491">encodage 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="265b9-491">4:2:0 encoding.</span></span> <span data-ttu-id="265b9-492">La résolution Chroma est 1/4 de la résolution de luminance.</span><span class="sxs-lookup"><span data-stu-id="265b9-492">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="265b9-493">0</span><span class="sxs-lookup"><span data-stu-id="265b9-493">0</span></span></td>
<td><span data-ttu-id="265b9-494">Encodage 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="265b9-494">4:0:0 encoding.</span></span> <span data-ttu-id="265b9-495">Ignore toutes les valeurs de chrominance et conserve uniquement la luminance.</span><span class="sxs-lookup"><span data-stu-id="265b9-495">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="265b9-496">Ce mode n’est pas recommandé, car le codec utilise une définition de luminance légèrement modifiée pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="265b9-496">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="265b9-497">Au lieu de cela, il est préférable de convertir l’image en monochrome avant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="265b9-497">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="265b9-498">4:2:2 et 4:2:0 conservent les détails de la luminance aux dépens des détails des couleurs.</span><span class="sxs-lookup"><span data-stu-id="265b9-498">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="265b9-499">Si vous définissez cette propriété, affectez également à [UseCodecOptions](#usecodecoptions) la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="265b9-499">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="265b9-500">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="265b9-500">UseCodecOptions</span></span>

<span data-ttu-id="265b9-501">Spécifie s’il faut utiliser les propriétés [Quality](#image-quality-settings), [chevauchement](#overlap)et [subéchantillonner](#subsampling) à la place de la propriété [ImageQuality](#imagequality) générique.</span><span class="sxs-lookup"><span data-stu-id="265b9-501">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="265b9-502">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-502">Data type</span></span>         | <span data-ttu-id="265b9-503">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-503">VARTYPE</span></span>      | <span data-ttu-id="265b9-504">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-504">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="265b9-505">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="265b9-505">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="265b9-506">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="265b9-506">**VT\_BOOL**</span></span> | <span data-ttu-id="265b9-507">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="265b9-507">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="265b9-508">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="265b9-508">VerticalTileSlices</span></span>

<span data-ttu-id="265b9-509">Définit le nombre de mosaïques horizontales.</span><span class="sxs-lookup"><span data-stu-id="265b9-509">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="265b9-510">Type de données</span><span class="sxs-lookup"><span data-stu-id="265b9-510">Data type</span></span>  | <span data-ttu-id="265b9-511">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="265b9-511">VARTYPE</span></span>     | <span data-ttu-id="265b9-512">Plage</span><span class="sxs-lookup"><span data-stu-id="265b9-512">Range</span></span>  | <span data-ttu-id="265b9-513">Default</span><span class="sxs-lookup"><span data-stu-id="265b9-513">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="265b9-514">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="265b9-514">**USHORT**</span></span> | <span data-ttu-id="265b9-515">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="265b9-515">**VT\_UI2**</span></span> | <span data-ttu-id="265b9-516">de 0 à 4 095</span><span class="sxs-lookup"><span data-stu-id="265b9-516">0–4095</span></span> | <span data-ttu-id="265b9-517">(hauteur d’image – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="265b9-517">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="265b9-518">La valeur est le nombre de sous-divisions verticales ; autrement dit, le nombre de vignettes verticales – 1.</span><span class="sxs-lookup"><span data-stu-id="265b9-518">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="265b9-519">Formats de couleurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="265b9-519">Supported Color Formats</span></span>

<span data-ttu-id="265b9-520">Pour plus d’informations sur ces formats, consultez [formats de pixel natifs](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="265b9-520">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="265b9-521">**Formats RGB d’entier**</span><span class="sxs-lookup"><span data-stu-id="265b9-521">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="265b9-522">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="265b9-522">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="265b9-523">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="265b9-523">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="265b9-524">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="265b9-524">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="265b9-525">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="265b9-525">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="265b9-526">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="265b9-526">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="265b9-527">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="265b9-527">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="265b9-528">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="265b9-528">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="265b9-529">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="265b9-529">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="265b9-530">**Formats RGB à virgule fixe**</span><span class="sxs-lookup"><span data-stu-id="265b9-530">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="265b9-531">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-531">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="265b9-532">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-532">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="265b9-533">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-533">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="265b9-534">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-534">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="265b9-535">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-535">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="265b9-536">**Formats RGB à virgule flottante**</span><span class="sxs-lookup"><span data-stu-id="265b9-536">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="265b9-537">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="265b9-537">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="265b9-538">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="265b9-538">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="265b9-539">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="265b9-539">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="265b9-540">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-540">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="265b9-541">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="265b9-541">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="265b9-542">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="265b9-542">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="265b9-543">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="265b9-543">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="265b9-544">**Formats de nuances de gris**</span><span class="sxs-lookup"><span data-stu-id="265b9-544">**Grayscale formats**</span></span>
    -   <span data-ttu-id="265b9-545">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="265b9-545">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="265b9-546">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="265b9-546">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="265b9-547">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-547">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="265b9-548">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="265b9-548">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="265b9-549">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="265b9-549">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="265b9-550">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="265b9-550">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="265b9-551">**Formats compactés**</span><span class="sxs-lookup"><span data-stu-id="265b9-551">**Packed formats**</span></span>
    -   <span data-ttu-id="265b9-552">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="265b9-552">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="265b9-553">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="265b9-553">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="265b9-554">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="265b9-554">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="265b9-555">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="265b9-555">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="265b9-556">**Formats CMJN**</span><span class="sxs-lookup"><span data-stu-id="265b9-556">**CMYK formats**</span></span>
    -   <span data-ttu-id="265b9-557">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-557">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="265b9-558">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="265b9-558">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="265b9-559">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-559">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="265b9-560">**Formats N-Channel**</span><span class="sxs-lookup"><span data-stu-id="265b9-560">**N-channel formats**</span></span>
    -   <span data-ttu-id="265b9-561">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-561">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="265b9-562">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-562">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="265b9-563">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-563">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="265b9-564">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-564">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="265b9-565">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-565">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="265b9-566">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-566">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-567">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-567">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-568">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-568">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-569">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-569">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-570">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-570">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-571">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-571">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-572">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-572">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="265b9-573">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-573">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="265b9-574">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-574">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="265b9-575">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-575">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="265b9-576">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="265b9-576">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="265b9-577">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-577">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-578">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-578">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-579">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-579">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-580">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-580">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-581">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-581">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="265b9-582">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="265b9-582">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
