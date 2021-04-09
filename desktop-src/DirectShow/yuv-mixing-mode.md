---
description: Mode de mixage YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Mode de mixage YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867485"
---
# <a name="yuv-mixing-mode"></a><span data-ttu-id="d2aa8-103">Mode de mixage YUV</span><span class="sxs-lookup"><span data-stu-id="d2aa8-103">YUV Mixing Mode</span></span>

<span data-ttu-id="d2aa8-104">Cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="d2aa8-105">À compter de Windows XP Service Pack 2, VMR prend en charge un mode de mixage appelé mode de mixage YUV.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-105">Starting in Windows XP Service Pack 2, the VMR supports a mixing mode called YUV mixing mode.</span></span> <span data-ttu-id="d2aa8-106">Ce mode est particulièrement utile pour les applications TV ou DVD avancées.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-106">This mode is most useful for advanced TV or DVD applications.</span></span> <span data-ttu-id="d2aa8-107">Il intègre une partie de la puissance de VMR mixer pour améliorer les performances sur le matériel graphique de bas niveau qui utilise une conception d’architecture de mémoire unifiée.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-107">It trades some of the power of the VMR mixer for better performance on low end graphics hardware that uses a unified memory architecture design.</span></span> <span data-ttu-id="d2aa8-108">Le mode de mixage YUV est pris en charge sur VMR-7 et VMR-9.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-108">YUV mixing mode is supported on both the VMR-7 and VMR-9.</span></span>

<span data-ttu-id="d2aa8-109">**Avantages**</span><span class="sxs-lookup"><span data-stu-id="d2aa8-109">**Advantages**</span></span>

<span data-ttu-id="d2aa8-110">Le mode de mixage YUV présente plusieurs avantages en ce qui concerne le rendu des performances par rapport au mode de mixage RVB d’origine pris en charge par VMR :</span><span class="sxs-lookup"><span data-stu-id="d2aa8-110">YUV mixing mode has several advantages relating to rendering performance over the original RGB mixing mode supported by the VMR:</span></span>

-   <span data-ttu-id="d2aa8-111">Lorsque VMR est en mode de mixage YUV, toutes les opérations de composition de flux vidéo et de désentrelacement sont effectuées dans l’espace colorimétrique YUV.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-111">When the VMR is in YUV mixing mode, all de-interlacing and video stream composition operations are performed in YUV color space.</span></span> <span data-ttu-id="d2aa8-112">Les surfaces YUV requièrent généralement entre 50% et 60% de bande passante de mémoire que les surfaces RVB équivalentes.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-112">YUV surfaces typically require from 50% to 60% less memory bandwidth than equivalent RGB surfaces.</span></span>
-   <span data-ttu-id="d2aa8-113">La composition de désentrelacement et de flux est effectuée par un appel unique au pilote Graphics.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-113">The deinterlacing and stream composition are performed by a single call to the graphics driver.</span></span> <span data-ttu-id="d2aa8-114">Le pilote peut utiliser les fonctionnalités de multi-texturisation du matériel graphique, ce qui permet d’économiser davantage de bande passante en mémoire.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-114">The driver can use the graphics hardware's multi-texturing capabilities, resulting in additional memory bandwidth savings.</span></span>

<span data-ttu-id="d2aa8-115">Même si une application vidéo peut utiliser le mode de mélange YUV, elle est principalement destinée à deux types d’applications de lecture vidéo :</span><span class="sxs-lookup"><span data-stu-id="d2aa8-115">Although any video application can use YUV mixing mode, it is primarily intended for two types of video playback application:</span></span>

1.  <span data-ttu-id="d2aa8-116">Applications TV qui affichent des sous-titres ou du télétexte.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-116">TV applications that display closed captions or teletext.</span></span>
2.  <span data-ttu-id="d2aa8-117">Les applications DVD affichent des données de sous-image de DVD ou des sous-titres.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-117">DVD applications display DVD subpicture data or closed captions.</span></span>

<span data-ttu-id="d2aa8-118">**Restrictions**</span><span class="sxs-lookup"><span data-stu-id="d2aa8-118">**Restrictions**</span></span>

<span data-ttu-id="d2aa8-119">Un certain nombre de restrictions sont appliquées par le VMR lorsqu’il est placé en mode de mixage YUV :</span><span class="sxs-lookup"><span data-stu-id="d2aa8-119">A number of restrictions are enforced by the VMR when it is put into YUV mixing mode:</span></span>

-   <span data-ttu-id="d2aa8-120">Le flux 0 (le flux connecté à la broche d’entrée 0) peut être progressif ou entrelacé ; tous les autres flux doivent être progressifs.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-120">Stream 0 (the stream connected to Input Pin 0) can be progressive or interlaced; all other streams must be progressive.</span></span>
-   <span data-ttu-id="d2aa8-121">Le GUID \_ null (mode tissage) n’est pas autorisé pour le flux 0.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-121">GUID\_NULL (weave mode) is not allowed for stream 0.</span></span>
-   <span data-ttu-id="d2aa8-122">DeinterlacePref \_ tissage ne peut pas être utilisé comme mode de secours, car cela peut empêcher la création d’un appareil de désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-122">DeinterlacePref\_Weave cannot be used as a fallback mode because this could prevent a de-interlace device from being created.</span></span> <span data-ttu-id="d2aa8-123">Le mode de mixage YUV requiert un appareil de désentrelacement, même si la vidéo entrante n’est pas entrelacée.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-123">YUV mixing mode requires a deinterlace device even if the incoming video is not interlaced.</span></span>
-   <span data-ttu-id="d2aa8-124">Aucune modification ne peut être apportée à la valeur alpha planaire associée à chaque flux d’entrée VMR.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-124">No changes can be made to the planar alpha value associated with each VMR input stream.</span></span>
-   <span data-ttu-id="d2aa8-125">L’utilisateur ne peut pas modifier l’ordre de plan des flux vidéo connectés.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-125">The user cannot alter the Z-order of the connected video streams.</span></span> <span data-ttu-id="d2aa8-126">L’ordre de plan par défaut est issu de l’ordre du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-126">The default Z-order is taken from the pin order.</span></span>
-   <span data-ttu-id="d2aa8-127">Le masquage des couleurs n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-127">Color keying is not supported.</span></span>
-   <span data-ttu-id="d2aa8-128">La broche d’entrée 0 doit recevoir le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-128">Input pin 0 must receive the video stream.</span></span>
-   <span data-ttu-id="d2aa8-129">Les autres broches d’entrée peuvent uniquement recevoir des données de sous-flux vidéo, telles que des sous-images de DVD, des sous-titres ou du télétexte.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-129">The other inputs pins can only receive video sub-stream data such as DVD sub-picture, closed captions or teletext.</span></span>
-   <span data-ttu-id="d2aa8-130">Les autres broches d’entrée peuvent uniquement accepter des formats YUV alpha par pixel, tels que AYUV, AI44 et IA44.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-130">The other inputs pins can only accept per-pixel alpha YUV formats, such as AYUV, AI44 and IA44.</span></span>
-   <span data-ttu-id="d2aa8-131">Aucune des broches d’entrée de VMR ne peut accepter des formats RVB.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-131">None of the VMR's input pins can accept any RGB formats.</span></span>
-   <span data-ttu-id="d2aa8-132">Les images bitmap fournies par l’application ne peuvent plus être combinées avec la vidéo avant la présentation à l’écran.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-132">Application supplied bitmap images can no longer be combined with the video prior to presentation to the display.</span></span>
-   <span data-ttu-id="d2aa8-133">Les sous-flux individuels ne peuvent pas être inversés horizontalement ou verticalement à l’aide des fonctions « rectangle de sortie » du mélangeur VMR.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-133">Individual sub-streams cannot be inverted horizontally or vertically using the VMR's mixer "output rectangle" functions.</span></span> <span data-ttu-id="d2aa8-134">Le repositionnement et le redimensionnement du flux « normal » sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-134">"Normal" stream re-positioning and re-sizing is supported.</span></span>
-   <span data-ttu-id="d2aa8-135">La couleur d’arrière-plan de mixage (spécifiée par [**IVMRMixerControl :: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) est toujours spécifiée dans l’espace de couleurs RVB, tout comme en mode de mélange RVB.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-135">The mixing background color (specified by [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) is still specified in the RGB color space, just as in RGB mixing mode.</span></span>

<span data-ttu-id="d2aa8-136">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="d2aa8-136">**Configuration**</span></span>

<span data-ttu-id="d2aa8-137">Les applications doivent configurer explicitement VMR pour tirer parti du mode de mélange YUV ; le mode de mixage RVB d’origine reste le mode de mixage par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-137">Applications must explicitly configure the VMR to take advantage of YUV mixing mode; the original RGB mixing mode remains the default mixing mode.</span></span> <span data-ttu-id="d2aa8-138">Pour activer le mode de mixage YUV dans VMR-7, appelez [**IVMRMixerControl :: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) avec l' \_ indicateur RenderTargetYUV MixerPref.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-138">To enable YUV mixing mode in the VMR-7, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_RenderTargetYUV flag.</span></span> <span data-ttu-id="d2aa8-139">Cet appel doit être effectué avant que l’une des broches d’entrée de VMR soit connectée.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-139">This call must be made before any of the VMR's input pins are connected.</span></span> <span data-ttu-id="d2aa8-140">Pour activer le mode de mixage YUV dans VMR-9, appelez [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) avec l' \_ indicateur RenderTargetYUV MixerPref9.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-140">To enable YUV mixing mode in the VMR-9, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_RenderTargetYUV flag.</span></span>

<span data-ttu-id="d2aa8-141">La seule façon de déterminer si VMR-7 prend en charge le nouveau mode de mixage YUV consiste à essayer de définir le VMR dans ce mode.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-141">The only way to determine if the VMR-7 supports the new YUV mixing mode is to try setting the VMR into that mode.</span></span> <span data-ttu-id="d2aa8-142">Si l’appel est effectué, vous pouvez toujours remettre VMR en mode de mixage RVB si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-142">If the call succeeds, you can still put the VMR back into RGB mixing mode if necessary.</span></span> <span data-ttu-id="d2aa8-143">Une fois qu’elle est définie en mode de mixage YUV, le VMR peut uniquement être rétabli en mode mixte RVB après que toutes les broches d’entrée ont été déconnectées.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-143">After it is set into YUV mixing mode, the VMR can only be changed back to RGB mixing mode after all input pins have been disconnected.</span></span>

<span data-ttu-id="d2aa8-144">En mode mélange YUV, vous pouvez réduire la charge sur l’unité de traitement graphique (GPU) en appliquant les indicateurs suivants dans la méthode **SetMixingPrefs** :</span><span class="sxs-lookup"><span data-stu-id="d2aa8-144">In YUV mixing mode, you can reduce the load on the graphics processing unit (GPU) by applying the following flags in the **SetMixingPrefs** method:</span></span>



| <span data-ttu-id="d2aa8-145">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d2aa8-145">Flag</span></span>                                                                                 | <span data-ttu-id="d2aa8-146">Description</span><span class="sxs-lookup"><span data-stu-id="d2aa8-146">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d2aa8-147">VMR-7 : MixerPref \_ DynamicSwitchToBOBVMR-9 : MixerPref9 \_ DynamicSwitchToBOB</span><span class="sxs-lookup"><span data-stu-id="d2aa8-147">VMR-7: MixerPref\_DynamicSwitchToBOBVMR-9: MixerPref9\_DynamicSwitchToBOB</span></span><br/> | <span data-ttu-id="d2aa8-148">Basculez vers le désentrelacement Bob.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-148">Switch to bob deinterlacing.</span></span>                                     |
| <span data-ttu-id="d2aa8-149">VMR-7 : MixerPref \_ DynamicDecimateBy2VMR-9 : MixerPref \_ DynamicDecimateBy2</span><span class="sxs-lookup"><span data-stu-id="d2aa8-149">VMR-7: MixerPref\_DynamicDecimateBy2VMR-9: MixerPref\_DynamicDecimateBy2</span></span><br/>  | <span data-ttu-id="d2aa8-150">Décimez l’image d’un facteur de 2 horizontalement et verticalement.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-150">Decimate the image by a factor of 2 horizontally and vertically.</span></span> |



 

<span data-ttu-id="d2aa8-151">Vous pouvez ajouter ou supprimer ces indicateurs pendant que le graphique de filtre est en cours d’exécution ; la modification est appliquée lorsque le mélangeur VMR compose la prochaine image vidéo.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-151">You can add or remove these flags while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.</span></span> <span data-ttu-id="d2aa8-152">Les indicateurs ne s’excluent pas mutuellement.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-152">The flags are not mutually exclusive.</span></span> <span data-ttu-id="d2aa8-153">Ces paramètres réduisent la qualité de l’image. en général, vous les appliquez uniquement lorsque la qualité vidéo est moins importante, par exemple si la vidéo est lue dans une petite partie de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2aa8-153">These settings reduce the quality of the image, so typically you would apply them only when video quality is less important — for example, if video is playing in a small portion of the user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2aa8-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2aa8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2aa8-155">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="d2aa8-155">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




