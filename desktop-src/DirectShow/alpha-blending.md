---
description: Fusion alpha
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Fusion alpha (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109639"
---
# <a name="alpha-blending-directshow"></a><span data-ttu-id="a6d87-103">Fusion alpha (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="a6d87-103">Alpha Blending (DirectShow)</span></span>

<span data-ttu-id="a6d87-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="a6d87-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a6d87-105">Cet article décrit la fusion alpha dans les [services d’édition DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="a6d87-105">This article describes alpha blending in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="a6d87-106">Alpha mesure la transparence d’un pixel ou d’une image.</span><span class="sxs-lookup"><span data-stu-id="a6d87-106">Alpha measures the transparency of a pixel or image.</span></span> <span data-ttu-id="a6d87-107">Dans la vidéo RVB non compressée 32 bits, quatre composants définissent chaque pixel : un canal alpha (A) et trois composants de couleur (RVB).</span><span class="sxs-lookup"><span data-stu-id="a6d87-107">In 32-bit uncompressed RGB video, four components define each pixel: an alpha channel (A) and three color components (RGB).</span></span> <span data-ttu-id="a6d87-108">Un pixel dont la valeur alpha est égale à zéro est totalement transparent.</span><span class="sxs-lookup"><span data-stu-id="a6d87-108">A pixel with an alpha value of zero is completely transparent.</span></span> <span data-ttu-id="a6d87-109">Un pixel avec une valeur alpha de 255 est opaque.</span><span class="sxs-lookup"><span data-stu-id="a6d87-109">A pixel with an alpha value of 255 is opaque.</span></span> <span data-ttu-id="a6d87-110">Entre ces valeurs, le pixel a différents degrés de transparence.</span><span class="sxs-lookup"><span data-stu-id="a6d87-110">Between these values, the pixel has various degrees of transparency.</span></span>

<span data-ttu-id="a6d87-111">DirectShow définit deux types de médias pour la vidéo RGB 32 bits :</span><span class="sxs-lookup"><span data-stu-id="a6d87-111">DirectShow defines two media types for 32-bit RGB video:</span></span>

-   <span data-ttu-id="a6d87-112">**MEDIASUBTYPE \_ ARGB32**: la vidéo est 32 bits RGB avec un canal alpha valide.</span><span class="sxs-lookup"><span data-stu-id="a6d87-112">**MEDIASUBTYPE\_ARGB32**: The video is 32-bit RGB with a valid alpha channel.</span></span>
-   <span data-ttu-id="a6d87-113">**MEDIASUBTYPE \_ RGB32**: les pixels sont 32 bits, mais le canal alpha n’est pas nécessairement valide.</span><span class="sxs-lookup"><span data-stu-id="a6d87-113">**MEDIASUBTYPE\_RGB32**: Pixels are 32 bits, but the alpha channel is not necessarily valid.</span></span>

<span data-ttu-id="a6d87-114">Pour effectuer une fusion alpha dans DES, définissez le type de média non compressé du groupe vidéo sur MEDIASUBTYPE \_ ARGB32.</span><span class="sxs-lookup"><span data-stu-id="a6d87-114">To perform alpha blending in DES, set the video group's uncompressed media type to MEDIASUBTYPE\_ARGB32.</span></span> <span data-ttu-id="a6d87-115">En C++, appelez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d87-115">In C++, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span> <span data-ttu-id="a6d87-116">Dans le format XTL, l’affectation de la valeur 32 à l’attribut [**bitdepth**](bitdepth-attribute.md) de l’élément [**Group**](group-element.md) est également possible.</span><span class="sxs-lookup"><span data-stu-id="a6d87-116">In the XTL format, setting the [**bitdepth**](bitdepth-attribute.md) attribute of the [**group**](group-element.md) element to 32 accomplishes this as well.</span></span>

<span data-ttu-id="a6d87-117">Ensuite, vous avez besoin de données vidéo qui contiennent un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-117">Next, you need video data that contains an alpha channel.</span></span> <span data-ttu-id="a6d87-118">Il existe plusieurs options :</span><span class="sxs-lookup"><span data-stu-id="a6d87-118">There are several options:</span></span>

-   <span data-ttu-id="a6d87-119">Vous pouvez utiliser un fichier AVI qui possède déjà une vidéo RGB 32 bits avec des données alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-119">You can use an AVI file that already has 32-bit RGB video with alpha data.</span></span> <span data-ttu-id="a6d87-120">Actuellement, alpha n’est pas pris en charge pour les fichiers sources MPEG ou WMF (Microsoft Windows Media Format).</span><span class="sxs-lookup"><span data-stu-id="a6d87-120">Currently, alpha is not supported for MPEG or Microsoft Windows Media Format (WMF) source files.</span></span>
-   <span data-ttu-id="a6d87-121">DES prend en charge les fichiers bitmap 32 bits (. bmp) et Targa (. TGA) avec des données alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-121">DES supports 32-bit bitmap (.bmp) and Targa (.tga) files with alpha data.</span></span>
-   <span data-ttu-id="a6d87-122">Vous pouvez écrire un filtre source personnalisé qui crée des données RGB 32 bits avec alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-122">You can write a custom source filter that creates 32-bit RGB data with alpha.</span></span> <span data-ttu-id="a6d87-123">Le type de média de sortie doit être **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="a6d87-123">The output media type must be **MEDIASUBTYPE\_ARGB32**.</span></span> <span data-ttu-id="a6d87-124">Utilisez le filtre en tant que sous-objet dans un objet source de chronologie.</span><span class="sxs-lookup"><span data-stu-id="a6d87-124">Use the filter as the subobject in a timeline source object.</span></span>

<span data-ttu-id="a6d87-125">Si votre source vidéo n’a pas d’alpha, vous pouvez utiliser un effet qui crée des données alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-125">If your video source does not have alpha, you can use an effect that creates alpha data.</span></span> <span data-ttu-id="a6d87-126">L' [effet d’accesseur Set alpha](alpha-setter-effect.md) définit le canal alpha pour l’intégralité de l’image sur une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="a6d87-126">The [Alpha Setter Effect](alpha-setter-effect.md) sets the alpha channel for the entire image to a constant value.</span></span> <span data-ttu-id="a6d87-127">Pour faire varier l’alpha dans le temps, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) avec l’effet d’accesseur Set alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-127">To vary the alpha over time, use the [**IPropertySetter**](ipropertysetter.md) interface with the Alpha Setter Effect.</span></span> <span data-ttu-id="a6d87-128">La source d’origine ne doit pas nécessairement être de 32 bits, à condition que le type de support non compressé du groupe soit **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="a6d87-128">The original source does not have to be 32 bits, as long as the group's uncompressed media type is **MEDIASUBTYPE\_ARGB32**.</span></span>

<span data-ttu-id="a6d87-129">Enfin, passez la vidéo à un effet ou à une transition qui effectue une fusion alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-129">Finally, pass the video to an effect or transition that performs alpha blending.</span></span> <span data-ttu-id="a6d87-130">La [transition du compositeur](compositor-transition.md) effectue une fusion alpha et la [transition de clé](key-transition.md) peut être associée à la valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="a6d87-130">The [Compositor Transition](compositor-transition.md) performs alpha blending, and the [Key Transition](key-transition.md) can key by alpha value.</span></span>

<span data-ttu-id="a6d87-131">L’exemple de projet XTL suivant effectue une fusion alpha :</span><span class="sxs-lookup"><span data-stu-id="a6d87-131">The following sample XTL project performs alpha blending:</span></span>


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a><span data-ttu-id="a6d87-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6d87-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d87-133">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="a6d87-133">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



