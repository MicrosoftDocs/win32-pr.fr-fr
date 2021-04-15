---
description: Le traitement vidéo DXVA encapsule les fonctions du matériel graphique dédié au traitement d’images vidéo non compressées. Les services de traitement vidéo incluent l’entrelacement et le mixage vidéo.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Traitement vidéo DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524543"
---
# <a name="dxva-video-processing"></a><span data-ttu-id="b2005-104">Traitement vidéo DXVA</span><span class="sxs-lookup"><span data-stu-id="b2005-104">DXVA Video Processing</span></span>

<span data-ttu-id="b2005-105">Le traitement vidéo DXVA encapsule les fonctions du matériel graphique dédié au traitement d’images vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="b2005-105">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="b2005-106">Les services de traitement vidéo incluent l’entrelacement et le mixage vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-106">Video processing services include deinterlacing and video mixing.</span></span>

<span data-ttu-id="b2005-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2005-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b2005-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b2005-108">Overview</span></span>](#overview)
-   [<span data-ttu-id="b2005-109">Création d’un périphérique de traitement vidéo</span><span class="sxs-lookup"><span data-stu-id="b2005-109">Creating a Video Processing Device</span></span>](#creating-a-video-processing-device)
    -   [<span data-ttu-id="b2005-110">Obtient le pointeur IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="b2005-110">Get the IDirectXVideoProcessorService Pointer</span></span>](#get-the-idirectxvideoprocessorservice-pointer)
    -   [<span data-ttu-id="b2005-111">Énumérer les appareils de traitement vidéo</span><span class="sxs-lookup"><span data-stu-id="b2005-111">Enumerate the Video Processing Devices</span></span>](#enumerate-the-video-processing-devices)
    -   [<span data-ttu-id="b2005-112">Énumérer les formats de Render-Target</span><span class="sxs-lookup"><span data-stu-id="b2005-112">Enumerate Render-Target Formats</span></span>](#enumerate-render-target-formats)
    -   [<span data-ttu-id="b2005-113">Interroger les fonctionnalités de l’appareil</span><span class="sxs-lookup"><span data-stu-id="b2005-113">Query the Device Capabilities</span></span>](#query-the-device-capabilities)
    -   [<span data-ttu-id="b2005-114">Créer l’appareil</span><span class="sxs-lookup"><span data-stu-id="b2005-114">Create the Device</span></span>](#create-the-device)
-   [<span data-ttu-id="b2005-115">Blit de traitement vidéo</span><span class="sxs-lookup"><span data-stu-id="b2005-115">Video Process Blit</span></span>](#video-process-blit)
    -   [<span data-ttu-id="b2005-116">Paramètres blit</span><span class="sxs-lookup"><span data-stu-id="b2005-116">Blit Parameters</span></span>](#blit-parameters)
    -   [<span data-ttu-id="b2005-117">Exemples d’entrée</span><span class="sxs-lookup"><span data-stu-id="b2005-117">Input Samples</span></span>](#input-samples)
-   [<span data-ttu-id="b2005-118">Composition de l’image</span><span class="sxs-lookup"><span data-stu-id="b2005-118">Image Composition</span></span>](#image-composition)
    -   [<span data-ttu-id="b2005-119">Exemple 1 : cadre</span><span class="sxs-lookup"><span data-stu-id="b2005-119">Example 1: Letterboxing</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="b2005-120">Exemple 2 : étirer des images de sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-120">Example 2: Stretching Substream Images</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="b2005-121">Exemple 3 : hauteurs de flux incompatibles</span><span class="sxs-lookup"><span data-stu-id="b2005-121">Example 3: Mismatched Stream Heights</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="b2005-122">Exemple 4 : rectangle cible plus petit que la surface de destination</span><span class="sxs-lookup"><span data-stu-id="b2005-122">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [<span data-ttu-id="b2005-123">Exemple 5 : rectangles sources</span><span class="sxs-lookup"><span data-stu-id="b2005-123">Example 5: Source Rectangles</span></span>](#example-5-source-rectangles)
    -   [<span data-ttu-id="b2005-124">Exemple 6 : rectangles de destination d’intersection</span><span class="sxs-lookup"><span data-stu-id="b2005-124">Example 6: Intersecting Destination Rectangles</span></span>](#example-6-intersecting-destination-rectangles)
    -   [<span data-ttu-id="b2005-125">Exemple 7 : vidéo sur l’étirement et le rognage</span><span class="sxs-lookup"><span data-stu-id="b2005-125">Example 7: Stretching and Cropping Video</span></span>](#example-7-stretching-and-cropping-video)
-   [<span data-ttu-id="b2005-126">Ordre de l’exemple d’entrée</span><span class="sxs-lookup"><span data-stu-id="b2005-126">Input Sample Order</span></span>](#input-sample-order)
    -   [<span data-ttu-id="b2005-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b2005-127">Example 1</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="b2005-128">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b2005-128">Example 2</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="b2005-129">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="b2005-129">Example 3</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="b2005-130">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="b2005-130">Example 4</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
-   [<span data-ttu-id="b2005-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2005-131">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="b2005-132">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b2005-132">Overview</span></span>

<span data-ttu-id="b2005-133">Le matériel graphique peut utiliser l’unité de traitement graphique (GPU) pour traiter les images vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="b2005-133">Graphics hardware can use the graphics processing unit (GPU) to process uncompressed video images.</span></span> <span data-ttu-id="b2005-134">Un périphérique de *traitement vidéo* est un composant logiciel qui encapsule ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="b2005-134">A *video processing* device is a software component that encapsulates these functions.</span></span> <span data-ttu-id="b2005-135">Les applications peuvent utiliser un appareil de traitement vidéo pour exécuter des fonctions telles que :</span><span class="sxs-lookup"><span data-stu-id="b2005-135">Applications can use a video processing device to perform functions such as:</span></span>

-   <span data-ttu-id="b2005-136">Désentrelacement et inversement</span><span class="sxs-lookup"><span data-stu-id="b2005-136">Deinterlacing and inverse telecine</span></span>
-   <span data-ttu-id="b2005-137">Mixage de sous-flux vidéo sur l’image vidéo principale</span><span class="sxs-lookup"><span data-stu-id="b2005-137">Mixing video substreams onto the main video image</span></span>
-   <span data-ttu-id="b2005-138">Réglage des couleurs (ProcAmp) et filtrage d’images</span><span class="sxs-lookup"><span data-stu-id="b2005-138">Color adjustment (ProcAmp) and image filtering</span></span>
-   <span data-ttu-id="b2005-139">Mise à l’échelle des images</span><span class="sxs-lookup"><span data-stu-id="b2005-139">Image scaling</span></span>
-   <span data-ttu-id="b2005-140">Conversion de l’espace colorimétrique</span><span class="sxs-lookup"><span data-stu-id="b2005-140">Color-space conversion</span></span>
-   <span data-ttu-id="b2005-141">Fusion alpha</span><span class="sxs-lookup"><span data-stu-id="b2005-141">Alpha blending</span></span>

<span data-ttu-id="b2005-142">Le diagramme suivant montre les étapes du pipeline de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-142">The following diagram shows the stages in the video processing pipeline.</span></span> <span data-ttu-id="b2005-143">Le diagramme n’est pas destiné à illustrer une implémentation réelle.</span><span class="sxs-lookup"><span data-stu-id="b2005-143">The diagram is not meant to show an actual implementation.</span></span> <span data-ttu-id="b2005-144">Par exemple, le pilote Graphics peut combiner plusieurs étapes en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="b2005-144">For example, the graphics driver might combine several stages into a single operation.</span></span> <span data-ttu-id="b2005-145">Toutes ces opérations peuvent être effectuées dans un seul appel à l’appareil de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-145">All of these operations can be performed in a single call to the video processing device.</span></span> <span data-ttu-id="b2005-146">Certaines étapes présentées ici, telles que le filtrage du bruit et du détail, peuvent ne pas être prises en charge par le pilote.</span><span class="sxs-lookup"><span data-stu-id="b2005-146">Some stages shown here, such as noise and detail filtering, might not be supported by the driver.</span></span>

![Diagramme montrant les étapes du traitement vidéo DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

<span data-ttu-id="b2005-148">L’entrée du pipeline de traitement vidéo inclut toujours un flux vidéo *principal* , qui contient les données d’image principales.</span><span class="sxs-lookup"><span data-stu-id="b2005-148">The input to the video processing pipeline always includes a *primary* video stream, which contains the main image data.</span></span> <span data-ttu-id="b2005-149">Le flux vidéo principal détermine la fréquence d’images de la vidéo de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2005-149">The primary video stream determines the frame rate for the output video.</span></span> <span data-ttu-id="b2005-150">Chaque image de la vidéo de sortie est calculée par rapport aux données d’entrée du flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-150">Each frame of the output video is calculated relative to the input data from the primary video stream.</span></span> <span data-ttu-id="b2005-151">Les pixels du flux principal sont toujours opaques, sans données alpha par pixel.</span><span class="sxs-lookup"><span data-stu-id="b2005-151">Pixels in the primary stream are always opaque, with no per-pixel alpha data.</span></span> <span data-ttu-id="b2005-152">Le flux vidéo principal peut être progressif ou entrelacé.</span><span class="sxs-lookup"><span data-stu-id="b2005-152">The primary video stream can be progressive or interlaced.</span></span>

<span data-ttu-id="b2005-153">Le pipeline de traitement vidéo peut éventuellement recevoir jusqu’à 15 sous-flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-153">Optionally, the video processing pipeline can receive up to 15 video substreams.</span></span> <span data-ttu-id="b2005-154">Un sous-flux contient des données d’image auxiliaire, telles que des sous-titres ou des sous-images de DVD.</span><span class="sxs-lookup"><span data-stu-id="b2005-154">A substream contains auxiliary image data, such as closed captions or DVD subpictures.</span></span> <span data-ttu-id="b2005-155">Ces images sont affichées sur le flux vidéo principal et ne sont généralement pas censées être affichées par elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="b2005-155">These images are displayed over the primary video stream, and are generally not meant to be shown by themselves.</span></span> <span data-ttu-id="b2005-156">Les images de sous-flux peuvent contenir des données alpha par pixel et sont toujours des images progressives.</span><span class="sxs-lookup"><span data-stu-id="b2005-156">Substream pictures can contain per-pixel alpha data, and are always progressive frames.</span></span> <span data-ttu-id="b2005-157">L’appareil de traitement vidéo alpha-fusionne les images de sous-flux avec la trame désentrelacée actuelle du flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-157">The video processing device alpha-blends the substream images with the current deinterlaced frame from the primary video stream.</span></span>

<span data-ttu-id="b2005-158">Dans le reste de cette rubrique, le terme *image* est utilisé pour les données d’entrée sur un appareil de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-158">In the remainder of this topic, the term *picture* is used for the input data to a video processing device.</span></span> <span data-ttu-id="b2005-159">Une image peut se composer d’une trame progressive, d’un champ unique ou de deux champs entrelacés.</span><span class="sxs-lookup"><span data-stu-id="b2005-159">A picture might consist of a progressive frame, a single field, or two interleaved fields.</span></span> <span data-ttu-id="b2005-160">La sortie est toujours un frame désentrelacé.</span><span class="sxs-lookup"><span data-stu-id="b2005-160">The output is always a deinterlaced frame.</span></span>

<span data-ttu-id="b2005-161">Un pilote vidéo peut implémenter plusieurs périphériques de traitement vidéo pour fournir différents jeux de fonctionnalités de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-161">A video driver can implement more than one video processing device, to provide different sets of video processing capabilities.</span></span> <span data-ttu-id="b2005-162">Les appareils sont identifiés par un GUID.</span><span class="sxs-lookup"><span data-stu-id="b2005-162">Devices are identified by GUID.</span></span> <span data-ttu-id="b2005-163">Les GUID suivants sont prédéfinis :</span><span class="sxs-lookup"><span data-stu-id="b2005-163">The following GUIDs are predefined:</span></span>

-   <span data-ttu-id="b2005-164">**DXVA2 \_ VideoProcBobDevice**.</span><span class="sxs-lookup"><span data-stu-id="b2005-164">**DXVA2\_VideoProcBobDevice**.</span></span> <span data-ttu-id="b2005-165">Cet appareil effectue une désentrelacement Bob.</span><span class="sxs-lookup"><span data-stu-id="b2005-165">This device performs bob deinterlacing.</span></span>
-   <span data-ttu-id="b2005-166">**DXVA2 \_ VideoProcProgressiveDevice**.</span><span class="sxs-lookup"><span data-stu-id="b2005-166">**DXVA2\_VideoProcProgressiveDevice**.</span></span> <span data-ttu-id="b2005-167">Ce périphérique est utilisé si la vidéo contient uniquement des images progressives, sans Frame entrelacé.</span><span class="sxs-lookup"><span data-stu-id="b2005-167">This device is used if the video contains only progressive frames, with no interlaced frames.</span></span> <span data-ttu-id="b2005-168">(Un contenu vidéo contient un mélange d’images progressives et entrelacées.</span><span class="sxs-lookup"><span data-stu-id="b2005-168">(Some video content contains a mix of progressive and interlaced frames.</span></span> <span data-ttu-id="b2005-169">L’appareil progressif ne peut pas être utilisé pour ce type de contenu vidéo « mixte », car une étape de désentrelacement est requise pour les images entrelacées.)</span><span class="sxs-lookup"><span data-stu-id="b2005-169">The progressive device cannot be used for this kind of "mixed" video content, because a deinterlacing step is required for the interlaced frames.)</span></span>

<span data-ttu-id="b2005-170">Chaque pilote graphique qui prend en charge le traitement vidéo DXVA doit implémenter au moins ces deux appareils.</span><span class="sxs-lookup"><span data-stu-id="b2005-170">Every graphics driver that supports DXVA video processing must implement at least these two devices.</span></span> <span data-ttu-id="b2005-171">Le pilote Graphics peut également fournir d’autres périphériques, identifiés par des GUID spécifiques au pilote.</span><span class="sxs-lookup"><span data-stu-id="b2005-171">The graphics driver may also provide other devices, which are identified by driver-specific GUIDs.</span></span> <span data-ttu-id="b2005-172">Par exemple, un pilote peut implémenter un algorithme de désentrelacement propriétaire qui produit une sortie de qualité supérieure à celle de Bob.</span><span class="sxs-lookup"><span data-stu-id="b2005-172">For example, a driver might implement a proprietary deinterlacing algorithm that produces better quality output than bob deinterlacing.</span></span> <span data-ttu-id="b2005-173">Certains algorithmes de désentrelacement peuvent nécessiter des images de référence vers l’avant ou vers l’arrière à partir du flux principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-173">Some deinterlacing algorithms may require forward or backward reference pictures from the primary stream.</span></span> <span data-ttu-id="b2005-174">Dans ce cas, l’appelant doit fournir ces images au pilote dans l’ordre approprié, comme décrit plus loin dans cette section.</span><span class="sxs-lookup"><span data-stu-id="b2005-174">If so, the caller must provide these pictures to the driver in the correct sequence, as described later in this section.</span></span>

<span data-ttu-id="b2005-175">Un périphérique logiciel de référence est également fourni.</span><span class="sxs-lookup"><span data-stu-id="b2005-175">A reference software device is also provided.</span></span> <span data-ttu-id="b2005-176">L’appareil logiciel est optimisé pour une qualité supérieure à la vitesse et peut ne pas être adapté au traitement vidéo en temps réel.</span><span class="sxs-lookup"><span data-stu-id="b2005-176">The software device is optimized for quality rather than speed, and may not be adequate for real-time video processing.</span></span> <span data-ttu-id="b2005-177">Le périphérique logiciel de référence utilise la valeur GUID DXVA2 \_ VideoProcSoftwareDevice.</span><span class="sxs-lookup"><span data-stu-id="b2005-177">The reference software device uses the GUID value DXVA2\_VideoProcSoftwareDevice.</span></span>

## <a name="creating-a-video-processing-device"></a><span data-ttu-id="b2005-178">Création d’un périphérique de traitement vidéo</span><span class="sxs-lookup"><span data-stu-id="b2005-178">Creating a Video Processing Device</span></span>

<span data-ttu-id="b2005-179">Avant d’utiliser le traitement vidéo DXVA, l’application doit créer un périphérique de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-179">Before using DXVA video processing, the application must create a video processing device.</span></span> <span data-ttu-id="b2005-180">Voici un bref aperçu des étapes qui sont expliquées plus en détail dans le reste de cette section :</span><span class="sxs-lookup"><span data-stu-id="b2005-180">Here is a brief outline of the steps, which are explained in greater detail in the remainder of this section:</span></span>

1.  <span data-ttu-id="b2005-181">Obtient un pointeur vers l’interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .</span><span class="sxs-lookup"><span data-stu-id="b2005-181">Get a pointer to the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface.</span></span>
2.  <span data-ttu-id="b2005-182">Créez une description du format vidéo pour le flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-182">Create a description of the video format for the primary video stream.</span></span> <span data-ttu-id="b2005-183">Utilisez cette description pour obtenir la liste des périphériques de traitement vidéo qui prennent en charge le format vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-183">Use this description to get a list of the video processing devices that support the video format.</span></span> <span data-ttu-id="b2005-184">Les appareils sont identifiés par un GUID.</span><span class="sxs-lookup"><span data-stu-id="b2005-184">Devices are identified by GUID.</span></span>
3.  <span data-ttu-id="b2005-185">Pour un appareil particulier, obtenir la liste des formats de cible de rendu pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2005-185">For a particular device, get a list of render-target formats supported by the device.</span></span> <span data-ttu-id="b2005-186">Les formats sont retournés sous la forme d’une liste de valeurs **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="b2005-186">The formats are returned as a list of **D3DFORMAT** values.</span></span> <span data-ttu-id="b2005-187">Si vous envisagez de mélanger des sous-flux, récupérez également la liste des formats de sous-flux pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2005-187">If you plan to mix substreams, get a list of the supported substream formats as well.</span></span>
4.  <span data-ttu-id="b2005-188">Interroger les fonctionnalités de chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="b2005-188">Query the capabilities of each device.</span></span>
5.  <span data-ttu-id="b2005-189">Créez le périphérique de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-189">Create the video processing device.</span></span>

<span data-ttu-id="b2005-190">Parfois, vous pouvez omettre certaines de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="b2005-190">Sometimes you can omit some of these steps.</span></span> <span data-ttu-id="b2005-191">Par exemple, au lieu d’obtenir la liste des formats de cible de rendu, vous pouvez simplement essayer de créer le périphérique de traitement vidéo avec votre format préféré et voir s’il a été correctement exécuté.</span><span class="sxs-lookup"><span data-stu-id="b2005-191">For example, instead of getting the list of render-target formats, you could simply try creating the video processing device with your preferred format, and see if it succeeds.</span></span> <span data-ttu-id="b2005-192">Un format courant, tel que D3DFMT \_ X8R8G8B8, est susceptible d’être correctement exécuté.</span><span class="sxs-lookup"><span data-stu-id="b2005-192">A common format such as D3DFMT\_X8R8G8B8 is likely to succeed.</span></span>

<span data-ttu-id="b2005-193">Le reste de cette section décrit ces étapes en détail.</span><span class="sxs-lookup"><span data-stu-id="b2005-193">The remainder of this section describes these steps in detail.</span></span>

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a><span data-ttu-id="b2005-194">Obtient le pointeur IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="b2005-194">Get the IDirectXVideoProcessorService Pointer</span></span>

<span data-ttu-id="b2005-195">L’interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) est obtenue à partir de l’appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b2005-195">The [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface is obtained from the Direct3D device.</span></span> <span data-ttu-id="b2005-196">Il existe deux façons d’obtenir un pointeur vers cette interface :</span><span class="sxs-lookup"><span data-stu-id="b2005-196">There are two ways to get a pointer to this interface:</span></span>

-   <span data-ttu-id="b2005-197">À partir d’un appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b2005-197">From a Direct3D device.</span></span>
-   <span data-ttu-id="b2005-198">À partir de la [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="b2005-198">From the [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="b2005-199">Si vous avez un pointeur vers un appareil Direct3D, vous pouvez obtenir un pointeur [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) en appelant la fonction [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) .</span><span class="sxs-lookup"><span data-stu-id="b2005-199">If you have a pointer to a Direct3D device, you can get an [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer by calling the [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) function.</span></span> <span data-ttu-id="b2005-200">Transmettez un pointeur vers l’interface **IDirect3DDevice9** de l’appareil et spécifiez **IID \_ IDirectXVideoProcessorService** pour le paramètre *riid* , comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b2005-200">Pass in a pointer to the device's **IDirect3DDevice9** interface, and specify **IID\_IDirectXVideoProcessorService** for the *riid* parameter, as shown in the following code:</span></span>


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



<span data-ttu-id="b2005-201">dans certains cas, un objet crée le périphérique Direct3D, puis le partage avec d’autres objets via le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="b2005-201">n some cases, one object creates the Direct3D device and then shares it with other objects through the [Direct3D Device Manager](direct3d-device-manager.md).</span></span> <span data-ttu-id="b2005-202">Dans ce cas, vous pouvez appeler [**IDirect3DDeviceManager9 :: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) sur le gestionnaire de périphériques pour accéder au pointeur [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b2005-202">In this situation, you can call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) on the device manager to get the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer, as shown in the following code:</span></span>


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a><span data-ttu-id="b2005-203">Énumérer les appareils de traitement vidéo</span><span class="sxs-lookup"><span data-stu-id="b2005-203">Enumerate the Video Processing Devices</span></span>

<span data-ttu-id="b2005-204">Pour obtenir la liste des périphériques de traitement vidéo, remplissez une structure [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) avec le format du flux vidéo principal, puis transmettez cette structure à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) .</span><span class="sxs-lookup"><span data-stu-id="b2005-204">To get a list of video processing devices, fill in a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure with the format of the primary video stream, and pass this structure to the [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method.</span></span> <span data-ttu-id="b2005-205">La méthode retourne un tableau de GUID, un pour chaque périphérique de traitement vidéo qui peut être utilisé avec ce format vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-205">The method returns an array of GUIDs, one for each video processing device that can be used with this video format.</span></span>

<span data-ttu-id="b2005-206">Prenons l’exemple d’une application qui affiche un flux vidéo au format YUY2, à l’aide de la définition BT. 709 de couleur YUV, avec une fréquence d’images de 29,97 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="b2005-206">Consider an application that renders a video stream in YUY2 format, using the BT.709 definition of YUV color, with a frame rate of 29.97 frames per second.</span></span> <span data-ttu-id="b2005-207">Supposons que le contenu vidéo se compose uniquement d’images progressives.</span><span class="sxs-lookup"><span data-stu-id="b2005-207">Assume that the video content consists entirely of progressive frames.</span></span> <span data-ttu-id="b2005-208">Le fragment de code suivant montre comment remplir la description de format et récupérer les GUID d’appareil :</span><span class="sxs-lookup"><span data-stu-id="b2005-208">The following code fragment shows how to fill in the format description and get the device GUIDs:</span></span>


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



<span data-ttu-id="b2005-209">Le code de cet exemple provient de l’exemple du kit de développement logiciel (SDK) [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="b2005-209">The code for this example is taken from the [DXVA2\_VideoProc](dxva2-videoproc-sample.md) SDK sample.</span></span>

<span data-ttu-id="b2005-210">Dans cet exemple, le tableau *pGuids* est alloué par la méthode [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , de sorte que l’application doit libérer le tableau en appelant [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="b2005-210">The *pGuids* array in this example is allocated by the [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method, so the application must free the array by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="b2005-211">Les étapes restantes peuvent être effectuées à l’aide de l’un des GUID d’appareil retournés par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b2005-211">The remaining steps can be performed using any of the device GUIDs returned by this method.</span></span>

### <a name="enumerate-render-target-formats"></a><span data-ttu-id="b2005-212">Énumérer les formats de Render-Target</span><span class="sxs-lookup"><span data-stu-id="b2005-212">Enumerate Render-Target Formats</span></span>

<span data-ttu-id="b2005-213">Pour obtenir la liste des formats de cible de rendu pris en charge par l’appareil, transmettez le GUID de l’appareil et la structure [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b2005-213">To get the list of render-target formats supported by the device, pass the device GUID and the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure to the [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) method, as shown in the following code:</span></span>


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="b2005-214">La méthode retourne un tableau de valeurs **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="b2005-214">The method returns an array of **D3DFORMAT** values.</span></span> <span data-ttu-id="b2005-215">Dans cet exemple, où le type d’entrée est YUY2, une liste type de formats peut être D3DFMT \_ X8R8G8B8 (32 bits RGB) et D3DMFT \_ YUY2 (format d’entrée).</span><span class="sxs-lookup"><span data-stu-id="b2005-215">In this example, where the input type is YUY2, a typical list of formats might be D3DFMT\_X8R8G8B8 (32-bit RGB) and D3DMFT\_YUY2 (the input format).</span></span> <span data-ttu-id="b2005-216">Toutefois, la liste exacte dépend du pilote.</span><span class="sxs-lookup"><span data-stu-id="b2005-216">However, the exact list will depend on the driver.</span></span>

<span data-ttu-id="b2005-217">La liste des formats disponibles pour les sous-flux peut varier en fonction du format de la cible de rendu et du format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b2005-217">The list of available formats for the substreams can vary depending on the render-target format and the input format.</span></span> <span data-ttu-id="b2005-218">Pour obtenir la liste des formats de sous-flux, transmettez le GUID de l’appareil, la structure du format et le format de la cible de rendu à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b2005-218">To get the list of substream formats, pass the device GUID, the format structure, and the render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) method, as shown in the following code:</span></span>


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="b2005-219">Cette méthode retourne un autre tableau de valeurs **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="b2005-219">This method returns another array of **D3DFORMAT** values.</span></span> <span data-ttu-id="b2005-220">Les formats de sous-flux types sont AYUV et AI44.</span><span class="sxs-lookup"><span data-stu-id="b2005-220">Typical substream formats are AYUV and AI44.</span></span>

### <a name="query-the-device-capabilities"></a><span data-ttu-id="b2005-221">Interroger les fonctionnalités de l’appareil</span><span class="sxs-lookup"><span data-stu-id="b2005-221">Query the Device Capabilities</span></span>

<span data-ttu-id="b2005-222">Pour obtenir les fonctionnalités d’un appareil particulier, transmettez le GUID de l’appareil, la structure du format et un format de cible de rendu à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) .</span><span class="sxs-lookup"><span data-stu-id="b2005-222">To get the capabilities of a particular device, pass the device GUID, the format structure, and a render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) method.</span></span> <span data-ttu-id="b2005-223">La méthode remplit une structure de structure [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) avec les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2005-223">The method fills in a [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure structure with the device capabilities.</span></span>


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a><span data-ttu-id="b2005-224">Créer l’appareil</span><span class="sxs-lookup"><span data-stu-id="b2005-224">Create the Device</span></span>

<span data-ttu-id="b2005-225">Pour créer le périphérique de traitement vidéo, appelez [**IDirectXVideoProcessorService :: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span><span class="sxs-lookup"><span data-stu-id="b2005-225">To create the video processing device, call [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span></span> <span data-ttu-id="b2005-226">L’entrée de cette méthode est le GUID de l’appareil, la description du format, le format de la cible de rendu et le nombre maximal de sous-flux que vous envisagez de mélanger.</span><span class="sxs-lookup"><span data-stu-id="b2005-226">The input to this method is the device GUID, the format description, the render-target format, and the maximum number of substreams that you plan to mix.</span></span> <span data-ttu-id="b2005-227">La méthode retourne un pointeur vers l’interface [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , qui représente le périphérique de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-227">The method returns a pointer to the [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) interface, which represents the video processing device.</span></span>


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a><span data-ttu-id="b2005-228">Blit de traitement vidéo</span><span class="sxs-lookup"><span data-stu-id="b2005-228">Video Process Blit</span></span>

<span data-ttu-id="b2005-229">L’opération principale de traitement vidéo est le *blit de traitement vidéo*.</span><span class="sxs-lookup"><span data-stu-id="b2005-229">The main video processing operation is the *video processing blit*.</span></span> <span data-ttu-id="b2005-230">(Un *blit* est une opération qui combine deux ou plusieurs bitmaps en une seule bitmap.</span><span class="sxs-lookup"><span data-stu-id="b2005-230">(A *blit* is any operation that combines two or more bitmaps into a single bitmap.</span></span> <span data-ttu-id="b2005-231">Un blit de traitement vidéo combine des images d’entrée pour créer un frame de sortie.) Pour effectuer un blit de traitement vidéo, appelez [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="b2005-231">A video processing blit combines input pictures to create an output frame.) To perform a video processing blit, call [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="b2005-232">Cette méthode passe un ensemble d’exemples de vidéos à l’appareil de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-232">This method passes a set of video samples to the video processing device.</span></span> <span data-ttu-id="b2005-233">En réponse, le périphérique de traitement vidéo traite les images d’entrée et génère une trame de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2005-233">In response, the video processing device processes the input pictures and generates one output frame.</span></span> <span data-ttu-id="b2005-234">Le traitement peut inclure la désentrelacement, la conversion de l’espace colorimétrique et le mixage de sous-flux.</span><span class="sxs-lookup"><span data-stu-id="b2005-234">Processing can include deinterlacing, color-space conversion, and substream mixing.</span></span> <span data-ttu-id="b2005-235">La sortie est écrite dans une surface de destination fournie par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b2005-235">The output is written to a destination surface provided by the caller.</span></span>

<span data-ttu-id="b2005-236">La méthode [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-236">The [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method takes the following parameters:</span></span>

-   <span data-ttu-id="b2005-237">*pRT* pointe vers une surface cible de rendu **IDirect3DSurface9** qui recevra la trame vidéo traitée.</span><span class="sxs-lookup"><span data-stu-id="b2005-237">*pRT* points to an **IDirect3DSurface9** render target surface that will receive the processed video frame.</span></span>
-   <span data-ttu-id="b2005-238">*pBltParams* pointe vers une structure [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) qui spécifie les paramètres de la blit.</span><span class="sxs-lookup"><span data-stu-id="b2005-238">*pBltParams* points to a [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure that specifies the parameters for the blit.</span></span>
-   <span data-ttu-id="b2005-239">*pSamples* est l’adresse d’un tableau de [**structures \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="b2005-239">*pSamples* is the address of an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="b2005-240">Ces structures contiennent les exemples d’entrée pour la blit.</span><span class="sxs-lookup"><span data-stu-id="b2005-240">These structures contain the input samples for the blit.</span></span>
-   <span data-ttu-id="b2005-241">*Échantillons* donne la taille du tableau *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="b2005-241">*NumSamples* gives the size of the *pSamples* array.</span></span>
-   <span data-ttu-id="b2005-242">Le paramètre *reserved* est réservé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="b2005-242">The *Reserved* parameter is reserved and should be set to **NULL**.</span></span>

<span data-ttu-id="b2005-243">Dans le tableau *pSamples* , l’appelant doit fournir les exemples d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-243">In the *pSamples* array, the caller must provide the following input samples:</span></span>

-   <span data-ttu-id="b2005-244">Image actuelle du flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-244">The current picture from the primary video stream.</span></span>
-   <span data-ttu-id="b2005-245">Les images de référence avant et arrière, si elles sont requises par l’algorithme de désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="b2005-245">Forward and backward reference pictures, if required by the deinterlacing algorithm.</span></span>
-   <span data-ttu-id="b2005-246">Zéro, une ou plusieurs images de sous-flux, jusqu’à un maximum de 15 sous-flux.</span><span class="sxs-lookup"><span data-stu-id="b2005-246">Zero or more substream pictures, up to a maximum of 15 substreams.</span></span>

<span data-ttu-id="b2005-247">Le pilote s’attend à ce que ce tableau soit dans un ordre particulier, comme décrit dans l' [exemple d’ordre d’entrée](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="b2005-247">The driver expects this array to be in a particular order, as described in [Input Sample Order](#input-sample-order).</span></span>

### <a name="blit-parameters"></a><span data-ttu-id="b2005-248">Paramètres blit</span><span class="sxs-lookup"><span data-stu-id="b2005-248">Blit Parameters</span></span>

<span data-ttu-id="b2005-249">La structure [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contient des paramètres généraux pour la blit.</span><span class="sxs-lookup"><span data-stu-id="b2005-249">The [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure contains general parameters for the blit.</span></span> <span data-ttu-id="b2005-250">Les paramètres les plus importants sont stockés dans les membres suivants de la structure :</span><span class="sxs-lookup"><span data-stu-id="b2005-250">The most important parameters are stored in the following members of the structure:</span></span>

-   <span data-ttu-id="b2005-251">**TargetFrame** est l’heure de présentation du frame de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2005-251">**TargetFrame** is the presentation time of the output frame.</span></span> <span data-ttu-id="b2005-252">Pour le contenu progressif, cette heure doit être égale à l’heure de début de l’image actuelle du flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-252">For progressive content, this time must equal the start time for the current frame from the primary video stream.</span></span> <span data-ttu-id="b2005-253">Cette heure est spécifiée dans le membre **Start** de la [**structure \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) pour cet exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b2005-253">This time is specified in the **Start** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure for that input sample.</span></span>

    <span data-ttu-id="b2005-254">Pour le contenu entrelacé, un frame avec deux champs entrelacés produit deux trames de sortie désentrelacées.</span><span class="sxs-lookup"><span data-stu-id="b2005-254">For interlaced content, a frame with two interleaved fields produces two deinterlaced output frames.</span></span> <span data-ttu-id="b2005-255">Sur le premier frame de sortie, l’heure de la présentation doit être égale à l’heure de début de l’image actuelle dans le flux vidéo principal, tout comme du contenu progressif.</span><span class="sxs-lookup"><span data-stu-id="b2005-255">On the first output frame, the presentation time must equal the start time of the current picture in the primary video stream, just like progressive content.</span></span> <span data-ttu-id="b2005-256">Sur le deuxième frame de sortie, l’heure de début doit être égale au point médian entre l’heure de début de l’image actuelle dans le flux vidéo principal et l’heure de début de l’image suivante dans le flux.</span><span class="sxs-lookup"><span data-stu-id="b2005-256">On the second output frame, the start time must equal the midpoint between the start time of the current picture in the primary video stream and the start time of the next picture in the stream.</span></span> <span data-ttu-id="b2005-257">Par exemple, si la vidéo d’entrée est de 25 images par seconde (50 champs par seconde), les trames de sortie auront les horodatages indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-257">For example, if the input video is 25 frames per second (50 fields per second), the output frames will have the time stamps shown in the following table.</span></span> <span data-ttu-id="b2005-258">Les horodatages sont affichés en unités de nanosecondes de 100.</span><span class="sxs-lookup"><span data-stu-id="b2005-258">Time stamps are shown in units of 100 nanoseconds.</span></span>

    

    | <span data-ttu-id="b2005-259">Image d’entrée</span><span class="sxs-lookup"><span data-stu-id="b2005-259">Input picture</span></span> | <span data-ttu-id="b2005-260">**TargetFrame** (1)</span><span class="sxs-lookup"><span data-stu-id="b2005-260">**TargetFrame** (1)</span></span> | <span data-ttu-id="b2005-261">**TargetFrame** (2)</span><span class="sxs-lookup"><span data-stu-id="b2005-261">**TargetFrame** (2)</span></span> |
    |---------------|---------------------|---------------------|
    | <span data-ttu-id="b2005-262">0</span><span class="sxs-lookup"><span data-stu-id="b2005-262">0</span></span>             | <span data-ttu-id="b2005-263">0</span><span class="sxs-lookup"><span data-stu-id="b2005-263">0</span></span>                   | <span data-ttu-id="b2005-264">200000</span><span class="sxs-lookup"><span data-stu-id="b2005-264">200000</span></span>              |
    | <span data-ttu-id="b2005-265">400000</span><span class="sxs-lookup"><span data-stu-id="b2005-265">400000</span></span>        | <span data-ttu-id="b2005-266">0</span><span class="sxs-lookup"><span data-stu-id="b2005-266">0</span></span>                   | <span data-ttu-id="b2005-267">600000</span><span class="sxs-lookup"><span data-stu-id="b2005-267">600000</span></span>              |
    | <span data-ttu-id="b2005-268">800000</span><span class="sxs-lookup"><span data-stu-id="b2005-268">800000</span></span>        | <span data-ttu-id="b2005-269">800000</span><span class="sxs-lookup"><span data-stu-id="b2005-269">800000</span></span>              | <span data-ttu-id="b2005-270">1000000</span><span class="sxs-lookup"><span data-stu-id="b2005-270">1000000</span></span>             |
    | <span data-ttu-id="b2005-271">1,2 million</span><span class="sxs-lookup"><span data-stu-id="b2005-271">1200000</span></span>       | <span data-ttu-id="b2005-272">1,2 million</span><span class="sxs-lookup"><span data-stu-id="b2005-272">1200000</span></span>             | <span data-ttu-id="b2005-273">1,4 million</span><span class="sxs-lookup"><span data-stu-id="b2005-273">1400000</span></span>             |

    

     

    <span data-ttu-id="b2005-274">Si le contenu entrelacé se compose de champs uniques plutôt que de champs entrelacés, les temps de sortie correspondent toujours aux temps d’entrée, comme avec le contenu progressif.</span><span class="sxs-lookup"><span data-stu-id="b2005-274">If interlaced content consists of single fields rather than interleaved fields, the output times always match the input times, as with progressive content.</span></span>

-   <span data-ttu-id="b2005-275">**TargetRect** définit une zone rectangulaire dans la surface de destination.</span><span class="sxs-lookup"><span data-stu-id="b2005-275">**TargetRect** defines a rectangular region within the destination surface.</span></span> <span data-ttu-id="b2005-276">La blit écrira la sortie dans cette région.</span><span class="sxs-lookup"><span data-stu-id="b2005-276">The blit will write the output to this region.</span></span> <span data-ttu-id="b2005-277">Plus précisément, chaque pixel dans **TargetRect** sera modifié, et aucun pixel en dehors de **TargetRect** ne sera modifié.</span><span class="sxs-lookup"><span data-stu-id="b2005-277">Specifically, every pixel inside **TargetRect** will be modified, and no pixels outside of **TargetRect** will be modified.</span></span> <span data-ttu-id="b2005-278">Le rectangle cible définit le rectangle englobant pour tous les flux vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b2005-278">The target rectangle defines the bounding rectangle for all of the input video streams.</span></span> <span data-ttu-id="b2005-279">Le positionnement des flux individuels dans ce rectangle est contrôlé par le paramètre *pSamples* de [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="b2005-279">Placement of individual streams within that rectangle is controlled through the *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span>
-   <span data-ttu-id="b2005-280">**BackgroundColor** donne la couleur de l’arrière-plan où aucune image vidéo ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b2005-280">**BackgroundColor** gives the color of the background wherever no video image appears.</span></span> <span data-ttu-id="b2005-281">Par exemple, lorsqu’une image vidéo 16 x 9 s’affiche dans une zone de 4 x 3 (cadre), les régions letterboxed sont affichées avec la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b2005-281">For example, when a 16 x 9 video image is displayed within a 4 x 3 area (letterboxing), the letterboxed regions are displayed with the background color.</span></span> <span data-ttu-id="b2005-282">La couleur d’arrière-plan ne s’applique qu’à l’intérieur du rectangle cible (**TargetRect**).</span><span class="sxs-lookup"><span data-stu-id="b2005-282">The background color applies only within the target rectangle (**TargetRect**).</span></span> <span data-ttu-id="b2005-283">Tous les pixels en dehors de **TargetRect** ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="b2005-283">Any pixels outside of **TargetRect** are not modified.</span></span>
-   <span data-ttu-id="b2005-284">**DestFormat** décrit l’espace colorimétrique de la vidéo de sortie (par exemple, si ITU-R BT. 709 ou BT. 601 Color est utilisé).</span><span class="sxs-lookup"><span data-stu-id="b2005-284">**DestFormat** describes the color space for the output video—for example, whether ITU-R BT.709 or BT.601 color is used.</span></span> <span data-ttu-id="b2005-285">Ces informations peuvent affecter la façon dont l’image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b2005-285">This information can affect how the image is displayed.</span></span> <span data-ttu-id="b2005-286">Pour plus d’informations, consultez [informations sur les couleurs étendues](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="b2005-286">For more information, see [Extended Color Information](extended-color-information.md).</span></span>

<span data-ttu-id="b2005-287">D’autres paramètres sont décrits dans la page de référence de la structure [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="b2005-287">Other parameters are described on the reference page for the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="input-samples"></a><span data-ttu-id="b2005-288">Exemples d’entrée</span><span class="sxs-lookup"><span data-stu-id="b2005-288">Input Samples</span></span>

<span data-ttu-id="b2005-289">Le paramètre *pSamples* de [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) pointe vers un tableau de [**structures \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="b2005-289">The *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) points to an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="b2005-290">Chacune de ces structures contient des informations sur un exemple d’entrée et un pointeur vers la surface Direct3D contenant l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b2005-290">Each of these structures contains information about one input sample and a pointer to the Direct3D surface that contains the sample.</span></span> <span data-ttu-id="b2005-291">Chaque échantillon est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-291">Each sample is one of the following:</span></span>

-   <span data-ttu-id="b2005-292">Image actuelle du flux principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-292">The current picture from the primary stream.</span></span>
-   <span data-ttu-id="b2005-293">Image de référence vers l’avant ou vers l’arrière à partir du flux principal, utilisée pour l’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="b2005-293">A forward or backward reference picture from the primary stream, used for deinterlacing.</span></span>
-   <span data-ttu-id="b2005-294">Image de sous-flux.</span><span class="sxs-lookup"><span data-stu-id="b2005-294">A substream picture.</span></span>

<span data-ttu-id="b2005-295">L’ordre exact dans lequel les exemples doivent apparaître dans le tableau est décrit plus loin dans la section [exemple d’ordre d’entrée](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="b2005-295">The exact order in which the samples must appear in the array is described later, in the section [Input Sample Order](#input-sample-order).</span></span>

<span data-ttu-id="b2005-296">Vous pouvez fournir jusqu’à 15 images sous-flux, même si la plupart des applications vidéo n’ont besoin que d’un seul sous-flux.</span><span class="sxs-lookup"><span data-stu-id="b2005-296">Up to 15 substream pictures can be provided, although most video applications need only one substream, at the most.</span></span> <span data-ttu-id="b2005-297">Le nombre de sous-flux peut changer à chaque appel à [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="b2005-297">The number of substreams can change with each call to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="b2005-298">Les images de sous-flux sont indiquées en affectant au membre **SampleFormat. SampleFormat** de la structure [**\_ VIDEOSAMPLE DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) la valeur DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="b2005-298">Substream pictures are indicated by setting the **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure equal to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="b2005-299">Pour le flux vidéo principal, ce membre décrit l’entrelacement de la vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b2005-299">For the primary video stream, this member describes the interlacing of the input video.</span></span> <span data-ttu-id="b2005-300">Pour plus d’informations, consultez [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) , énumération.</span><span class="sxs-lookup"><span data-stu-id="b2005-300">For more information, see [**DXVA2\_SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) enumeration.</span></span>

<span data-ttu-id="b2005-301">Pour le flux vidéo principal, les membres de **début** et de **fin** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fournissent les heures de début et de fin de l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b2005-301">For the primary video stream, the **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the start and end times of the input sample.</span></span> <span data-ttu-id="b2005-302">Pour les images sous-flux, définissez ces valeurs sur zéro, car l’heure de présentation est toujours calculée à partir du flux principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-302">For substream pictures, set these values to zero, because the presentation time is always calculated from the primary stream.</span></span> <span data-ttu-id="b2005-303">L’application est chargée de suivre le moment où chaque image de sous-flux doit être présentée et de la soumettre à [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) au moment opportun.</span><span class="sxs-lookup"><span data-stu-id="b2005-303">The application is responsible for tracking when each substream picture should be presented and submitting it to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) at the proper time.</span></span>

<span data-ttu-id="b2005-304">Deux rectangles définissent la façon dont la vidéo source est positionnée pour chaque flux :</span><span class="sxs-lookup"><span data-stu-id="b2005-304">Two rectangles define how the source video is positioned for each stream:</span></span>

-   <span data-ttu-id="b2005-305">Le membre **SrcRect** de la [**structure \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) spécifie le *rectangle source*, une zone rectangulaire de l’image source qui s’affichera dans le frame de sortie composite.</span><span class="sxs-lookup"><span data-stu-id="b2005-305">The **SrcRect** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure specifies the *source rectangle*, a rectangular region of the source picture that will appear in the composited output frame.</span></span> <span data-ttu-id="b2005-306">Pour rogner l’image, définissez cette valeur sur une valeur inférieure à la taille du cadre.</span><span class="sxs-lookup"><span data-stu-id="b2005-306">To crop the picture, set this to a value smaller than the frame size.</span></span> <span data-ttu-id="b2005-307">Sinon, affectez-lui une valeur égale à la taille du frame.</span><span class="sxs-lookup"><span data-stu-id="b2005-307">Otherwise, set it equal to the frame size.</span></span>
-   <span data-ttu-id="b2005-308">Le membre **au dstrect** de la même structure spécifie le *rectangle de destination*, une zone rectangulaire de la surface de destination dans laquelle le cadre vidéo apparaît.</span><span class="sxs-lookup"><span data-stu-id="b2005-308">The **DstRect** member of the same structure specifies the *destination rectangle*, a rectangular region of the destination surface where the video frame will appear.</span></span>

<span data-ttu-id="b2005-309">Le pilote BLITS les pixels du rectangle source dans le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="b2005-309">The driver blits pixels from the source rectangle into the destination rectangle.</span></span> <span data-ttu-id="b2005-310">Les deux rectangles peuvent avoir des tailles ou des proportions différentes ; le pilote met à l’échelle l’image en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="b2005-310">The two rectangles can have different sizes or aspect ratios; the driver will scale the image as needed.</span></span> <span data-ttu-id="b2005-311">En outre, chaque flux d’entrée peut utiliser un facteur d’échelle différent.</span><span class="sxs-lookup"><span data-stu-id="b2005-311">Moreover, each input stream can use a different scaling factor.</span></span> <span data-ttu-id="b2005-312">En fait, la mise à l’échelle peut être nécessaire pour produire les proportions correctes dans le frame de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2005-312">In fact, scaling might be necessary to produce the correct aspect ratio in the output frame.</span></span> <span data-ttu-id="b2005-313">Le pilote ne prend pas en compte le rapport hauteur des pixels de la source. par conséquent, si l’image source utilise des pixels non carrés, c’est à l’application de calculer le rectangle de destination approprié.</span><span class="sxs-lookup"><span data-stu-id="b2005-313">The driver does not take the source's pixel aspect ratio into account, so if the source image uses non-square pixels, it is up to the application to calculate the correct destination rectangle.</span></span>

<span data-ttu-id="b2005-314">Les formats de sous-flux préférés sont AYUV et AI44.</span><span class="sxs-lookup"><span data-stu-id="b2005-314">The preferred substream formats are AYUV and AI44.</span></span> <span data-ttu-id="b2005-315">Ce dernier est un format de palette de 16 couleurs.</span><span class="sxs-lookup"><span data-stu-id="b2005-315">The latter is a palletized format with 16 colors.</span></span> <span data-ttu-id="b2005-316">Les entrées de palette sont spécifiées dans le membre **PAL** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="b2005-316">Palette entries are specified in the **Pal** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span> <span data-ttu-id="b2005-317">(Si votre format vidéo source est initialement exprimé comme un type de média Media Foundation, les entrées de palette sont stockées dans l’attribut de la [**\_ \_ palette MF MT**](mf-mt-palette-attribute.md) .) Pour les formats qui ne sont pas des palettes, désactivez ce tableau à zéro.</span><span class="sxs-lookup"><span data-stu-id="b2005-317">(If your source video format is originally expressed as a Media Foundation media type, the palette entries are stored in the [**MF\_MT\_PALETTE**](mf-mt-palette-attribute.md) attribute.) For non-palletized formats, clear this array to zero.</span></span>

## <a name="image-composition"></a><span data-ttu-id="b2005-318">Composition de l’image</span><span class="sxs-lookup"><span data-stu-id="b2005-318">Image Composition</span></span>

<span data-ttu-id="b2005-319">Chaque opération blit est définie par les trois rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-319">Every blit operation is defined by the following three rectangles:</span></span>

-   <span data-ttu-id="b2005-320">Le rectangle *cible* (**TargetRect**) définit la région dans la surface de destination où la sortie apparaît.</span><span class="sxs-lookup"><span data-stu-id="b2005-320">The *target* rectangle (**TargetRect**) defines the region within the destination surface where the output will appear.</span></span> <span data-ttu-id="b2005-321">L’image de sortie est découpée sur ce rectangle.</span><span class="sxs-lookup"><span data-stu-id="b2005-321">The output image is clipped to this rectangle.</span></span>
-   <span data-ttu-id="b2005-322">Le rectangle de *destination* pour chaque flux (**au dstrect**) définit l’emplacement où le flux d’entrée apparaît dans l’image composite.</span><span class="sxs-lookup"><span data-stu-id="b2005-322">The *destination* rectangle for each stream (**DstRect**) defines where the input stream appears in the composited image.</span></span>
-   <span data-ttu-id="b2005-323">Le rectangle *source* pour chaque flux (**SrcRect**) définit la partie de l’image source qui apparaît.</span><span class="sxs-lookup"><span data-stu-id="b2005-323">The *source* rectangle for each stream (**SrcRect**) defines which part of the source image appears.</span></span>

<span data-ttu-id="b2005-324">Les rectangles cible et de destination sont spécifiés par rapport à la surface de destination.</span><span class="sxs-lookup"><span data-stu-id="b2005-324">The target and destination rectangles are specified relative to the destination surface.</span></span> <span data-ttu-id="b2005-325">Le rectangle source est spécifié par rapport à l’image source.</span><span class="sxs-lookup"><span data-stu-id="b2005-325">The source rectangle is specified relative to the source image.</span></span> <span data-ttu-id="b2005-326">Tous les rectangles sont spécifiés en pixels.</span><span class="sxs-lookup"><span data-stu-id="b2005-326">All rectangles are specified in pixels.</span></span>

![Diagramme montrant les rectangles source, de destination et cible](images/dxva-vp-rects.gif)

<span data-ttu-id="b2005-328">L’appareil de traitement vidéo alpha fusionne les images d’entrée, à l’aide de l’une des sources de données alpha suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2005-328">The video processing device alpha blends the input pictures, using any of the following sources of alpha data:</span></span>

-   <span data-ttu-id="b2005-329">Données alpha par pixel issues de sous-flux.</span><span class="sxs-lookup"><span data-stu-id="b2005-329">Per-pixel alpha data from substreams.</span></span>
-   <span data-ttu-id="b2005-330">Valeur alpha planaire pour chaque flux vidéo, spécifiée dans le membre **PlanarAlpha** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="b2005-330">A planar alpha value for each video stream, specified in the **PlanarAlpha** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span>
-   <span data-ttu-id="b2005-331">Valeur alpha planaire de l’image composite, spécifiée dans le membre **alpha** de la [**structure \_ VideoProcessBltParams DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="b2005-331">The planar alpha value of the composited image, specified in the **Alpha** member of the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span> <span data-ttu-id="b2005-332">Cette valeur est utilisée pour fusionner la totalité de l’image composite avec la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b2005-332">This value is used to blend the entire composited image with the background color.</span></span>

<span data-ttu-id="b2005-333">Cette section fournit une série d’exemples qui illustrent la façon dont le périphérique de traitement vidéo crée l’image de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2005-333">This section gives a series of examples that show how the video processing device creates the output image.</span></span>

### <a name="example-1-letterboxing"></a><span data-ttu-id="b2005-334">Exemple 1 : cadre</span><span class="sxs-lookup"><span data-stu-id="b2005-334">Example 1: Letterboxing</span></span>

<span data-ttu-id="b2005-335">Cet exemple montre comment mettre en bandes l’image source en définissant le rectangle de destination sur une valeur inférieure à celle du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="b2005-335">This example shows how to letterbox the source image, by setting the destination rectangle to be smaller than the target rectangle.</span></span> <span data-ttu-id="b2005-336">Le flux vidéo principal de cet exemple est une image 720 × 480 et est destiné à être affiché à un proportions de 16:9.</span><span class="sxs-lookup"><span data-stu-id="b2005-336">The primary video stream in this example is a 720 × 480 image, and is meant to be displayed at a 16:9 aspect ratio.</span></span> <span data-ttu-id="b2005-337">La surface de destination est 640 × 480 pixels (proportions 4:3).</span><span class="sxs-lookup"><span data-stu-id="b2005-337">The destination surface is 640 × 480 pixels (4:3 aspect ratio).</span></span> <span data-ttu-id="b2005-338">Pour obtenir les proportions correctes, le rectangle de destination doit être 640 × 360.</span><span class="sxs-lookup"><span data-stu-id="b2005-338">To achieve the correct aspect ratio, the destination rectangle must be 640 × 360.</span></span> <span data-ttu-id="b2005-339">Par souci de simplicité, cet exemple n’inclut pas de sous-flux.</span><span class="sxs-lookup"><span data-stu-id="b2005-339">For simplicity, this example does not include a substream.</span></span> <span data-ttu-id="b2005-340">Le diagramme suivant montre les rectangles source et de destination.</span><span class="sxs-lookup"><span data-stu-id="b2005-340">The following diagram shows the source and destination rectangles.</span></span>

![Diagramme montrant cadre.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

<span data-ttu-id="b2005-342">Le diagramme ci-dessus montre les rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-342">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="b2005-343">Rectangle cible : {0, 0, 640, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-343">Target rectangle: { 0, 0, 640, 480 }</span></span>
-   <span data-ttu-id="b2005-344">Vidéo principale :</span><span class="sxs-lookup"><span data-stu-id="b2005-344">Primary video:</span></span>

    -   <span data-ttu-id="b2005-345">Rectangle source : {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-345">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="b2005-346">Rectangle de destination : {0, 60, 640, 420}</span><span class="sxs-lookup"><span data-stu-id="b2005-346">Destination rectangle: { 0, 60, 640, 420 }</span></span>

<span data-ttu-id="b2005-347">Le pilote désentrelace la vidéo, réduit le frame désentrelacé à 640 × 360 et blit le frame dans le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="b2005-347">The driver will deinterlace the video, shrink the deinterlaced frame to 640 × 360, and blit the frame into the destination rectangle.</span></span> <span data-ttu-id="b2005-348">Le rectangle cible est plus grand que le rectangle de destination, de sorte que le pilote utilise la couleur d’arrière-plan pour remplir les barres horizontales au-dessus et en dessous du cadre.</span><span class="sxs-lookup"><span data-stu-id="b2005-348">The target rectangle is larger than the destination rectangle, so the driver will use the background color to fill the horizontal bars above and below the frame.</span></span> <span data-ttu-id="b2005-349">La couleur d’arrière-plan est spécifiée dans la structure [**\_ VideoProcessBltParams DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="b2005-349">The background color is specified in the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="example-2-stretching-substream-images"></a><span data-ttu-id="b2005-350">Exemple 2 : étirer des images de sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-350">Example 2: Stretching Substream Images</span></span>

<span data-ttu-id="b2005-351">Les images de sous-flux peuvent s’étendre au-delà de l’image vidéo principale.</span><span class="sxs-lookup"><span data-stu-id="b2005-351">Substream pictures can extend beyond the primary video picture.</span></span> <span data-ttu-id="b2005-352">Dans la vidéo DVD, par exemple, le flux vidéo principal peut avoir un proportions de 4:3, tandis que le sous-flux est 16:9.</span><span class="sxs-lookup"><span data-stu-id="b2005-352">In DVD video, for example, the primary video stream can have a 4:3 aspect ratio while the substream is 16:9.</span></span> <span data-ttu-id="b2005-353">Dans cet exemple, les deux flux vidéo ont les mêmes dimensions sources (720 × 480), mais le sous-flux est destiné à être affiché à un proportions de 16:9.</span><span class="sxs-lookup"><span data-stu-id="b2005-353">In this example, both video streams have the same source dimensions (720 × 480), but the substream is intended to be shown at a 16:9 aspect ratio.</span></span> <span data-ttu-id="b2005-354">Pour obtenir ces proportions, l’image de sous-flux est étirée horizontalement.</span><span class="sxs-lookup"><span data-stu-id="b2005-354">To achieve this aspect ratio, the substream image is stretched horizontally.</span></span> <span data-ttu-id="b2005-355">Les rectangles source et de destination sont présentés dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-355">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramme montrant l’étirement d’image sous-flux.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

<span data-ttu-id="b2005-357">Le diagramme ci-dessus montre les rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-357">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="b2005-358">Rectangle cible : {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-358">Target rectangle: { 0, 0, 854, 480 }</span></span>
-   <span data-ttu-id="b2005-359">Vidéo principale :</span><span class="sxs-lookup"><span data-stu-id="b2005-359">Primary video:</span></span>

    -   <span data-ttu-id="b2005-360">Rectangle source : {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-360">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="b2005-361">Rectangle de destination : {0, 107, 474, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-361">Destination rectangle: { 0, 107, 474, 480 }</span></span>

-   <span data-ttu-id="b2005-362">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-362">Substream:</span></span>
    -   <span data-ttu-id="b2005-363">Rectangle source : {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-363">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="b2005-364">Rectangle de destination : {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-364">Destination rectangle: { 0, 0, 854, 480 }</span></span>

<span data-ttu-id="b2005-365">Ces valeurs préservent la hauteur de l’image et ajustent les deux images horizontalement.</span><span class="sxs-lookup"><span data-stu-id="b2005-365">These values preserve the image height and scale both images horizontally.</span></span> <span data-ttu-id="b2005-366">Dans les régions où les deux images apparaissent, elles sont mélangées en alpha.</span><span class="sxs-lookup"><span data-stu-id="b2005-366">In the regions where both images appear, they are alpha blended.</span></span> <span data-ttu-id="b2005-367">Lorsque l’image de sous-flux se termine au-delà de la vidéo à l’origine, le sous-flux est fusionné alpha avec la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b2005-367">Where the substream picture exends beyond the primay video, the substream is alpha blended with the background color.</span></span> <span data-ttu-id="b2005-368">Cette couche alpha fusionne les couleurs modifiées dans le côté droit du diagramme.</span><span class="sxs-lookup"><span data-stu-id="b2005-368">This alpha blending accounts for the altered colors in the right-hand side of the diagram.</span></span>

### <a name="example-3-mismatched-stream-heights"></a><span data-ttu-id="b2005-369">Exemple 3 : hauteurs de flux incompatibles</span><span class="sxs-lookup"><span data-stu-id="b2005-369">Example 3: Mismatched Stream Heights</span></span>

<span data-ttu-id="b2005-370">Dans l’exemple précédent, le sous-flux et le flux principal sont de la même hauteur.</span><span class="sxs-lookup"><span data-stu-id="b2005-370">In the previous example, the substream and the primary stream are the same height.</span></span> <span data-ttu-id="b2005-371">Les flux peuvent également avoir des hauteurs incompatibles, comme illustré dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="b2005-371">Streams can also have mismatched heights, as shown in this example.</span></span> <span data-ttu-id="b2005-372">Les zones du rectangle cible où aucune vidéo ne s’affiche sont dessinées à l’aide de la couleur d’arrière-plan (noir dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="b2005-372">Areas within the target rectangle where no video appears are drawn using the background color—black in this example.</span></span> <span data-ttu-id="b2005-373">Les rectangles source et de destination sont présentés dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-373">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramme montrant des hauteurs de flux incompatibles,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

<span data-ttu-id="b2005-375">Le diagramme ci-dessus montre les rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-375">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="b2005-376">Rectangle cible : {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="b2005-376">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="b2005-377">Vidéo principale :</span><span class="sxs-lookup"><span data-stu-id="b2005-377">Primary video:</span></span>
    -   <span data-ttu-id="b2005-378">Rectangle source : {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="b2005-378">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="b2005-379">Rectangle de destination : {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="b2005-379">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="b2005-380">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-380">Substream:</span></span>
    -   <span data-ttu-id="b2005-381">Rectangle source : {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="b2005-381">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="b2005-382">Rectangle de destination : {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="b2005-382">Destination rectangle: { 25, 0, 125, 85 }</span></span>

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a><span data-ttu-id="b2005-383">Exemple 4 : rectangle cible plus petit que la surface de destination</span><span class="sxs-lookup"><span data-stu-id="b2005-383">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>

<span data-ttu-id="b2005-384">Cet exemple montre un cas où le rectangle cible est plus petit que la surface de destination.</span><span class="sxs-lookup"><span data-stu-id="b2005-384">This example shows a case where the target rectangle is smaller than the destination surface.</span></span>

![Diagramme montrant un blit dans un rectangle de destination.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

<span data-ttu-id="b2005-386">Le diagramme ci-dessus montre les rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-386">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="b2005-387">Surface de destination : {0, 0, 300, 200}</span><span class="sxs-lookup"><span data-stu-id="b2005-387">Destination surface: { 0, 0, 300, 200 }</span></span>
-   <span data-ttu-id="b2005-388">Rectangle cible : {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="b2005-388">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="b2005-389">Vidéo principale :</span><span class="sxs-lookup"><span data-stu-id="b2005-389">Primary video:</span></span>
    -   <span data-ttu-id="b2005-390">Rectangle source : {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="b2005-390">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="b2005-391">Rectangle de destination : {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="b2005-391">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="b2005-392">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-392">Substream:</span></span>
    -   <span data-ttu-id="b2005-393">Rectangle source : {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="b2005-393">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="b2005-394">Rectangle de destination : {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="b2005-394">Destination rectangle: { 25, 0, 125, 85 }</span></span>

<span data-ttu-id="b2005-395">Les pixels en dehors du rectangle cible ne sont pas modifiés, donc la couleur d’arrière-plan apparaît uniquement dans le rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="b2005-395">Pixels outside of the target rectangle are not modified, so the background color appears only within the target rectangle.</span></span> <span data-ttu-id="b2005-396">La zone en pointillés indique des parties de la surface de destination qui ne sont pas affectées par la blit.</span><span class="sxs-lookup"><span data-stu-id="b2005-396">The dotted area indicates portions of the destination surface that are not affected by the blit.</span></span>

### <a name="example-5-source-rectangles"></a><span data-ttu-id="b2005-397">Exemple 5 : rectangles sources</span><span class="sxs-lookup"><span data-stu-id="b2005-397">Example 5: Source Rectangles</span></span>

<span data-ttu-id="b2005-398">Si vous spécifiez un rectangle source plus petit que l’image source, le pilote blit uniquement cette partie de l’image.</span><span class="sxs-lookup"><span data-stu-id="b2005-398">If you specify a source rectangle that is smaller than the source picture, the driver will blit just that portion of the picture.</span></span> <span data-ttu-id="b2005-399">Dans cet exemple, les rectangles sources spécifient le quadrant inférieur droit du flux vidéo principal et le quadrant inférieur gauche du sous-flux (indiqué par les marques de hachage dans le diagramme).</span><span class="sxs-lookup"><span data-stu-id="b2005-399">In this example, the source rectangles specify the lower-right quadrant of the primary video stream and the lower-left quadrant of the substream (indicated by hash marks in the diagram).</span></span> <span data-ttu-id="b2005-400">Les rectangles de destination ont la même taille que les rectangles sources, donc la vidéo n’est pas étirée.</span><span class="sxs-lookup"><span data-stu-id="b2005-400">The destination rectangles are the same sizes as the source rectangles, so the video is not stretched.</span></span> <span data-ttu-id="b2005-401">Les rectangles source et de destination sont présentés dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-401">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramme montrant un blit de deux rectangles sources.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

<span data-ttu-id="b2005-403">Le diagramme ci-dessus montre les rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-403">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="b2005-404">Rectangle cible : {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="b2005-404">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="b2005-405">Vidéo principale :</span><span class="sxs-lookup"><span data-stu-id="b2005-405">Primary video:</span></span>
    -   <span data-ttu-id="b2005-406">Taille de la surface source : {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-406">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="b2005-407">Rectangle source : {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-407">Source rectangle: { 360, 240, 720, 480 }</span></span>
    -   <span data-ttu-id="b2005-408">Rectangle de destination : {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="b2005-408">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="b2005-409">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-409">Substream:</span></span>
    -   <span data-ttu-id="b2005-410">Taille de la surface source : {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="b2005-410">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="b2005-411">Rectangle source : {0, 288, 320, 576}</span><span class="sxs-lookup"><span data-stu-id="b2005-411">Source rectangle: { 0, 288, 320, 576 }</span></span>
    -   <span data-ttu-id="b2005-412">Rectangle de destination : {400, 0, 720, 288}</span><span class="sxs-lookup"><span data-stu-id="b2005-412">Destination rectangle: { 400, 0, 720, 288 }</span></span>

### <a name="example-6-intersecting-destination-rectangles"></a><span data-ttu-id="b2005-413">Exemple 6 : rectangles de destination d’intersection</span><span class="sxs-lookup"><span data-stu-id="b2005-413">Example 6: Intersecting Destination Rectangles</span></span>

<span data-ttu-id="b2005-414">Cet exemple est similaire à l’exemple précédent, mais les rectangles de destination se croisent.</span><span class="sxs-lookup"><span data-stu-id="b2005-414">This example is similar to previous one, but the destination rectangles intersect.</span></span> <span data-ttu-id="b2005-415">Les dimensions de surface sont les mêmes que dans l’exemple précédent, mais les rectangles source et de destination ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="b2005-415">The surface dimensions are the same as in the previous example, but the source and destination rectangles are not.</span></span> <span data-ttu-id="b2005-416">Là encore, la vidéo est rognée, mais pas étirée.</span><span class="sxs-lookup"><span data-stu-id="b2005-416">Again, the video is cropped but not stretched.</span></span> <span data-ttu-id="b2005-417">Les rectangles source et de destination sont présentés dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-417">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramme montrant l’intersection des rectangles de destination.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

<span data-ttu-id="b2005-419">Le diagramme ci-dessus montre les rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-419">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="b2005-420">Rectangle cible : {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="b2005-420">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="b2005-421">Vidéo principale :</span><span class="sxs-lookup"><span data-stu-id="b2005-421">Primary video:</span></span>
    -   <span data-ttu-id="b2005-422">Taille de la surface source : {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-422">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="b2005-423">Rectangle source : {260, 92, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-423">Source rectangle: { 260, 92, 720, 480 }</span></span>
    -   <span data-ttu-id="b2005-424">Rectangle de destination : {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="b2005-424">Destination rectangle: { 0, 0, 460, 388 }</span></span>
-   <span data-ttu-id="b2005-425">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-425">Substream:</span></span>
    -   <span data-ttu-id="b2005-426">Taille de la surface source : {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="b2005-426">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="b2005-427">Rectangle source : {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="b2005-427">Source rectangle: { 0, 0, 460, 388 }</span></span>
    -   <span data-ttu-id="b2005-428">Rectangle de destination : {260, 188, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="b2005-428">Destination rectangle: { 260, 188, 720, 576 }</span></span>

### <a name="example-7-stretching-and-cropping-video"></a><span data-ttu-id="b2005-429">Exemple 7 : vidéo sur l’étirement et le rognage</span><span class="sxs-lookup"><span data-stu-id="b2005-429">Example 7: Stretching and Cropping Video</span></span>

<span data-ttu-id="b2005-430">Dans cet exemple, la vidéo est étirée et rognée.</span><span class="sxs-lookup"><span data-stu-id="b2005-430">In this example, the video is stretched as well as cropped.</span></span> <span data-ttu-id="b2005-431">Une région 180 × 120 de chaque flux est étirée pour couvrir une zone 360 × 240 dans le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="b2005-431">A 180 × 120 region from each stream is stretched to cover a 360 × 240 area in the destination rectangle.</span></span>

![Diagramme montrant l’étirement et le rognage.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

<span data-ttu-id="b2005-433">Le diagramme ci-dessus montre les rectangles suivants :</span><span class="sxs-lookup"><span data-stu-id="b2005-433">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="b2005-434">Rectangle cible : {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-434">Target rectangle: { 0, 0, 720, 480 }</span></span>
-   <span data-ttu-id="b2005-435">Vidéo principale :</span><span class="sxs-lookup"><span data-stu-id="b2005-435">Primary video:</span></span>
    -   <span data-ttu-id="b2005-436">Taille de la surface source : {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="b2005-436">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="b2005-437">Rectangle source : {180, 120, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="b2005-437">Source rectangle: { 180, 120, 360, 240 }</span></span>
    -   <span data-ttu-id="b2005-438">Rectangle de destination : {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="b2005-438">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="b2005-439">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-439">Substream:</span></span>
    -   <span data-ttu-id="b2005-440">Taille de la surface source : {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="b2005-440">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="b2005-441">Rectangle source : {0, 0, 180, 120}</span><span class="sxs-lookup"><span data-stu-id="b2005-441">Source rectangle: { 0, 0, 180, 120 }</span></span>
    -   <span data-ttu-id="b2005-442">Rectangle de destination : {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="b2005-442">Destination rectangle: { 360, 240, 720, 480 }</span></span>

## <a name="input-sample-order"></a><span data-ttu-id="b2005-443">Ordre de l’exemple d’entrée</span><span class="sxs-lookup"><span data-stu-id="b2005-443">Input Sample Order</span></span>

<span data-ttu-id="b2005-444">Le paramètre *pSamples* de la méthode [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) est un pointeur vers un tableau d’exemples d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b2005-444">The *pSamples* parameter of the [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method is a pointer to an array of input samples.</span></span> <span data-ttu-id="b2005-445">Les exemples du flux vidéo principal apparaissent en premier, suivis d’images sous-flux dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="b2005-445">Samples from the primary video stream appear first, followed by substream pictures in Z-order.</span></span> <span data-ttu-id="b2005-446">Les exemples doivent être placés dans le tableau dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="b2005-446">Samples must be placed into the array in the following order:</span></span>

-   <span data-ttu-id="b2005-447">Les exemples du flux vidéo principal apparaissent en premier dans le tableau, dans l’ordre temporel.</span><span class="sxs-lookup"><span data-stu-id="b2005-447">Samples for the primary video stream appear first in the array, in temporal order.</span></span> <span data-ttu-id="b2005-448">Selon le mode de désentrelacement, le pilote peut nécessiter un ou plusieurs exemples de référence à partir du flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-448">Depending on the deinterlace mode, the driver may require one or more reference samples from the primary video stream.</span></span> <span data-ttu-id="b2005-449">Les membres **NumForwardRefSamples** et **NumBackwardRefSamples** de la [**structure \_ VideoProcessorCaps DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) spécifient le nombre d’exemples de référence ascendante et descendante nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b2005-449">The **NumForwardRefSamples** and **NumBackwardRefSamples** members of the [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure specify how many forward and backward reference samples are needed.</span></span> <span data-ttu-id="b2005-450">L’appelant doit fournir ces exemples de référence même si le contenu vidéo est progressif et ne nécessite pas de désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="b2005-450">The caller must provide these reference samples even if the video content is progressive and does not require deinterlacing.</span></span> <span data-ttu-id="b2005-451">(Cela peut se produire lorsque des trames progressifs sont attribuées à un appareil de désentrelacement, par exemple lorsque la source contient une combinaison de trames entrelacées et progressives.)</span><span class="sxs-lookup"><span data-stu-id="b2005-451">(This can occur when progressive frames are given to a deinterlacing device, for example when the source contains a mix of both interlaced and progressive frames.)</span></span>
-   <span data-ttu-id="b2005-452">Après les exemples du flux vidéo principal, le tableau peut contenir jusqu’à 15 exemples de sous-flux, organisés en ordre de plan, de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="b2005-452">After the samples for the primary video stream, the array can contain up to 15 substream samples, arranged in Z-order, from bottom to top.</span></span> <span data-ttu-id="b2005-453">Les sous-flux sont toujours progressifs et ne nécessitent pas d’images de référence.</span><span class="sxs-lookup"><span data-stu-id="b2005-453">Substreams are always progressive and do not require reference pictures.</span></span>

<span data-ttu-id="b2005-454">À tout moment, le flux vidéo principal peut basculer entre le contenu entrelacé et le contenu progressif, et le nombre de sous-flux peut changer.</span><span class="sxs-lookup"><span data-stu-id="b2005-454">At any time, the primary video stream can switch between interlaced and progressive content, and the number of substreams can change.</span></span>

<span data-ttu-id="b2005-455">Le membre **SampleFormat. SampleFormat** de la [**structure \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indique le type d’image.</span><span class="sxs-lookup"><span data-stu-id="b2005-455">The **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure indicates the type of picture.</span></span> <span data-ttu-id="b2005-456">Pour les images sous-flux, définissez cette valeur sur DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="b2005-456">For substream pictures, set this value to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="b2005-457">Pour les images progressives, la valeur est DXVA2 \_ SampleProgressiveFrame.</span><span class="sxs-lookup"><span data-stu-id="b2005-457">For progressive pictures, the value is DXVA2\_SampleProgressiveFrame.</span></span> <span data-ttu-id="b2005-458">Pour les images entrelacées, la valeur dépend de la disposition des champs.</span><span class="sxs-lookup"><span data-stu-id="b2005-458">For interlaced pictures, the value depends on the field layout.</span></span>

<span data-ttu-id="b2005-459">Si le pilote requiert des exemples de référence avant et arrière, le nombre complet d’exemples peut ne pas être disponible au début de la séquence vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2005-459">If the driver requires forward and backward reference samples, the full number of samples might not be available at the start of the video sequence.</span></span> <span data-ttu-id="b2005-460">Dans ce cas, incluez des entrées pour celles-ci dans le tableau *pSamples* , mais Marquez les exemples manquants comme ayant le type DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="b2005-460">In that case, include entries for them in the *pSamples* array, but mark the missing samples as having type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="b2005-461">Les membres de **début** et de **fin** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fournissent l’emplacement temporel de chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="b2005-461">The **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the temporal location of each sample.</span></span> <span data-ttu-id="b2005-462">Ces valeurs sont utilisées uniquement pour les exemples du flux vidéo principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-462">These values are used only for samples from the primary video stream.</span></span> <span data-ttu-id="b2005-463">Pour les images sous-flux, définissez les deux membres sur zéro.</span><span class="sxs-lookup"><span data-stu-id="b2005-463">For substream pictures, set both members to zero.</span></span>

<span data-ttu-id="b2005-464">Les exemples suivants peuvent vous aider à clarifier ces exigences.</span><span class="sxs-lookup"><span data-stu-id="b2005-464">The following examples may help to clarify these requirements.</span></span>

### <a name="example-1"></a><span data-ttu-id="b2005-465">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b2005-465">Example 1</span></span>

<span data-ttu-id="b2005-466">Le cas le plus simple se produit lorsqu’il n’y a aucun sous-flux et que l’algorithme de désentrelacement ne requiert pas d’exemples de référence (**NumForwardRefSamples** et **NumBackwardRefSamples** sont tous deux nuls).</span><span class="sxs-lookup"><span data-stu-id="b2005-466">The simplest case occurs when there are no substreams and the deinterlacing algorithm does not require reference samples (**NumForwardRefSamples** and **NumBackwardRefSamples** are both zero).</span></span> <span data-ttu-id="b2005-467">Bob désentrelacement est un exemple de ce type d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="b2005-467">Bob deinterlacing is an example of such an algorithm.</span></span> <span data-ttu-id="b2005-468">Dans ce cas, le tableau *pSamples* doit contenir une seule surface d’entrée, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-468">In this case, the *pSamples* array should contain a single input surface, as shown in the following table.</span></span>



| <span data-ttu-id="b2005-469">Index</span><span class="sxs-lookup"><span data-stu-id="b2005-469">Index</span></span>           | <span data-ttu-id="b2005-470">Type de surface</span><span class="sxs-lookup"><span data-stu-id="b2005-470">Surface type</span></span>        | <span data-ttu-id="b2005-471">Emplacement temporel</span><span class="sxs-lookup"><span data-stu-id="b2005-471">Temporal location</span></span> |
|-----------------|---------------------|-------------------|
| <span data-ttu-id="b2005-472">*pSamples* \[ entre\]</span><span class="sxs-lookup"><span data-stu-id="b2005-472">*pSamples*\[0\]</span></span> | <span data-ttu-id="b2005-473">Image entrelacée.</span><span class="sxs-lookup"><span data-stu-id="b2005-473">Interlaced picture.</span></span> | <span data-ttu-id="b2005-474">*T*</span><span class="sxs-lookup"><span data-stu-id="b2005-474">*T*</span></span>               |



 

<span data-ttu-id="b2005-475">La valeur d’heure *T* est supposée être l’heure de début de la trame vidéo actuelle.</span><span class="sxs-lookup"><span data-stu-id="b2005-475">The time value *T* is assumed to be the start time of the current video frame.</span></span>

### <a name="example-2"></a><span data-ttu-id="b2005-476">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b2005-476">Example 2</span></span>

<span data-ttu-id="b2005-477">Dans cet exemple, l’application mélange deux sous-flux avec le flux principal.</span><span class="sxs-lookup"><span data-stu-id="b2005-477">In this example, the application mixes two substreams with the primary stream.</span></span> <span data-ttu-id="b2005-478">L’algorithme de désentrelacement ne requiert pas d’exemples de référence.</span><span class="sxs-lookup"><span data-stu-id="b2005-478">The deinterlacing algorithm does not require reference samples.</span></span> <span data-ttu-id="b2005-479">Le tableau suivant montre comment ces exemples sont organisés dans le tableau *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="b2005-479">The following table shows how these samples are arranged in the *pSamples* array.</span></span>



| <span data-ttu-id="b2005-480">Index</span><span class="sxs-lookup"><span data-stu-id="b2005-480">Index</span></span>           | <span data-ttu-id="b2005-481">Type de surface</span><span class="sxs-lookup"><span data-stu-id="b2005-481">Surface type</span></span>       | <span data-ttu-id="b2005-482">Emplacement temporel</span><span class="sxs-lookup"><span data-stu-id="b2005-482">Temporal location</span></span> | <span data-ttu-id="b2005-483">Ordre de plan</span><span class="sxs-lookup"><span data-stu-id="b2005-483">Z-order</span></span> |
|-----------------|--------------------|-------------------|---------|
| <span data-ttu-id="b2005-484">*pSamples* \[ entre\]</span><span class="sxs-lookup"><span data-stu-id="b2005-484">*pSamples*\[0\]</span></span> | <span data-ttu-id="b2005-485">Image entrelacée</span><span class="sxs-lookup"><span data-stu-id="b2005-485">Interlaced picture</span></span> | <span data-ttu-id="b2005-486">*T*</span><span class="sxs-lookup"><span data-stu-id="b2005-486">*T*</span></span>               | <span data-ttu-id="b2005-487">0</span><span class="sxs-lookup"><span data-stu-id="b2005-487">0</span></span>       |
| <span data-ttu-id="b2005-488">*pSamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="b2005-488">*pSamples*\[1\]</span></span> | <span data-ttu-id="b2005-489">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-489">Substream</span></span>          | <span data-ttu-id="b2005-490">0</span><span class="sxs-lookup"><span data-stu-id="b2005-490">0</span></span>                 | <span data-ttu-id="b2005-491">1</span><span class="sxs-lookup"><span data-stu-id="b2005-491">1</span></span>       |
| <span data-ttu-id="b2005-492">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b2005-492">*pSamples*\[2\]</span></span> | <span data-ttu-id="b2005-493">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-493">Substream</span></span>          | <span data-ttu-id="b2005-494">0</span><span class="sxs-lookup"><span data-stu-id="b2005-494">0</span></span>                 | <span data-ttu-id="b2005-495">2</span><span class="sxs-lookup"><span data-stu-id="b2005-495">2</span></span>       |



 

### <a name="example-3"></a><span data-ttu-id="b2005-496">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="b2005-496">Example 3</span></span>

<span data-ttu-id="b2005-497">Supposons à présent que l’algorithme de désentrelacement nécessite un exemple de référence arrière et un exemple de référence avant.</span><span class="sxs-lookup"><span data-stu-id="b2005-497">Now suppose that the deinterlacing algorithm requires one backward reference sample and one forward reference sample.</span></span> <span data-ttu-id="b2005-498">En outre, deux images de sous-flux sont fournies, pour un total de cinq surfaces.</span><span class="sxs-lookup"><span data-stu-id="b2005-498">In addition, two substream pictures are provided, for a total of five surfaces.</span></span> <span data-ttu-id="b2005-499">Le classement correct est indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-499">The correct ordering is shown in the following table.</span></span>



| <span data-ttu-id="b2005-500">Index</span><span class="sxs-lookup"><span data-stu-id="b2005-500">Index</span></span>           | <span data-ttu-id="b2005-501">Type de surface</span><span class="sxs-lookup"><span data-stu-id="b2005-501">Surface type</span></span>                   | <span data-ttu-id="b2005-502">Emplacement temporel</span><span class="sxs-lookup"><span data-stu-id="b2005-502">Temporal location</span></span> | <span data-ttu-id="b2005-503">Ordre de plan</span><span class="sxs-lookup"><span data-stu-id="b2005-503">Z-order</span></span>        |
|-----------------|--------------------------------|-------------------|----------------|
| <span data-ttu-id="b2005-504">*pSamples* \[ entre\]</span><span class="sxs-lookup"><span data-stu-id="b2005-504">*pSamples*\[0\]</span></span> | <span data-ttu-id="b2005-505">Image entrelacée (référence)</span><span class="sxs-lookup"><span data-stu-id="b2005-505">Interlaced picture (reference)</span></span> | <span data-ttu-id="b2005-506">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="b2005-506">*T* −1</span></span>            | <span data-ttu-id="b2005-507">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b2005-507">Not applicable</span></span> |
| <span data-ttu-id="b2005-508">*pSamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="b2005-508">*pSamples*\[1\]</span></span> | <span data-ttu-id="b2005-509">Image entrelacée</span><span class="sxs-lookup"><span data-stu-id="b2005-509">Interlaced picture</span></span>             | <span data-ttu-id="b2005-510">*T*</span><span class="sxs-lookup"><span data-stu-id="b2005-510">*T*</span></span>               | <span data-ttu-id="b2005-511">0</span><span class="sxs-lookup"><span data-stu-id="b2005-511">0</span></span>              |
| <span data-ttu-id="b2005-512">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b2005-512">*pSamples*\[2\]</span></span> | <span data-ttu-id="b2005-513">Image entrelacée (référence)</span><span class="sxs-lookup"><span data-stu-id="b2005-513">Interlaced picture (reference)</span></span> | <span data-ttu-id="b2005-514">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="b2005-514">*T* +1</span></span>            | <span data-ttu-id="b2005-515">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b2005-515">Not applicable</span></span> |
| <span data-ttu-id="b2005-516">*pSamples* \[ 1,3\]</span><span class="sxs-lookup"><span data-stu-id="b2005-516">*pSamples*\[3\]</span></span> | <span data-ttu-id="b2005-517">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-517">Substream</span></span>                      | <span data-ttu-id="b2005-518">0</span><span class="sxs-lookup"><span data-stu-id="b2005-518">0</span></span>                 | <span data-ttu-id="b2005-519">1</span><span class="sxs-lookup"><span data-stu-id="b2005-519">1</span></span>              |
| <span data-ttu-id="b2005-520">*pSamples* \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="b2005-520">*pSamples*\[4\]</span></span> | <span data-ttu-id="b2005-521">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-521">Substream</span></span>                      | <span data-ttu-id="b2005-522">0</span><span class="sxs-lookup"><span data-stu-id="b2005-522">0</span></span>                 | <span data-ttu-id="b2005-523">2</span><span class="sxs-lookup"><span data-stu-id="b2005-523">2</span></span>              |



 

<span data-ttu-id="b2005-524">L’heure *t* − 1 est l’heure de début de l’image avant le frame actuel, et *t* + 1 est l’heure de début du cadre suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-524">The time *T* −1 is the start time of the frame before the current frame, and *T* +1 is the start time of the following frame.</span></span>

<span data-ttu-id="b2005-525">Si le flux vidéo bascule vers du contenu progressif, en utilisant le même mode de désentrelacement, l’application doit fournir le même nombre d’exemples, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b2005-525">If the video stream switches to progressive content, using the same deinterlacing mode, the application must provide the same number of samples, as shown in the following table.</span></span>



| <span data-ttu-id="b2005-526">Index</span><span class="sxs-lookup"><span data-stu-id="b2005-526">Index</span></span>           | <span data-ttu-id="b2005-527">Type de surface</span><span class="sxs-lookup"><span data-stu-id="b2005-527">Surface type</span></span>                    | <span data-ttu-id="b2005-528">Emplacement temporel</span><span class="sxs-lookup"><span data-stu-id="b2005-528">Temporal location</span></span> | <span data-ttu-id="b2005-529">Ordre de plan</span><span class="sxs-lookup"><span data-stu-id="b2005-529">Z-order</span></span>        |
|-----------------|---------------------------------|-------------------|----------------|
| <span data-ttu-id="b2005-530">*pSamples* \[ entre\]</span><span class="sxs-lookup"><span data-stu-id="b2005-530">*pSamples*\[0\]</span></span> | <span data-ttu-id="b2005-531">Image progressive (référence)</span><span class="sxs-lookup"><span data-stu-id="b2005-531">Progressive picture (reference)</span></span> | <span data-ttu-id="b2005-532">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="b2005-532">*T* −1</span></span>            | <span data-ttu-id="b2005-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b2005-533">Not applicable</span></span> |
| <span data-ttu-id="b2005-534">*pSamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="b2005-534">*pSamples*\[1\]</span></span> | <span data-ttu-id="b2005-535">Image progressive</span><span class="sxs-lookup"><span data-stu-id="b2005-535">Progressive picture</span></span>             | <span data-ttu-id="b2005-536">*T*</span><span class="sxs-lookup"><span data-stu-id="b2005-536">*T*</span></span>               | <span data-ttu-id="b2005-537">0</span><span class="sxs-lookup"><span data-stu-id="b2005-537">0</span></span>              |
| <span data-ttu-id="b2005-538">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b2005-538">*pSamples*\[2\]</span></span> | <span data-ttu-id="b2005-539">Image progressive (référence)</span><span class="sxs-lookup"><span data-stu-id="b2005-539">Progressive picture (reference)</span></span> | <span data-ttu-id="b2005-540">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="b2005-540">*T* +1</span></span>            | <span data-ttu-id="b2005-541">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b2005-541">Not applicable</span></span> |
| <span data-ttu-id="b2005-542">*pSamples* \[ 1,3\]</span><span class="sxs-lookup"><span data-stu-id="b2005-542">*pSamples*\[3\]</span></span> | <span data-ttu-id="b2005-543">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-543">Substream</span></span>                       | <span data-ttu-id="b2005-544">0</span><span class="sxs-lookup"><span data-stu-id="b2005-544">0</span></span>                 | <span data-ttu-id="b2005-545">1</span><span class="sxs-lookup"><span data-stu-id="b2005-545">1</span></span>              |
| <span data-ttu-id="b2005-546">*pSamples* \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="b2005-546">*pSamples*\[4\]</span></span> | <span data-ttu-id="b2005-547">Sous-flux</span><span class="sxs-lookup"><span data-stu-id="b2005-547">Substream</span></span>                       | <span data-ttu-id="b2005-548">0</span><span class="sxs-lookup"><span data-stu-id="b2005-548">0</span></span>                 | <span data-ttu-id="b2005-549">2</span><span class="sxs-lookup"><span data-stu-id="b2005-549">2</span></span>              |



 

### <a name="example-4"></a><span data-ttu-id="b2005-550">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="b2005-550">Example 4</span></span>

<span data-ttu-id="b2005-551">Au début d’une séquence vidéo, les exemples de référence ascendante et descendante peuvent ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="b2005-551">At the start of a video sequence, forward and backward reference samples might not be available.</span></span> <span data-ttu-id="b2005-552">Dans ce cas, les entrées des exemples manquants sont incluses dans le tableau *pSamples* , avec l’exemple de type DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="b2005-552">When this happens, entries for the missing samples are included in the *pSamples* array, with sample type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="b2005-553">En supposant que le mode de désentrelacement a besoin d’un exemple de référence ascendante et descendante, les trois premiers appels à [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) auront les séquences d’entrées affichées dans les trois tables suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2005-553">Assuming that the deinterlacing mode needs one forward and one backward reference sample, the first three calls to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) would have the sequences of inputs shown in the following three tables.</span></span>



| <span data-ttu-id="b2005-554">Index</span><span class="sxs-lookup"><span data-stu-id="b2005-554">Index</span></span>           | <span data-ttu-id="b2005-555">Type de surface</span><span class="sxs-lookup"><span data-stu-id="b2005-555">Surface type</span></span>                   | <span data-ttu-id="b2005-556">Emplacement temporel</span><span class="sxs-lookup"><span data-stu-id="b2005-556">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="b2005-557">*pSamples* \[ entre\]</span><span class="sxs-lookup"><span data-stu-id="b2005-557">*pSamples*\[0\]</span></span> | <span data-ttu-id="b2005-558">Unknown</span><span class="sxs-lookup"><span data-stu-id="b2005-558">Unknown</span></span>                        | <span data-ttu-id="b2005-559">0</span><span class="sxs-lookup"><span data-stu-id="b2005-559">0</span></span>                 |
| <span data-ttu-id="b2005-560">*pSamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="b2005-560">*pSamples*\[1\]</span></span> | <span data-ttu-id="b2005-561">Unknown</span><span class="sxs-lookup"><span data-stu-id="b2005-561">Unknown</span></span>                        | <span data-ttu-id="b2005-562">0</span><span class="sxs-lookup"><span data-stu-id="b2005-562">0</span></span>                 |
| <span data-ttu-id="b2005-563">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b2005-563">*pSamples*\[2\]</span></span> | <span data-ttu-id="b2005-564">Image entrelacée (référence)</span><span class="sxs-lookup"><span data-stu-id="b2005-564">Interlaced picture (reference)</span></span> | <span data-ttu-id="b2005-565">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="b2005-565">*T* +1</span></span>            |



 



| <span data-ttu-id="b2005-566">Index</span><span class="sxs-lookup"><span data-stu-id="b2005-566">Index</span></span>           | <span data-ttu-id="b2005-567">Type de surface</span><span class="sxs-lookup"><span data-stu-id="b2005-567">Surface type</span></span>                   | <span data-ttu-id="b2005-568">Emplacement temporel</span><span class="sxs-lookup"><span data-stu-id="b2005-568">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="b2005-569">*pSamples* \[ entre\]</span><span class="sxs-lookup"><span data-stu-id="b2005-569">*pSamples*\[0\]</span></span> | <span data-ttu-id="b2005-570">Unknown</span><span class="sxs-lookup"><span data-stu-id="b2005-570">Unknown</span></span>                        | <span data-ttu-id="b2005-571">0</span><span class="sxs-lookup"><span data-stu-id="b2005-571">0</span></span>                 |
| <span data-ttu-id="b2005-572">*pSamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="b2005-572">*pSamples*\[1\]</span></span> | <span data-ttu-id="b2005-573">Image entrelacée</span><span class="sxs-lookup"><span data-stu-id="b2005-573">Interlaced picture</span></span>             | <span data-ttu-id="b2005-574">*T*</span><span class="sxs-lookup"><span data-stu-id="b2005-574">*T*</span></span>               |
| <span data-ttu-id="b2005-575">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b2005-575">*pSamples*\[2\]</span></span> | <span data-ttu-id="b2005-576">Image entrelacée (référence)</span><span class="sxs-lookup"><span data-stu-id="b2005-576">Interlaced picture (reference)</span></span> | <span data-ttu-id="b2005-577">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="b2005-577">*T* +1</span></span>            |



 



| <span data-ttu-id="b2005-578">Index</span><span class="sxs-lookup"><span data-stu-id="b2005-578">Index</span></span>           | <span data-ttu-id="b2005-579">Type de surface</span><span class="sxs-lookup"><span data-stu-id="b2005-579">Surface type</span></span>                   | <span data-ttu-id="b2005-580">Emplacement temporel</span><span class="sxs-lookup"><span data-stu-id="b2005-580">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="b2005-581">*pSamples* \[ entre\]</span><span class="sxs-lookup"><span data-stu-id="b2005-581">*pSamples*\[0\]</span></span> | <span data-ttu-id="b2005-582">Image entrelacée</span><span class="sxs-lookup"><span data-stu-id="b2005-582">Interlaced picture</span></span>             | <span data-ttu-id="b2005-583">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="b2005-583">*T* −1</span></span>            |
| <span data-ttu-id="b2005-584">*pSamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="b2005-584">*pSamples*\[1\]</span></span> | <span data-ttu-id="b2005-585">Image entrelacée</span><span class="sxs-lookup"><span data-stu-id="b2005-585">Interlaced picture</span></span>             | <span data-ttu-id="b2005-586">*T*</span><span class="sxs-lookup"><span data-stu-id="b2005-586">*T*</span></span>               |
| <span data-ttu-id="b2005-587">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b2005-587">*pSamples*\[2\]</span></span> | <span data-ttu-id="b2005-588">Image entrelacée (référence)</span><span class="sxs-lookup"><span data-stu-id="b2005-588">Interlaced picture (reference)</span></span> | <span data-ttu-id="b2005-589">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="b2005-589">*T* +1</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="b2005-590">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2005-590">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2005-591">Accélération vidéo DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="b2005-591">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="b2005-592">\_Exemple DXVA2 VideoProc</span><span class="sxs-lookup"><span data-stu-id="b2005-592">DXVA2\_VideoProc Sample</span></span>](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
