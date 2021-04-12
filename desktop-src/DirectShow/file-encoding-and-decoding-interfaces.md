---
description: Interfaces d’encodage et de décodage de fichier
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfaces d’encodage et de décodage de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109898"
---
# <a name="file-encoding-and-decoding-interfaces"></a><span data-ttu-id="b7b37-103">Interfaces d’encodage et de décodage de fichier</span><span class="sxs-lookup"><span data-stu-id="b7b37-103">File Encoding and Decoding Interfaces</span></span>

<span data-ttu-id="b7b37-104">Ces interfaces prennent en charge l’encodage et le décodage de fichier.</span><span class="sxs-lookup"><span data-stu-id="b7b37-104">These interfaces support file encoding and decoding.</span></span>



| <span data-ttu-id="b7b37-105">Interface</span><span class="sxs-lookup"><span data-stu-id="b7b37-105">Interface</span></span>                                                    | <span data-ttu-id="b7b37-106">Description</span><span class="sxs-lookup"><span data-stu-id="b7b37-106">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7b37-107">**IAMMediaContent**</span><span class="sxs-lookup"><span data-stu-id="b7b37-107">**IAMMediaContent**</span></span>](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | <span data-ttu-id="b7b37-108">Récupérez les métadonnées d’un flux de données, telles que l’auteur et le titre.</span><span class="sxs-lookup"><span data-stu-id="b7b37-108">Retrieve meta-data from a stream, such as the author and title.</span></span>                                              |
| [<span data-ttu-id="b7b37-109">**IAMOpenProgress**</span><span class="sxs-lookup"><span data-stu-id="b7b37-109">**IAMOpenProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | <span data-ttu-id="b7b37-110">Déterminer la progression d’une opération d’ouverture de fichier.</span><span class="sxs-lookup"><span data-stu-id="b7b37-110">Determine the progress of a file-open operation.</span></span>                                                             |
| [<span data-ttu-id="b7b37-111">**IAMParse**</span><span class="sxs-lookup"><span data-stu-id="b7b37-111">**IAMParse**</span></span>](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | <span data-ttu-id="b7b37-112">Interroge et définit l’heure d’analyse de la position actuelle dans un flux MPEG.</span><span class="sxs-lookup"><span data-stu-id="b7b37-112">Query and set the parse time for the current position in an MPEG stream.</span></span>                                     |
| [<span data-ttu-id="b7b37-113">**IAMStreamSelect**</span><span class="sxs-lookup"><span data-stu-id="b7b37-113">**IAMStreamSelect**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | <span data-ttu-id="b7b37-114">Contrôlez les flux logiques lus et récupérez les informations les concernant.</span><span class="sxs-lookup"><span data-stu-id="b7b37-114">Control which logical streams are played, and retrieve information about them.</span></span>                               |
| [<span data-ttu-id="b7b37-115">**IAMVfwCompressDialogs**</span><span class="sxs-lookup"><span data-stu-id="b7b37-115">**IAMVfwCompressDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | <span data-ttu-id="b7b37-116">Affiche les boîtes de dialogue fournies par les codecs VFW.</span><span class="sxs-lookup"><span data-stu-id="b7b37-116">Display dialog boxes provided by VFW codecs.</span></span>                                                                 |
| [<span data-ttu-id="b7b37-117">**IAMVideoCompression**</span><span class="sxs-lookup"><span data-stu-id="b7b37-117">**IAMVideoCompression**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | <span data-ttu-id="b7b37-118">Définissez les paramètres de compression vidéo.</span><span class="sxs-lookup"><span data-stu-id="b7b37-118">Set video compression parameters.</span></span>                                                                            |
| [<span data-ttu-id="b7b37-119">**IConfigAsfWriter**</span><span class="sxs-lookup"><span data-stu-id="b7b37-119">**IConfigAsfWriter**</span></span>](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | <span data-ttu-id="b7b37-120">Contrôler la façon dont le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) écrit des fichiers ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="b7b37-120">Control how the [WM ASF Writer](wm-asf-writer-filter.md) filter writes Advanced Systems Format (ASF) files.</span></span> |
| [<span data-ttu-id="b7b37-121">**IConfigAviMux**</span><span class="sxs-lookup"><span data-stu-id="b7b37-121">**IConfigAviMux**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | <span data-ttu-id="b7b37-122">Contrôler la façon dont le filtre de [multiplexeur](avi-mux-filter.md) de fichier AVI écrit des fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="b7b37-122">Control how the [AVI Mux](avi-mux-filter.md) filter writes AVI files.</span></span>                                       |
| [<span data-ttu-id="b7b37-123">**IConfigInterleaving**</span><span class="sxs-lookup"><span data-stu-id="b7b37-123">**IConfigInterleaving**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | <span data-ttu-id="b7b37-124">Configurez l’entrelacement lorsque le filtre multiplex MUX écrit des fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="b7b37-124">Configure interleaving when the AVI Mux filter writes AVI files.</span></span>                                             |
| [<span data-ttu-id="b7b37-125">**IDVEnc**</span><span class="sxs-lookup"><span data-stu-id="b7b37-125">**IDVEnc**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | <span data-ttu-id="b7b37-126">Définissez la résolution d’encodage sur le filtre d' [encodeur vidéo DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b37-126">Set the encoding resolution on the [DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="b7b37-127">**IDVSplitter**</span><span class="sxs-lookup"><span data-stu-id="b7b37-127">**IDVSplitter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | <span data-ttu-id="b7b37-128">Rétrograder la fréquence d’images sur un flux vidéo numérique (DV)</span><span class="sxs-lookup"><span data-stu-id="b7b37-128">Downgrade the frame rate on a digital video (DV) stream</span></span>                                                      |
| [<span data-ttu-id="b7b37-129">**IIPDVDec**</span><span class="sxs-lookup"><span data-stu-id="b7b37-129">**IIPDVDec**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | <span data-ttu-id="b7b37-130">Définissez la résolution du décodage sur le filtre de décodage [vidéo DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b37-130">Set the decoding resolution on the [DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="b7b37-131">**IPersistMediaPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="b7b37-131">**IPersistMediaPropertyBag**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | <span data-ttu-id="b7b37-132">Définissez et récupérez des blocs d’informations et d’extraction dans des flux AVI.</span><span class="sxs-lookup"><span data-stu-id="b7b37-132">Set and retrieve INFO and DISP chunks in AVI streams.</span></span>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="b7b37-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7b37-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7b37-134">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b7b37-134">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



