---
description: Transmettre le fichier DV du fichier à la bande
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmettre le fichier DV du fichier à la bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529366"
---
# <a name="transmit-dv-from-file-to-tape"></a><span data-ttu-id="4abbf-103">Transmettre le fichier DV du fichier à la bande</span><span class="sxs-lookup"><span data-stu-id="4abbf-103">Transmit DV from File to Tape</span></span>

<span data-ttu-id="4abbf-104">La transmission d’un fichier DV AVI à VTR Tape est compliquée par le fait que les fichiers peuvent être de type-1 ou-2.</span><span class="sxs-lookup"><span data-stu-id="4abbf-104">Transmit from DV AVI file to VTR tape is complicated somewhat by the fact that files can type-1 or type-2.</span></span> <span data-ttu-id="4abbf-105">Pour transmettre un fichier DV à une bande, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4abbf-105">To transmit a DV file to tape, do the following:</span></span>

1.  <span data-ttu-id="4abbf-106">Créez une instance du filtre de [pilote MSDV](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="4abbf-106">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="4abbf-107">Pour plus d’informations, consultez [sélection d’un périphérique de capture](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="4abbf-107">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="4abbf-108">Assurez-vous que l’appareil est en mode VTR.</span><span class="sxs-lookup"><span data-stu-id="4abbf-108">Make sure the device is in VTR mode.</span></span> <span data-ttu-id="4abbf-109">Dans le cas contraire, vous ne pourrez pas transmettre à la bande. Consultez [mode](device-mode.md)de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4abbf-109">Otherwise, you cannot transmit to tape.See [Device Mode](device-mode.md).</span></span>
3.  <span data-ttu-id="4abbf-110">Initialisez le générateur de graphiques de capture, comme décrit dans [à propos du générateur de graphiques de capture](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="4abbf-110">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
4.  <span data-ttu-id="4abbf-111">Générez le graphique.</span><span class="sxs-lookup"><span data-stu-id="4abbf-111">Build the graph.</span></span> <span data-ttu-id="4abbf-112">La configuration du graphique dépend du type de fichier DV :</span><span class="sxs-lookup"><span data-stu-id="4abbf-112">The graph configuration depends on the DV file type:</span></span>
    -   [<span data-ttu-id="4abbf-113">Transmettre à partir d’un fichier de type-1</span><span class="sxs-lookup"><span data-stu-id="4abbf-113">Transmit from Type-1 File</span></span>](transmit-from-type-1-file.md)
    -   [<span data-ttu-id="4abbf-114">Transmettre à partir du fichier de type 2</span><span class="sxs-lookup"><span data-stu-id="4abbf-114">Transmit from Type-2 File</span></span>](transmit-from-type-2-file.md)
5.  <span data-ttu-id="4abbf-115">Mettez l’appareil en mode de pause d’enregistrement, comme décrit dans [contrôle d’un caméscope DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="4abbf-115">Put the device into record-pause mode, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>
6.  <span data-ttu-id="4abbf-116">Suspendez le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4abbf-116">Pause the filter graph.</span></span> <span data-ttu-id="4abbf-117">Lorsque le graphique de filtre est suspendu, il envoie un flux continu qui répète la première image de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="4abbf-117">While the filter graph is paused, it sends a continuous stream that repeats the first frame of video.</span></span>
7.  <span data-ttu-id="4abbf-118">Pour commencer la transmission, mettez l’appareil en mode enregistrement, puis exécutez le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4abbf-118">To start transmitting, put the device into record mode and then run the filter graph.</span></span> <span data-ttu-id="4abbf-119">L’appareil prend un certain temps jusqu’à ce que la tête d’enregistrement puisse enregistrer, donc patientez environ deux secondes avant d’exécuter le graphique.</span><span class="sxs-lookup"><span data-stu-id="4abbf-119">It takes the device a certain amount of time until the recording head is able to record, so wait for about two seconds before running the graph.</span></span> <span data-ttu-id="4abbf-120">Cela peut entraîner quelques images dupliquées au début de la bande, mais elle garantit qu’aucune donnée n’est perdue.</span><span class="sxs-lookup"><span data-stu-id="4abbf-120">This might result in a few duplicated frames at the beginning of the tape, but it ensures that no data is lost.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4abbf-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4abbf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4abbf-122">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="4abbf-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



