---
description: Affichage des sous-titres
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Affichage des sous-titres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561709"
---
# <a name="viewing-closed-captions"></a><span data-ttu-id="1ca6f-103">Affichage des sous-titres</span><span class="sxs-lookup"><span data-stu-id="1ca6f-103">Viewing Closed Captions</span></span>

<span data-ttu-id="1ca6f-104">Pour prendre en charge les sous-titres dans la télévision analogique, le filtre de capture expose un code confidentiel qui remet les données de sous-titres VBI ou Closed.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-104">To support closed captions in analog television, the capture filter exposes a pin that delivers either VBI or closed caption data.</span></span> <span data-ttu-id="1ca6f-105">Le code PIN aura l’une des catégories de code confidentiel suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ca6f-105">The pin will have one of the following pin categories:</span></span>

-   <span data-ttu-id="1ca6f-106">Code confidentiel VBI ( \_ catégorie de pin \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-106">VBI pin (PIN\_CATEGORY\_VBI).</span></span> <span data-ttu-id="1ca6f-107">Fournit un flux d’exemples de forme d’onde VBI.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-107">Delivers a stream of VBI waveform samples.</span></span> <span data-ttu-id="1ca6f-108">Ils sont passés à un filtre de décodeur qui extrait les données de sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-108">These are passed to a decoder filter that extracts the closed captioning data.</span></span>
-   <span data-ttu-id="1ca6f-109">Code PIN CC (code confidentiel de \_ catégorie \_ cc).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-109">CC pin (PIN\_CATEGORY\_CC).</span></span> <span data-ttu-id="1ca6f-110">Fournit des paires d’octets à légende fermée, extraites des données de la ligne-21.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-110">Delivers closed-caption byte pairs, extracted from the line-21 data.</span></span>
-   <span data-ttu-id="1ca6f-111">Découpage matériel code confidentiel CC (PINNAME \_ vidéo \_ cc \_ capture).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-111">Hardware slicing CC pin (PINNAME\_VIDEO\_CC\_CAPTURE).</span></span>

<span data-ttu-id="1ca6f-112">Pour afficher un aperçu des sous-titres, appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) avec la catégorie de code confidentiel VBI et, si cela échoue, rappelez-le avec la catégorie CC.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-112">To preview closed captions, call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the VBI pin category, and if that fails, call it again with the CC category.</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



<span data-ttu-id="1ca6f-113">Le diagramme suivant montre un graphique de filtre classique pour l’affichage des sous-titres.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-113">The following diagram shows a typical filter graph for displaying closed captions.</span></span>

![graphique de prévisualisation du sous-titrage](images/vidcap08.png)

<span data-ttu-id="1ca6f-115">Ce graphique utilise les filtres suivants pour l’affichage des sous-titres :</span><span class="sxs-lookup"><span data-stu-id="1ca6f-115">This graph uses the following filters for closed caption display:</span></span>

-   <span data-ttu-id="1ca6f-116">[Convertisseur de tee/récepteur à récepteur](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-116">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="1ca6f-117">Accepte les informations VBI du filtre de capture et les divise en flux distincts pour chaque service de données présent sur le signal.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-117">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span> <span data-ttu-id="1ca6f-118">Microsoft fournit des codecs VBI pour les sous-titres, les NABTS et le Teletext standard (WST).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-118">Microsoft provides VBI codecs for Closed Caption, NABTS, and World Standard Teletext (WST).</span></span>
-   <span data-ttu-id="1ca6f-119">[Décodeur CC](cc-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-119">[CC Decoder](cc-decoder-filter.md).</span></span> <span data-ttu-id="1ca6f-120">Décode les données CC à partir des formes d’onde VBI échantillonnées fournies par le filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-120">Decodes CC data from the sampled VBI waveforms provided by the capture filter.</span></span>
-   <span data-ttu-id="1ca6f-121">[Décodeur de ligne 21](line-21-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-121">[Line 21 Decoder](line-21-decoder-filter.md).</span></span> <span data-ttu-id="1ca6f-122">Traduit les paires d’octets CC et dessine le texte de légende sur les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-122">Translates the CC byte pairs and draws the caption text onto bitmaps.</span></span> <span data-ttu-id="1ca6f-123">Le filtre en aval (dans ce cas, le mélangeur de superposition) recouvre les bitmaps dans la vidéo.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-123">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="1ca6f-124">La méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) du générateur de graphiques de capture ajoute automatiquement ces filtres.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-124">The Capture Graph Builder's [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds these filters automatically.</span></span> <span data-ttu-id="1ca6f-125">Si le filtre de capture a un pin CC au lieu d’un code confidentiel VBI, le code PIN CC est directement connecté au filtre de décodeur de ligne 21.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-125">If the capture filter has a CC pin instead of a VBI pin, the CC pin is connected directly to the Line 21 Decoder filter.</span></span>

> [!Note]  
> <span data-ttu-id="1ca6f-126">Si vous utilisez le filtre de convertisseur de mixage vidéo (VMR) pour le rendu, utilisez le filtre de décodeur de ligne 21 2.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-126">If you are using the Video Mixing Renderer (VMR) filter for rendering, use the Line 21 Decoder Filter 2.</span></span> <span data-ttu-id="1ca6f-127">Ce filtre a les mêmes fonctionnalités que le décodeur de ligne 21, mais le CLSID est CLSID \_ Line21Decoder2.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-127">This filter has the same functionality as the Line 21 Decoder, but the CLSID is CLSID\_Line21Decoder2.</span></span>

 

> [!Note]  
> <span data-ttu-id="1ca6f-128">Le filtre de décodage CC a été supprimé de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-128">The CC Decoder filter was removed in Windows Vista.</span></span> <span data-ttu-id="1ca6f-129">Les nouvelles applications doivent utiliser le filtre VBICodec, qui est documenté dans la documentation Microsoft TV technologies.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-129">New applications should use the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

 

<span data-ttu-id="1ca6f-130">Si le périphérique de capture utilise un port vidéo, le filtre de capture peut avoir une broche de port vidéo VBI (catégorie de broche \_ \_ VIDEOPORT \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-130">If the capture device uses a video port, the capture filter might have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="1ca6f-131">Ce code confidentiel doit être connecté au filtre [allocateur de surface VBI](vbi-surface-allocator.md) , qui alloue des surfaces pour contenir les données VBI capturées.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-131">This pin must be connected to the [VBI Surface Allocator](vbi-surface-allocator.md) filter, which allocates surfaces to hold the captured VBI data.</span></span> <span data-ttu-id="1ca6f-132">La méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ajoute ce filtre si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-132">The [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds this filter if it is required.</span></span> <span data-ttu-id="1ca6f-133">Le diagramme suivant montre un graphique de filtre avec l’allocateur de surface VBI.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-133">The following diagram shows a filter graph with the VBI Surface Allocator.</span></span>

![graphique de prévisualisation de sous-titrage avec un allocateur de surface VBI](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a><span data-ttu-id="1ca6f-135">Activation et désactivation des légendes</span><span class="sxs-lookup"><span data-stu-id="1ca6f-135">Enabling and Disabling the Captions</span></span>

<span data-ttu-id="1ca6f-136">Pour contrôler l’affichage des sous-titres, utilisez l’interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) sur le filtre de décodeur de la ligne 21.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-136">To control the captioning display, use the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface on the Line 21 Decoder filter.</span></span> <span data-ttu-id="1ca6f-137">Par exemple, vous pouvez désactiver l’affichage des sous-titres à l’aide de la méthode [**IAMLine21Decoder :: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , comme suit :</span><span class="sxs-lookup"><span data-stu-id="1ca6f-137">For example, you can turn off the captioning display using the [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) method, as follows:</span></span>


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



<span data-ttu-id="1ca6f-138">Cet exemple utilise la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour localiser l’interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) .</span><span class="sxs-lookup"><span data-stu-id="1ca6f-138">This example uses the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface.</span></span> <span data-ttu-id="1ca6f-139">Le premier paramètre de **FindInterface** est **&Rechercher en \_ aval \_ uniquement**, qui spécifie de rechercher en aval à partir du filtre de capture (*pCap*).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-139">The first parameter to **FindInterface** is **&LOOK\_DOWNSTREAM\_ONLY**, which specifies to search downstream from the capture filter (*pCap*).</span></span>

### <a name="capturing-closed-caption-bitmaps"></a><span data-ttu-id="1ca6f-140">Capturer des bitmaps de sous-titres</span><span class="sxs-lookup"><span data-stu-id="1ca6f-140">Capturing Closed Caption Bitmaps</span></span>

<span data-ttu-id="1ca6f-141">Vous pouvez capturer les bitmaps de légende dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-141">You can capture the caption bitmaps into a file.</span></span> <span data-ttu-id="1ca6f-142">Pour ce faire, ajoutez la section d’écriture de fichiers du graphique de filtre, comme décrit dans [capture de la vidéo dans un fichier](capturing-video-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="1ca6f-142">To do so, add the file-writing section of the filter graph, as described in [Capturing Video to a File](capturing-video-to-a-file.md).</span></span> <span data-ttu-id="1ca6f-143">Ensuite, affichez le code confidentiel CC ou VBI dans le filtre Mux :</span><span class="sxs-lookup"><span data-stu-id="1ca6f-143">Then render the CC or VBI pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



<span data-ttu-id="1ca6f-144">Si vous capturez également la vidéo, cette opération crée un fichier avec deux flux vidéo distincts.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-144">If you are also capturing the video, this will create a file with two separate video streams.</span></span> <span data-ttu-id="1ca6f-145">Il ne capture pas de vidéo avec des sous-titres superposés au-dessus de l’image.</span><span class="sxs-lookup"><span data-stu-id="1ca6f-145">It will not capture video with captions overlaid on top of the picture.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ca6f-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ca6f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ca6f-147">Sous-titres et télétexte</span><span class="sxs-lookup"><span data-stu-id="1ca6f-147">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



