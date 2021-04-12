---
description: Combinaison de la capture vidéo et de l’aperçu
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinaison de la capture vidéo et de l’aperçu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481176"
---
# <a name="combining-video-capture-and-preview"></a><span data-ttu-id="d083c-103">Combinaison de la capture vidéo et de l’aperçu</span><span class="sxs-lookup"><span data-stu-id="d083c-103">Combining Video Capture and Preview</span></span>

<span data-ttu-id="d083c-104">Les sections précédentes décrivent comment capturer des vidéos dans divers formats de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d083c-104">The previous sections describe how to capture video to various file formats.</span></span> <span data-ttu-id="d083c-105">La section aperçu de la [vidéo](previewing-video.md) décrit comment créer un graphique d’aperçu instantané.</span><span class="sxs-lookup"><span data-stu-id="d083c-105">The section [Previewing Video](previewing-video.md) describes how to build a live preview graph.</span></span> <span data-ttu-id="d083c-106">Toutefois, de nombreuses applications doivent effectuer les deux à la fois.</span><span class="sxs-lookup"><span data-stu-id="d083c-106">However, many applications must do both at once.</span></span> <span data-ttu-id="d083c-107">Pour créer un graphique combiné d’aperçu et d’écriture de fichiers, effectuez simplement deux appels à [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span><span class="sxs-lookup"><span data-stu-id="d083c-107">To build a combined preview and file-writing graph, simply make two calls to [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span></span>


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



<span data-ttu-id="d083c-108">Dans ce code, le générateur de graphiques de capture masque certains détails :</span><span class="sxs-lookup"><span data-stu-id="d083c-108">In this code, the Capture Graph Builder is hiding some details:</span></span>

-   <span data-ttu-id="d083c-109">Si le filtre de capture a une broche d’aperçu ou un code PIN de port vidéo, ainsi qu’un code confidentiel de capture, la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) affiche simplement les deux broches, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d083c-109">If the capture filter has a preview pin or video port pin, plus a capture pin, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method simply renders both pins, as shown in the following illustration.</span></span>

    ![graphique de capture et d’aperçu](images/vidcap04.png)

-   <span data-ttu-id="d083c-111">Si le filtre a uniquement un code confidentiel de capture, le générateur de graphiques de capture utilise le filtre [tee intelligent](smart-tee-filter.md) pour fractionner le flux de capture.</span><span class="sxs-lookup"><span data-stu-id="d083c-111">If the filter has only a capture pin, the Capture Graph Builder uses the [Smart Tee](smart-tee-filter.md) filter to split the capture stream.</span></span> <span data-ttu-id="d083c-112">L’illustration suivante montre le graphique avec un tee Smart.</span><span class="sxs-lookup"><span data-stu-id="d083c-112">The following illustration shows the graph with a Smart Tee.</span></span>

    ![capturer et afficher un aperçu du graphique avec le filtre tee intelligent](images/vidcap05.png)

<span data-ttu-id="d083c-114">Le filtre tee intelligent a un code confidentiel de capture et un code PIN de prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="d083c-114">The Smart Tee filter has a capture pin and a preview pin.</span></span> <span data-ttu-id="d083c-115">Il prend un flux vidéo unique du filtre de capture et le divise en deux flux, un pour la capture et un pour l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="d083c-115">It takes a single video stream from the capture filter and splits it into two streams, one for capture and one for preview.</span></span> <span data-ttu-id="d083c-116">Pour maintenir le débit sur le code confidentiel de capture, la broche de prévisualisation supprime les frames en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="d083c-116">To maintain throughput on the capture pin, the preview pin drops frames as needed.</span></span> <span data-ttu-id="d083c-117">Elle supprime également les horodatages de chaque exemple avant de la diffuser, pour les raisons décrites dans la rubrique [filtres de capture vidéo DirectShow](directshow-video-capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d083c-117">It also strips the time stamps from each sample before delivering it, for the reasons discussed in the topic [DirectShow Video Capture Filters](directshow-video-capture-filters.md).</span></span>

<span data-ttu-id="d083c-118">Bien que le tee intelligent fractionne le flux, il ne duplique pas physiquement les données vidéo.</span><span class="sxs-lookup"><span data-stu-id="d083c-118">Although the Smart Tee splits the stream, it does not physically duplicate the video data.</span></span> <span data-ttu-id="d083c-119">Au lieu de cela, il utilise des exemples d’objets de média personnalisés qui partagent les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="d083c-119">Instead, it uses custom media sample objects that share the buffers.</span></span> <span data-ttu-id="d083c-120">Les exemples sont marqués en lecture seule pour s’assurer que les filtres en aval n’écrivent pas sur les données.</span><span class="sxs-lookup"><span data-stu-id="d083c-120">The samples are marked "read-only" to ensure that downstream filters do not write on the data.</span></span>

<span data-ttu-id="d083c-121">Si votre graphique de capture a une fenêtre d’aperçu, plusieurs choses peuvent entraîner l’arrêt de l’ensemble du graphique par le gestionnaire de graphique de filtre, y compris le flux de capture :</span><span class="sxs-lookup"><span data-stu-id="d083c-121">If your capture graph has a preview window, several things can cause the Filter Graph Manager to stop the entire graph, including the capture stream:</span></span>

-   <span data-ttu-id="d083c-122">Verrouillage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d083c-122">Locking the computer.</span></span>
-   <span data-ttu-id="d083c-123">En appuyant sur CTRL + ALT + SUPPR sur un ordinateur qui est membre d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="d083c-123">Pressing CTRL+ALT+DELETE on a computer that is a member of a domain.</span></span>
-   <span data-ttu-id="d083c-124">Exécution d’une application Direct3D en plein écran, telle qu’un jeu ou un économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="d083c-124">Running a full-screen Direct3D application, such as a game or screen saver.</span></span>
-   <span data-ttu-id="d083c-125">Basculement des moniteurs ou modification de la résolution d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d083c-125">Switching monitors or changing the display resolution.</span></span>
-   <span data-ttu-id="d083c-126">Exécution d’un programme qui amène Windows à afficher une boîte de dialogue de contrôle de compte d’utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="d083c-126">Running a program that causes Windows to display a User Account Control (UAC) dialog.</span></span> <span data-ttu-id="d083c-127">(Windows Vista ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="d083c-127">(Windows Vista or later.)</span></span>
-   <span data-ttu-id="d083c-128">Exécution d’une fenêtre DOS plein écran.</span><span class="sxs-lookup"><span data-stu-id="d083c-128">Running a full-screen DOS window.</span></span>

<span data-ttu-id="d083c-129">L’un de ces événements peut interrompre la session de capture, ce qui peut entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="d083c-129">Any of these events might interrupt the capture session, possibly causing data loss.</span></span> <span data-ttu-id="d083c-130">(Voici ce qui se produit en interne : le convertisseur vidéo perd les ressources Direct3D ou DirectDraw dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="d083c-130">(Here is what happens internally: The video renderer loses the Direct3D or DirectDraw resources that it needs.</span></span> <span data-ttu-id="d083c-131">Dans le processus de récupération de ces ressources, le convertisseur vidéo doit se reconnecter au filtre en amont, ce qui amène le gestionnaire de graphes de filtre à arrêter le graphique.</span><span class="sxs-lookup"><span data-stu-id="d083c-131">In the process of recovering those resources, the video renderer must reconnect with the upstream filter, causing the Filter Graph Manager to stop the graph.)</span></span>

<span data-ttu-id="d083c-132">Deux solutions possibles à ce problème sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d083c-132">Two possible solutions to this problem are the following:</span></span>

-   <span data-ttu-id="d083c-133">N’incluez pas de flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="d083c-133">Do not include a preview stream.</span></span> <span data-ttu-id="d083c-134">Toutefois, sachez que la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ajoute automatiquement une fenêtre d’aperçu lorsque l’appareil de capture a une broche de port vidéo.</span><span class="sxs-lookup"><span data-stu-id="d083c-134">However, be aware that the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically adds a preview window when the capture device has a video port pin.</span></span> <span data-ttu-id="d083c-135">Consultez les [broches des ports vidéo dans la capture de fichiers](video-port-pins-in-file-capture.md).</span><span class="sxs-lookup"><span data-stu-id="d083c-135">See [Video Port Pins in File Capture](video-port-pins-in-file-capture.md).</span></span>
-   <span data-ttu-id="d083c-136">Utilisez le moteur de mémoire tampon de flux pour envoyer le flux d’aperçu à un graphique dans un autre processus.</span><span class="sxs-lookup"><span data-stu-id="d083c-136">Use the Stream Buffer Engine to send the preview stream to a graph in another process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d083c-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d083c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d083c-138">Capture vidéo dans un fichier</span><span class="sxs-lookup"><span data-stu-id="d083c-138">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



