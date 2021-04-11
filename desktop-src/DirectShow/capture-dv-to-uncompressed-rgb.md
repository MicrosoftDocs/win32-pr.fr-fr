---
description: Capturer le DV avec la couleur RVB non compressée
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Capturer le DV avec la couleur RVB non compressée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108598"
---
# <a name="capture-dv-to-uncompressed-rgb"></a><span data-ttu-id="f74bb-103">Capturer le DV avec la couleur RVB non compressée</span><span class="sxs-lookup"><span data-stu-id="f74bb-103">Capture DV to Uncompressed RGB</span></span>

<span data-ttu-id="f74bb-104">Cet exemple montre comment capturer du DV à partir du caméscope et l’enregistrer dans un fichier au format RVB non compressé lors de l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="f74bb-104">This example shows how to capture DV from the camcorder and save it to a file as uncompressed RGB while previewing.</span></span> <span data-ttu-id="f74bb-105">Utilisez le graphique de filtre illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="f74bb-105">Use the filter graph shown in the following diagram.</span></span>

![capture de RGB non compressé dans un fichier](images/dv-rgb-cap.png)

<span data-ttu-id="f74bb-107">Le filtre de séparateur DV divise le fichier audio/vidéo entrelacé en flux vidéo et audio distincts. la vidéo encodée en DV passe au filtre de [décodeur vidéo DV](dv-video-decoder-filter.md) , qui génère une vidéo RVB non compressée.</span><span class="sxs-lookup"><span data-stu-id="f74bb-107">The DV Splitter filter splits the interleaved audio/video into separate video and audio streams The DV-encoded video goes to the [DV Video Decoder](dv-video-decoder-filter.md) filter, which outputs uncompressed RGB video.</span></span> <span data-ttu-id="f74bb-108">La vidéo RVB est routée via le filtre tee intelligent vers le filtre multiplex Mux (pour la capture) et le convertisseur vidéo (pour la version préliminaire).</span><span class="sxs-lookup"><span data-stu-id="f74bb-108">The RGB video is routed through the Smart Tee filter to the AVI Mux filter (for capture) and the video renderer (for preview).</span></span> <span data-ttu-id="f74bb-109">Pendant ce temps, le flux audio du séparateur DV passe par le filtre tee de code confidentiel infini à AVI MUX et au convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="f74bb-109">Meanwhile, the audio stream from the DV Splitter goes through the Infinite Pin Tee filter to the AVI Mux and the audio renderer.</span></span> <span data-ttu-id="f74bb-110">Le gestionnaire de graphes de filtre conserve tous ces flux synchronisés, en utilisant les horodatages sur les échantillons et l’horloge de référence du graphique.</span><span class="sxs-lookup"><span data-stu-id="f74bb-110">The Filter Graph Manager keeps all of these streams synchronized, using the time stamps on the samples and the graph reference clock.</span></span>

<span data-ttu-id="f74bb-111">Ce graphique peut paraître inutilement compliqué, mais il garantit que le flux vidéo encodé au format DV est décodé une seule fois, ce qui réduit les besoins en processeur.</span><span class="sxs-lookup"><span data-stu-id="f74bb-111">This graph might seem unnecessarily complicated, but it ensures that the DV-encoded video stream is decoded only once, which minimizes the CPU requirements.</span></span> <span data-ttu-id="f74bb-112">Notez également que la vidéo passe par le filtre tee intelligent pendant que l’audio passe par le filtre tee du pin infini.</span><span class="sxs-lookup"><span data-stu-id="f74bb-112">Also, note that the video goes through the Smart Tee filter while the audio goes through the Infinite Pin Tee filter.</span></span> <span data-ttu-id="f74bb-113">Le tee intelligent peut supprimer des images d’aperçu pour améliorer les performances de capture, ce qui est souhaitable pour la vidéo, mais pas pour l’audio, où les échantillons supprimés sont très perceptibles.</span><span class="sxs-lookup"><span data-stu-id="f74bb-113">The Smart Tee can drop preview frames to improve capture performance, which is desirable for video but not for audio, where dropped samples are highly noticeable.</span></span> <span data-ttu-id="f74bb-114">En outre, étant donné que l’audio nécessite beaucoup plus de bande passante que la vidéo, il y a relativement peu de chance de déposer de l’audio dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="f74bb-114">Also, because the audio requires much lower bandwidth than the video, there is relatively little chance of dropping audio in the file.</span></span>

<span data-ttu-id="f74bb-115">Vous devez générer ce graphique une section à la fois, mais la méthode RenderStream peut encore vous aider.</span><span class="sxs-lookup"><span data-stu-id="f74bb-115">You must build this graph one section at a time, but the RenderStream method can still help.</span></span> <span data-ttu-id="f74bb-116">Utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f74bb-116">Use the following code:</span></span>


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



<span data-ttu-id="f74bb-117">Vous devez créer le séparateur DV, le décodeur vidéo DV, le tee intelligent et les filtres tee de pin infinis, et les ajouter au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="f74bb-117">You must create the DV Splitter, DV Video Decoder, Smart Tee, and Infinite Pin Tee filters, and add each one to the filter graph.</span></span> <span data-ttu-id="f74bb-118">(Par souci de concision, ces étapes sont omises du code précédent.) Cet exemple utilise la méthode [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) pour rechercher les codes confidentiels de capture et de prévisualisation sur le filtre tee intelligent. la capture est toujours en sortie broche 0 et la version préliminaire est la broche 1 de sortie.</span><span class="sxs-lookup"><span data-stu-id="f74bb-118">(For brevity, these steps are omitted from the previous code.) This example uses the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to find the capture and preview pins on the Smart Tee filter; capture is always output pin 0, and preview is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f74bb-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f74bb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f74bb-120">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="f74bb-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



