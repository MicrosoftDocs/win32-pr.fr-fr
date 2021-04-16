---
description: Mélange non carré
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Mélange non carré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522052"
---
# <a name="non-square-mixing"></a><span data-ttu-id="96f80-103">Mélange non carré</span><span class="sxs-lookup"><span data-stu-id="96f80-103">Non-Square Mixing</span></span>

<span data-ttu-id="96f80-104">Cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="96f80-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="96f80-105">Lorsque VMR-9 mélange deux flux ou plus, il y a deux points où la mise à l’échelle peut se produire : lorsque le mélange composite les flux d’entrée, et lorsque l’Allocator-Presenter effectue le rendu de l’image composite.</span><span class="sxs-lookup"><span data-stu-id="96f80-105">When the VMR-9 mixes two or more streams, there are two points where scaling can occur: When the mixer composites the input streams, and when the allocator-presenter renders the composited image.</span></span>

![opérations de mixage VMR](images/vmr-nonsquare-mixing.png)

<span data-ttu-id="96f80-107">Les versions précédentes de VMR-9 ont toujours composé les flux d’entrée à l’aide d’un ratio de pixels carré (1:1), même s’il n’y avait qu’un seul flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="96f80-107">Previous versions of the VMR-9 always composited the input streams using a square (1:1) pixel aspect ratio (PAR), even when there was only a single video stream.</span></span> <span data-ttu-id="96f80-108">Si le flux d’entrée comportait des pixels non carrés, cela provoquait une opération de mise à l’échelle inutile.</span><span class="sxs-lookup"><span data-stu-id="96f80-108">If the input stream had non-square pixels, this caused an unnecessary scaling operation.</span></span> <span data-ttu-id="96f80-109">La mise à l’échelle doit être évitée, bien sûr, car elle dégrade la qualité finale de l’image.</span><span class="sxs-lookup"><span data-stu-id="96f80-109">Scaling should be avoided as much as possible, of course, because it degrades the final image quality.</span></span>

<span data-ttu-id="96f80-110">À compter de Windows XP Service Pack 2, VMR-9 prend en charge deux méthodes différentes pour éviter le problème de la double mise à l’échelle :</span><span class="sxs-lookup"><span data-stu-id="96f80-110">Starting in Windows XP Service Pack 2, the VMR-9 supports two different ways to avoid the problem of double scaling:</span></span>

-   <span data-ttu-id="96f80-111">Implémentez un Allocator-Presenter personnalisé et prenez en charge l’interface [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .</span><span class="sxs-lookup"><span data-stu-id="96f80-111">Implement a custom allocator-presenter and support the [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) interface.</span></span>
-   <span data-ttu-id="96f80-112">Utilisez le mode de mélange non carré.</span><span class="sxs-lookup"><span data-stu-id="96f80-112">Use non-square mixing mode.</span></span>

<span data-ttu-id="96f80-113">Cette section décrit le mode de mélange non carré.</span><span class="sxs-lookup"><span data-stu-id="96f80-113">This section describes non-square mixing mode.</span></span> <span data-ttu-id="96f80-114">Les applications peuvent combiner les deux techniques.</span><span class="sxs-lookup"><span data-stu-id="96f80-114">Applications can combine both techniques.</span></span>

<span data-ttu-id="96f80-115">**Fonctionnement du mixage non carré**</span><span class="sxs-lookup"><span data-stu-id="96f80-115">**How Non-Square Mixing Works**</span></span>

<span data-ttu-id="96f80-116">En mode de mélange non carré, VMR-9 sélectionne un flux d’entrée comme taille cible et PAR défaut.</span><span class="sxs-lookup"><span data-stu-id="96f80-116">In non-square mixing mode, the VMR-9 selects one input stream to be the target size and PAR.</span></span> <span data-ttu-id="96f80-117">Le mélangeur VMR ne met pas à l’échelle la vidéo à partir de ce flux ou de tout autre flux avec la même taille et la même image.</span><span class="sxs-lookup"><span data-stu-id="96f80-117">The VMR's mixer does not scale the video from that stream or from any other streams with the same image size and PAR.</span></span> <span data-ttu-id="96f80-118">Les flux avec une taille ou un proportions différentes sont mis à l’échelle pour correspondre au PAR-dessus cible et à letterboxed pour correspondre à la taille finale de l’image de sortie.</span><span class="sxs-lookup"><span data-stu-id="96f80-118">Streams with a different size or aspect ratio are scaled to match the target PAR and letterboxed to fit the final output image size.</span></span>

<span data-ttu-id="96f80-119">Le choix des flux dépend du mode de mixage actuel :</span><span class="sxs-lookup"><span data-stu-id="96f80-119">The choice of streams depends on the current mixing mode:</span></span>

-   <span data-ttu-id="96f80-120">Le mode de mixage YUV est limité à un flux vidéo sur le pin 0.</span><span class="sxs-lookup"><span data-stu-id="96f80-120">YUV mixing mode is restricted to one video stream on pin 0.</span></span> <span data-ttu-id="96f80-121">(Les autres broches peuvent avoir une sous-image ou des flux de sous-titres.) Par conséquent, VMR-9 sélectionne toujours la broche 0 pour la taille et le pair de l’image cible.</span><span class="sxs-lookup"><span data-stu-id="96f80-121">(The other pins may have subpicture or closed caption streams.) Therefore, the VMR-9 always selects pin 0 for the target image size and PAR.</span></span>
-   <span data-ttu-id="96f80-122">En mode de mixage RVB, VMR sélectionne le flux avec la plus grande taille d’image.</span><span class="sxs-lookup"><span data-stu-id="96f80-122">In RGB mixing mode, the VMR selects the stream with the largest image size.</span></span> <span data-ttu-id="96f80-123">S’il en existe plusieurs, il sélectionne celui dont l’ordre de plan est le plus élevé. et s’il y a toujours un lien, il sélectionne le flux avec le code confidentiel le plus petit.</span><span class="sxs-lookup"><span data-stu-id="96f80-123">If there is more than one, it selects the one with the highest z-order; and if there is still a tie, it selects the stream with the lowest pin number.</span></span>

<span data-ttu-id="96f80-124">**Exemples d’opérations**</span><span class="sxs-lookup"><span data-stu-id="96f80-124">**Examples of Operation**</span></span>

<span data-ttu-id="96f80-125">**Exemple 1.**</span><span class="sxs-lookup"><span data-stu-id="96f80-125">**Example 1.**</span></span> <span data-ttu-id="96f80-126">Le flux 0 est 720 x 480 pixels avec un rapport hauteur/largeur d’image de 16:9.</span><span class="sxs-lookup"><span data-stu-id="96f80-126">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="96f80-127">Stream 1 est un 640 x 480 pixels avec un rapport hauteur/largeur d’image de 4:3.</span><span class="sxs-lookup"><span data-stu-id="96f80-127">Stream 1 is a 640 x 480 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="96f80-128">Dans cet exemple, le flux 0 a la plus grande taille d’image. par conséquent, VMR choisit ce flux, quel que soit le mode de mélange RVB ou le mode de mixage YUB.</span><span class="sxs-lookup"><span data-stu-id="96f80-128">In this example, stream 0 has the largest image size, so the VMR chooses this stream, regardless of RGB mixing mode or YUB mixing mode.</span></span> <span data-ttu-id="96f80-129">Le pair est de 32:27 (16:9/720:480), ce qui signifie que l’image doit être étirée horizontalement par ce rapport pour produire les proportions de l’image de 16:9 correctes.</span><span class="sxs-lookup"><span data-stu-id="96f80-129">The PAR is 32:27 (16:9 / 720:480), meaning the image must be stretched horizontally by this ratio to produce the correct 16:9 picture aspect ratio.</span></span>

<span data-ttu-id="96f80-130">Pour correspondre au pair cible, le mélangeur VMR met à l’échelle le flux 1 en fonction du ratio inverse (27:32), ce qui génère une image 540 x 480.</span><span class="sxs-lookup"><span data-stu-id="96f80-130">To match the target PAR, the VMR mixer scales stream 1 by the inverse ratio (27:32), resulting in a 540 x 480 image.</span></span> <span data-ttu-id="96f80-131">Les deux flux sont ensuite composés sur une surface.</span><span class="sxs-lookup"><span data-stu-id="96f80-131">The two streams are then composited onto one surface.</span></span> <span data-ttu-id="96f80-132">Pour afficher correctement l’image résultante, le présentateur de l’allocateur doit étirer l’image horizontalement pour correspondre aux proportions de l’image 16:9.</span><span class="sxs-lookup"><span data-stu-id="96f80-132">To display the resulting image correctly, the allocator presenter must stretch the image horizontally to fit the 16:9 picture aspect ratio.</span></span>

![exemple 1 :](images/vmr-nonsquare-mixing2.png)

<span data-ttu-id="96f80-134">**Exemple 2.**</span><span class="sxs-lookup"><span data-stu-id="96f80-134">**Example 2.**</span></span> <span data-ttu-id="96f80-135">Le flux 0 est 720 x 480 pixels avec un rapport hauteur/largeur d’image de 16:9.</span><span class="sxs-lookup"><span data-stu-id="96f80-135">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="96f80-136">Stream 1 est un 1024 x 768 pixels avec un rapport hauteur/largeur d’image de 4:3.</span><span class="sxs-lookup"><span data-stu-id="96f80-136">Stream 1 is a 1024 x 768 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="96f80-137">Si VMR-9 utilise le mode de mixage YUV, il sélectionne toujours Stream 0.</span><span class="sxs-lookup"><span data-stu-id="96f80-137">If the VMR-9 is using YUV mixing mode, it always selects stream 0.</span></span> <span data-ttu-id="96f80-138">Par conséquent, il étire le flux 1 sur 540 x 480 pixels, pour qu’il corresponde au pair du flux 0.</span><span class="sxs-lookup"><span data-stu-id="96f80-138">Therefore, it stretches stream 1 to 540 x 480 pixels, to match the PAR of stream 0.</span></span>

<span data-ttu-id="96f80-139">Si VMR-9 utilise le mode de mixage RGB, il sélectionne Stream 1 comme cible, car ce flux a la plus grande taille d’image.</span><span class="sxs-lookup"><span data-stu-id="96f80-139">If the VMR-9 is using RGB mixing mode, it selects stream 1 as the target, because that stream has the largest image size.</span></span> <span data-ttu-id="96f80-140">Il étend le flux 0 à une taille d’image de 1024 x 576 pixels.</span><span class="sxs-lookup"><span data-stu-id="96f80-140">It stretches stream 0 to an image size of 1024 x 576 pixels.</span></span> <span data-ttu-id="96f80-141">Notez que dans ce cas, l’image composite a un-à-un de 1:1, par conséquent, l’Allocator-Presenter ne doit pas corriger les pixels non carrés.</span><span class="sxs-lookup"><span data-stu-id="96f80-141">Note that in this case, the composited image has a PAR of 1:1, so the allocator-presenter does not have to correct for non-square pixels.</span></span> <span data-ttu-id="96f80-142">(Il se peut que vous deviez toujours étirer la vidéo pour tenir compte du rectangle de destination.)</span><span class="sxs-lookup"><span data-stu-id="96f80-142">(It might still need to stretch the video to account for the destination rectangle.)</span></span>

<span data-ttu-id="96f80-143">**Utilisation du mode de mélange non carré**</span><span class="sxs-lookup"><span data-stu-id="96f80-143">**Using Non-Square Mixing Mode**</span></span>

<span data-ttu-id="96f80-144">Le mode de mélange non carré est recommandé si l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="96f80-144">Non-square mixing mode is recommended if either of the following conditions are true:</span></span>

-   <span data-ttu-id="96f80-145">Votre application n’envoie jamais plus d’un flux vidéo à VMR-9.</span><span class="sxs-lookup"><span data-stu-id="96f80-145">Your application never sends more than one video stream to the VMR-9.</span></span>
-   <span data-ttu-id="96f80-146">Votre application restitue des fichiers de DVD, de télévision ou MS-DVR.</span><span class="sxs-lookup"><span data-stu-id="96f80-146">Your application renders DVD, television, or ms-dvr files.</span></span> <span data-ttu-id="96f80-147">Vous devez également utiliser le mode de mixage YUV dans ce cas, si le matériel graphique le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="96f80-147">You should also use YUV mixing mode in this case, if the graphics hardware supports it.</span></span>

<span data-ttu-id="96f80-148">Si votre application mélange plusieurs flux vidéo qui peuvent avoir des tailles d’image ou des proportions de pixels variables, le mode de mélange de carrés par défaut est recommandé.</span><span class="sxs-lookup"><span data-stu-id="96f80-148">If your application mixes multiple video streams that may have varying image sizes or pixel aspect ratios, the default square mixing mode is recommended.</span></span>

<span data-ttu-id="96f80-149">Pour configurer le mode de mixage non carré, le graphique de filtre doit être arrêté et toutes les broches d’entrée déconnectées sur VMR-9.</span><span class="sxs-lookup"><span data-stu-id="96f80-149">To configure non-square mixing mode, the filter graph must be stopped and all input pins disconnected on the VMR-9.</span></span> <span data-ttu-id="96f80-150">Appelez ensuite [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) avec l' \_ indicateur MixerPref9 NonSquareMixing :</span><span class="sxs-lookup"><span data-stu-id="96f80-150">Then call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_NonSquareMixing flag:</span></span>


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> <span data-ttu-id="96f80-151">Si vous combinez l' \_ indicateur MixerPref9 NonSquareMixing avec l' \_ indicateur MixerPref9 ARADJUSTXORY, VMR-9 ignore l' \_ indicateur MixerPref9 ARAdjustXorY.</span><span class="sxs-lookup"><span data-stu-id="96f80-151">If you combine the MixerPref9\_NonSquareMixing flag with the MixerPref9\_ARAdjustXorY flag, the VMR-9 ignores the MixerPref9\_ARAdjustXorY flag.</span></span>

 

<span data-ttu-id="96f80-152">Si votre application utilise un allocateur-présentateur personnalisé avec le mode de mélange non carré, sachez que l’image composite peut avoir un PAR-défaut non carré.</span><span class="sxs-lookup"><span data-stu-id="96f80-152">If your application uses a custom allocator-presenter with non-square mixing mode, be aware that the composited image may have a non-square PAR.</span></span> <span data-ttu-id="96f80-153">L’Allocator-Presenter doit mettre l’image à l’échelle d’un carré (1:1) PAR.</span><span class="sxs-lookup"><span data-stu-id="96f80-153">The allocator-presenter must scale the image to a square (1:1) PAR.</span></span>

<span data-ttu-id="96f80-154">**Images bitmap statiques**</span><span class="sxs-lookup"><span data-stu-id="96f80-154">**Static Bitmaps**</span></span>

<span data-ttu-id="96f80-155">Si vous utilisez l’interface [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) pour fusionner une image bitmap statique sur la vidéo, vous devez considérer que l’image bitmap est un second flux vidéo pour les besoins du mode de mixage VMR.</span><span class="sxs-lookup"><span data-stu-id="96f80-155">If you use the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend a static bitmap onto the video, you should consider the bitmap to be a second video stream for purposes of the VMR mixing mode.</span></span>

<span data-ttu-id="96f80-156">VMR traite la bitmap comme ayant le même titre que la cible.</span><span class="sxs-lookup"><span data-stu-id="96f80-156">The VMR treats the bitmap as having the same PAR as the target.</span></span> <span data-ttu-id="96f80-157">Elle n’ajuste pas l’image bitmap pour qu’elle s’ajuste aux proportions de pixels de la cible.</span><span class="sxs-lookup"><span data-stu-id="96f80-157">It does not scale the bitmap to adjust for the target's pixel aspect ratio.</span></span> <span data-ttu-id="96f80-158">Dans la configuration par défaut de VMR, la cible a une valeur de 1:1 PAR, qui correspond à la plupart des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="96f80-158">In the VMR's default configuration, the target has a 1:1 PAR, which matches most bitmaps.</span></span> <span data-ttu-id="96f80-159">En mode de mélange non carré, la cible peut avoir des pixels non carrés.</span><span class="sxs-lookup"><span data-stu-id="96f80-159">In non-square mixing mode, the target might have non-square pixels.</span></span> <span data-ttu-id="96f80-160">Pour vous assurer que la bitmap est correctement affichée, l’application doit fournir une image dont le PAR correspond au pair cible.</span><span class="sxs-lookup"><span data-stu-id="96f80-160">To ensure that the bitmap is displayed correctly, the application should supply an image whose PAR matches the target PAR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96f80-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96f80-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96f80-162">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="96f80-162">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



