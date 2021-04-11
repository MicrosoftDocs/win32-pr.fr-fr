---
description: Capturer le fichier DV dans un fichier
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturer le fichier DV dans un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317742"
---
# <a name="capture-dv-to-file"></a><span data-ttu-id="5d881-103">Capturer le fichier DV dans un fichier</span><span class="sxs-lookup"><span data-stu-id="5d881-103">Capture DV to File</span></span>

<span data-ttu-id="5d881-104">Cette section décrit comment capturer une vidéo numérique (DV) à partir d’une caméra DV ou d’une bande VTR.</span><span class="sxs-lookup"><span data-stu-id="5d881-104">This section describes how to capture digital video (DV) from a DV camera or from a VTR tape.</span></span>

1.  <span data-ttu-id="5d881-105">Créez une instance du filtre de [pilote MSDV](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="5d881-105">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="5d881-106">Pour plus d’informations, consultez [sélection d’un périphérique de capture](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="5d881-106">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="5d881-107">Initialisez le générateur de graphiques de capture, comme décrit dans [à propos du générateur de graphiques de capture](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="5d881-107">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
3.  <span data-ttu-id="5d881-108">Générez le graphique de capture, en fonction du type de fichier cible :</span><span class="sxs-lookup"><span data-stu-id="5d881-108">Build the capture graph, depending on the target file type:</span></span>
    -   [<span data-ttu-id="5d881-109">Capturer un fichier DV de type 1</span><span class="sxs-lookup"><span data-stu-id="5d881-109">Capture a Type-1 DV File</span></span>](capture-a-type-1-dv-file.md)
    -   [<span data-ttu-id="5d881-110">Capturer un fichier DV de type 2</span><span class="sxs-lookup"><span data-stu-id="5d881-110">Capture a Type-2 DV File</span></span>](capture-a-type-2-dv-file.md)
    -   [<span data-ttu-id="5d881-111">Capturer le DV avec la couleur RVB non compressée</span><span class="sxs-lookup"><span data-stu-id="5d881-111">Capture DV to Uncompressed RGB</span></span>](capture-dv-to-uncompressed-rgb.md)
4.  <span data-ttu-id="5d881-112">Exécutez le graphique.</span><span class="sxs-lookup"><span data-stu-id="5d881-112">Run the graph.</span></span>

<span data-ttu-id="5d881-113">La capture à partir d’une bande VTR fonctionne comme la capture de vidéos en direct à partir de l’appareil photo, sauf que vous devez lire la bande, comme décrit dans [contrôle d’un caméscope DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="5d881-113">Capturing from a VTR tape works just like capturing live video from the camera, except that you must play the tape, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span> <span data-ttu-id="5d881-114">Pour éviter de perdre des frames, exécutez d’abord le graphique, puis jouez la bande.</span><span class="sxs-lookup"><span data-stu-id="5d881-114">To avoid losing any frames, run the graph first, and then play the tape.</span></span> <span data-ttu-id="5d881-115">Lorsque vous avez terminé la transmission, arrêtez d’abord la bande, puis arrêtez le graphique.</span><span class="sxs-lookup"><span data-stu-id="5d881-115">When you are done transmitting, stop the tape first and then stop the graph.</span></span>

> [!Note]  
> <span data-ttu-id="5d881-116">Le caméscope doit être en mode VTR.</span><span class="sxs-lookup"><span data-stu-id="5d881-116">The camcorder must be in VTR mode.</span></span> <span data-ttu-id="5d881-117">Consultez [mode](device-mode.md)de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5d881-117">See [Device Mode](device-mode.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5d881-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5d881-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d881-119">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="5d881-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="5d881-120">Types-1 et fichiers AVI DV type-2</span><span class="sxs-lookup"><span data-stu-id="5d881-120">Type-1 vs. Type-2 DV AVI Files</span></span>](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[<span data-ttu-id="5d881-121">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="5d881-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



