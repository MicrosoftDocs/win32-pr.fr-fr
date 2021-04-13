---
description: À propos de la vidéo numérique dans DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: À propos de la vidéo numérique dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104561284"
---
# <a name="about-digital-video-in-directshow"></a><span data-ttu-id="5ed0d-103">À propos de la vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="5ed0d-103">About Digital Video in DirectShow</span></span>

<span data-ttu-id="5ed0d-104">La vidéo numérique (DV) peut être capturée à partir d’une caméra DV, stockée dans un fichier sur l’ordinateur de l’utilisateur, ou stockée sur bande à l’aide d’un magnétoscope vidéo.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-104">Digital video (DV) can be captured from a DV camera, stored in a file on the user's computer, or stored on tape using a video tape recorder (VTR).</span></span> <span data-ttu-id="5ed0d-105">Par conséquent, les opérations qu’une application peut effectuer sur un flux DV sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5ed0d-105">Thus, the operations that an application might perform on a DV stream include:</span></span>

-   <span data-ttu-id="5ed0d-106">Capturez des vidéos en direct à partir d’une caméra DV.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-106">Capture live video from a DV camera.</span></span>
-   <span data-ttu-id="5ed0d-107">Transmettez les données DV de VTR tape sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-107">Transmit DV data from VTR tape to the computer.</span></span>
-   <span data-ttu-id="5ed0d-108">Transmettez les données DV de l’ordinateur au magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-108">Transmit DV data from the computer to the VTR.</span></span>
-   <span data-ttu-id="5ed0d-109">Lire des données DV à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-109">Read DV data from a file.</span></span>
-   <span data-ttu-id="5ed0d-110">Écrire des données DV dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-110">Write DV data to a file.</span></span>
-   <span data-ttu-id="5ed0d-111">Affichez l’audio et la vidéo dans un flux DV.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-111">Render the audio and video in a DV stream.</span></span>

<span data-ttu-id="5ed0d-112">DirectShow fournit les filtres DV suivants :</span><span class="sxs-lookup"><span data-stu-id="5ed0d-112">DirectShow provides the following DV filters:</span></span>

-   <span data-ttu-id="5ed0d-113">[Pilote MSDV](msdv-driver.md).</span><span class="sxs-lookup"><span data-stu-id="5ed0d-113">[MSDV Driver](msdv-driver.md).</span></span> <span data-ttu-id="5ed0d-114">Le pilote MSDV contrôle un périphérique DV, tel qu’un caméscope.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-114">The MSDV driver controls a DV device, such as a camcorder.</span></span> <span data-ttu-id="5ed0d-115">L’appareil peut avoir une sous-unité de caméra et une sous-unité VTR. MSDV contrôle les deux sous-unités.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-115">The device may have a camera subunit and a VTR subunit; MSDV controls both subunits.</span></span> <span data-ttu-id="5ed0d-116">Le pilote MSDV apparaît pour les applications sous la forme d’un filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-116">The MSDV driver appears to applications as a DirectShow filter.</span></span>
-   <span data-ttu-id="5ed0d-117">Filtre de [séparateur DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-117">[DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="5ed0d-118">Les images DV contiennent des données audio et vidéo dans le même cadre.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-118">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="5ed0d-119">Le filtre de séparateur DV extrait les données audio et les renvoie sous la forme d’un ou de deux flux audio.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-119">The DV Splitter filter extracts the audio data and outputs it as one or two audio streams.</span></span> <span data-ttu-id="5ed0d-120">Il génère les données d’origine sous la forme d’un flux vidéo DV distinct.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-120">It outputs the original data as a separate DV video stream.</span></span>
-   <span data-ttu-id="5ed0d-121">Filtre de [décodage vidéo DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-121">[DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span> <span data-ttu-id="5ed0d-122">Décode la vidéo DV en vidéo non compressée.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-122">Decodes DV video into uncompressed video.</span></span>
-   <span data-ttu-id="5ed0d-123">Filtre d' [encodeur vidéo DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-123">[DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span> <span data-ttu-id="5ed0d-124">Encode la vidéo non compressée en vidéo encodée en DV.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-124">Encodes uncompressed video to DV-encoded video.</span></span>
-   <span data-ttu-id="5ed0d-125">[Du multiplexeur DV](dv-muxer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="5ed0d-125">[DV Muxer](dv-muxer-filter.md).</span></span> <span data-ttu-id="5ed0d-126">Combine un flux vidéo DV avec un ou deux flux audio pour créer un flux DV entrelacé unique.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-126">Combines a DV video stream with one or two audio streams, to create a single interleaved DV stream.</span></span>

<span data-ttu-id="5ed0d-127">Le séparateur DV et le décodeur vidéo DV fonctionnent ensemble.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-127">The DV Splitter and DV Video Decoder work together.</span></span> <span data-ttu-id="5ed0d-128">Le séparateur prend le flux entrelacé et génère des flux de données audio et vidéo DV distincts.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-128">The splitter takes the interleaved stream and outputs separate audio and DV video streams.</span></span> <span data-ttu-id="5ed0d-129">Le décodeur convertit la vidéo DV en vidéo non compressée.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-129">The decoder converts the DV video to uncompressed video.</span></span> <span data-ttu-id="5ed0d-130">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-130">The following image illustrates this process.</span></span>

![séparateur DV et décodeur DV](images/dv-filters1.png)

<span data-ttu-id="5ed0d-132">L’encodeur vidéo DV et le DV du multiplexeur inversent le processus : l’encodeur convertit la vidéo non compressée en vidéo DV et le multiplexeur combine une vidéo audio et DV pour créer un flux entrelacé unique, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-132">The DV Video Encoder and the DV Muxer reverse the process: The encoder converts uncompressed video to DV video, and the mux combines audio and DV video to create a single interleaved stream, as shown in the following diagram.</span></span>

![encodeur DV et DV du multiplexeur](images/dv-filters2.png)

## <a name="related-topics"></a><span data-ttu-id="5ed0d-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ed0d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed0d-135">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="5ed0d-135">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



