---
description: Interfaces de capture vidéo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524088"
---
# <a name="video-capture-interfaces"></a><span data-ttu-id="e0bfc-103">Interfaces de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="e0bfc-103">Video Capture Interfaces</span></span>

<span data-ttu-id="e0bfc-104">Ces interfaces prennent en charge la capture vidéo, à l’aide d’appareils Microsoft® Windows® Driver Model (WDM) ou de Microsoft® Video pour les appareils Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="e0bfc-104">These interfaces support video capture, using Microsoft® Windows® Driver Model (WDM) devices or legacy Microsoft® Video for Windows® (VFW) devices.</span></span>



| <span data-ttu-id="e0bfc-105">Interface</span><span class="sxs-lookup"><span data-stu-id="e0bfc-105">Interface</span></span>                                                        | <span data-ttu-id="e0bfc-106">Description</span><span class="sxs-lookup"><span data-stu-id="e0bfc-106">Description</span></span>                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0bfc-107">**IAMAnalogVideoDecoder**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-107">**IAMAnalogVideoDecoder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | <span data-ttu-id="e0bfc-108">Contrôlez la numérisation vidéo sur une carte de capture vidéo WDM.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-108">Control video digitization on a WDM video capture card.</span></span>                                                      |
| [<span data-ttu-id="e0bfc-109">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-109">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | <span data-ttu-id="e0bfc-110">Contrôler la façon dont un code confidentiel alloue des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-110">Control how a pin allocates buffers.</span></span>                                                                         |
| [<span data-ttu-id="e0bfc-111">**IAMCopyCaptureFileProgress**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-111">**IAMCopyCaptureFileProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | <span data-ttu-id="e0bfc-112">Interface de rappel pour recevoir la progression d’une opération de copie de fichier.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-112">Callback interface to receive the progress of a file copy operation.</span></span>                                         |
| [<span data-ttu-id="e0bfc-113">**IAMCrossbar**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-113">**IAMCrossbar**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | <span data-ttu-id="e0bfc-114">Créez une connexion matérielle entre une source WDM Audio ou vidéo et un périphérique de capture WDM.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-114">Create a hardware connection between a WDM audio or video source and a WDM capture device.</span></span>                   |
| [<span data-ttu-id="e0bfc-115">**IAMDroppedFrames**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-115">**IAMDroppedFrames**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | <span data-ttu-id="e0bfc-116">Interrogez un filtre de capture sur les performances de capture.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-116">Query a capture filter about capture performance.</span></span>                                                            |
| [<span data-ttu-id="e0bfc-117">**IAMStreamControl**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-117">**IAMStreamControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | <span data-ttu-id="e0bfc-118">Contrôler les heures de démarrage et d’arrêt des flux individuels.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-118">Control the start and stop times of individual streams.</span></span>                                                      |
| [<span data-ttu-id="e0bfc-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | <span data-ttu-id="e0bfc-120">Interrogez et définissez le format de sortie du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-120">Query and set the capture filter's output format.</span></span>                                                            |
| [<span data-ttu-id="e0bfc-121">**IAMVfwCaptureDialogs**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-121">**IAMVfwCaptureDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | <span data-ttu-id="e0bfc-122">Affiche les boîtes de dialogue fournies par les pilotes de capture VFW.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-122">Display the dialog boxes provided by VFW capture drivers.</span></span>                                                    |
| [<span data-ttu-id="e0bfc-123">**IAMVideoControl**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-123">**IAMVideoControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | <span data-ttu-id="e0bfc-124">Contrôler l’image à partir d’un appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-124">Control the picture from a capture device.</span></span>                                                                   |
| [<span data-ttu-id="e0bfc-125">**IAMVideoProcAmp**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-125">**IAMVideoProcAmp**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | <span data-ttu-id="e0bfc-126">Ajustez les qualités d’un signal vidéo, telles que la luminosité, le contraste, la teinte, la saturation, la gamma et la netteté.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-126">Adjust the qualities of a video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.</span></span> |
| [<span data-ttu-id="e0bfc-127">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-127">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | <span data-ttu-id="e0bfc-128">Créer des graphiques de filtre pour la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-128">Build filter graphs for video capture.</span></span>                                                                       |
| [<span data-ttu-id="e0bfc-129">**IFileSinkFilter2**</span><span class="sxs-lookup"><span data-stu-id="e0bfc-129">**IFileSinkFilter2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | <span data-ttu-id="e0bfc-130">Spécifiez le nom et les attributs d’un fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-130">Specify the name and attributes of an output file.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="e0bfc-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0bfc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0bfc-132">Interfaces de contrôle de périphérique externe</span><span class="sxs-lookup"><span data-stu-id="e0bfc-132">External Device Control Interfaces</span></span>](external-device-control-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e0bfc-133">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="e0bfc-133">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



