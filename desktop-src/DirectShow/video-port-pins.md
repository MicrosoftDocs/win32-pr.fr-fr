---
description: Broches de port vidéo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Broches de port vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866434"
---
# <a name="video-port-pins"></a><span data-ttu-id="61ffa-103">Broches de port vidéo</span><span class="sxs-lookup"><span data-stu-id="61ffa-103">Video Port Pins</span></span>

<span data-ttu-id="61ffa-104">Un périphérique de capture avec un port vidéo matériel peut utiliser les extensions de port vidéo (VPE) dans Microsoft® DirectX®.</span><span class="sxs-lookup"><span data-stu-id="61ffa-104">A capture device with a hardware video port might use the video port extensions (VPE) in Microsoft® DirectX®.</span></span> <span data-ttu-id="61ffa-105">Si c’est le cas, le filtre de capture aura un code PIN de port vidéo (VP).</span><span class="sxs-lookup"><span data-stu-id="61ffa-105">If so, the capture filter will have a video port (VP) pin.</span></span> <span data-ttu-id="61ffa-106">Aucune donnée vidéo n’est acheminée du pin du VP via le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="61ffa-106">No video data travels from the VP pin through the filter graph.</span></span> <span data-ttu-id="61ffa-107">Au lieu de cela, les images vidéo sont produites dans le matériel et envoyées directement à la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="61ffa-107">Instead, video frames are produced in hardware and sent directly to video memory.</span></span> <span data-ttu-id="61ffa-108">Le pin du VP permet d’envoyer des messages de contrôle au matériel.</span><span class="sxs-lookup"><span data-stu-id="61ffa-108">The VP pin allows control messages to be sent to the hardware.</span></span>

<span data-ttu-id="61ffa-109">Il est important de connecter le code confidentiel du VP, même si votre application n’effectue que la capture de fichiers sans aperçu.</span><span class="sxs-lookup"><span data-stu-id="61ffa-109">It is important to connect the VP pin, even if your application only performs file capture with no preview.</span></span> <span data-ttu-id="61ffa-110">Si vous laissez le code confidentiel non connecté, le graphique ne s’exécutera pas correctement.</span><span class="sxs-lookup"><span data-stu-id="61ffa-110">If you leave the pin unconnected, the graph will not run correctly.</span></span> <span data-ttu-id="61ffa-111">Cela diffère des codes confidentiels d’aperçu, qui n’ont pas besoin d’être connectés.</span><span class="sxs-lookup"><span data-stu-id="61ffa-111">This is different from preview pins, which do not have to be connected.</span></span>

<span data-ttu-id="61ffa-112">Les différents convertisseurs vidéo DirectShow offrent une prise en charge différente des broches de vice-président :</span><span class="sxs-lookup"><span data-stu-id="61ffa-112">The different DirectShow video renderers provide varying support for VP pins:</span></span>

-   <span data-ttu-id="61ffa-113">Convertisseur vidéo : Connectez le code confidentiel du VP à la broche 0 sur le filtre de [mixage de superposition](overlay-mixer-filter.md) et connectez le filtre de mixage de recouvrement au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="61ffa-113">Video Renderer: Connect the VP pin to pin 0 on the [Overlay Mixer](overlay-mixer-filter.md) filter, and connect the Overlay Mixer filter to the Video Renderer.</span></span>
-   <span data-ttu-id="61ffa-114">VMR-7 : Connectez le code confidentiel du VP au filtre du [Gestionnaire de port vidéo](video-port-manager.md) et connectez le gestionnaire de port vidéo au VMR-7.</span><span class="sxs-lookup"><span data-stu-id="61ffa-114">VMR-7: Connect the VP pin to the [Video Port Manager](video-port-manager.md) filter, and connect the Video Port Manager to the VMR-7.</span></span>
-   <span data-ttu-id="61ffa-115">VMR-9 : vous ne pouvez pas utiliser VMR-9 si l’appareil a un code confidentiel de directeur, car Direct3D 9 ne prend pas en charge les ports vidéo.</span><span class="sxs-lookup"><span data-stu-id="61ffa-115">VMR-9: You cannot use the VMR-9 if the device has a VP pin, because Direct3D 9 does not support video ports.</span></span> <span data-ttu-id="61ffa-116">Utilisez le convertisseur vidéo ou VMR-7.</span><span class="sxs-lookup"><span data-stu-id="61ffa-116">Use either the Video Renderer or the VMR-7.</span></span>

<span data-ttu-id="61ffa-117">Pour les scénarios de port vidéo, le mélangeur de superposition et le convertisseur vidéo sont recommandés sur le gestionnaire de port vidéo et VMR-7, car tous les pilotes ne prennent pas en charge le gestionnaire de port vidéo.</span><span class="sxs-lookup"><span data-stu-id="61ffa-117">For video port scenarios, the Overlay Mixer and Video Renderer are recommended over the Video Port Manager and VMR-7, because not all drivers support the Video Port Manager.</span></span> <span data-ttu-id="61ffa-118">En général, le mélangeur de superposition est l’option la plus fiable pour les ports vidéo.</span><span class="sxs-lookup"><span data-stu-id="61ffa-118">In general, the Overlay Mixer is the most reliable option for video ports.</span></span>

<span data-ttu-id="61ffa-119">La méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insère automatiquement le mélangeur de superposition s’il y a un code confidentiel de VP.</span><span class="sxs-lookup"><span data-stu-id="61ffa-119">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Overlay Mixer if there is a VP pin.</span></span> <span data-ttu-id="61ffa-120">Si vous générez le graphique sans utiliser cette méthode, vous devez vérifier la présence d’une broche de port vidéo sur le filtre de capture et, le cas échéant, la connecter au filtre de mixage de superposition, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="61ffa-120">If you are building the graph without using this method, you should check for a video port pin on the capture filter, and if one is present, connect it to the Overlay Mixer filter, as shown in the following diagram.</span></span>

![connexion d’une broche de port vidéo au filtre de mixage de superposition.](images/vidcap11.png)

<span data-ttu-id="61ffa-122">Vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) pour rechercher un code confidentiel de VP sur le filtre de capture :</span><span class="sxs-lookup"><span data-stu-id="61ffa-122">You can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to search for a VP pin on the capture filter:</span></span>


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="61ffa-123">Une fois que vous avez ajouté le mélangeur de superposition au graphique, appelez à nouveau **FindPin** pour trouver la broche 0 sur le mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="61ffa-123">After you add the Overlay Mixer to the graph, call **FindPin** again to find pin 0 on the Overlay Mixer.</span></span> <span data-ttu-id="61ffa-124">La broche 0 est toujours la première broche d’entrée sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="61ffa-124">Pin 0 is always the first input pin on the filter.</span></span>


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



<span data-ttu-id="61ffa-125">Connectez les deux codes confidentiels en appelant [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span><span class="sxs-lookup"><span data-stu-id="61ffa-125">Connect the two pins by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span></span>


```C++
pGraph->Connect(pVPPin, pOvPin);
```



<span data-ttu-id="61ffa-126">Ensuite, connectez la broche de sortie du mixer de superposition au filtre de convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="61ffa-126">Then connect the Overlay Mixer's output pin to the Video Renderer filter.</span></span> <span data-ttu-id="61ffa-127">Vous pouvez masquer la vidéo en appelant les méthodes [**IVideoWindow ::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) et [**IVideoWindow ::p ut \_ visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="61ffa-127">You can hide the video by calling the [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) and [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span></span>

<span data-ttu-id="61ffa-128">Pour les tuners TV, le filtre de capture peut également avoir un code vidéo (PIN \_ catégorie \_ VIDEOPORT \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="61ffa-128">For TV tuners, the capture filter might also have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="61ffa-129">Si c’est le cas, connectez ce code PIN au filtre d' [allocateur de surface VBI](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="61ffa-129">If so, connect that pin to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="61ffa-130">Pour plus d’informations, consultez Affichage des sous- [titres](viewing-closed-captions.md).</span><span class="sxs-lookup"><span data-stu-id="61ffa-130">For more information, see [Viewing Closed Captions](viewing-closed-captions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61ffa-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61ffa-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61ffa-132">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="61ffa-132">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="61ffa-133">Utilisation du mélangeur de superposition dans la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="61ffa-133">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



