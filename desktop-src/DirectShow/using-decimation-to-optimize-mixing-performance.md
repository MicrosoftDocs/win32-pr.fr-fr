---
description: Utilisation de la décimalisation pour optimiser les performances de mixage
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Utilisation de la décimalisation pour optimiser les performances de mixage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866458"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a><span data-ttu-id="100ed-103">Utilisation de la décimalisation pour optimiser les performances de mixage</span><span class="sxs-lookup"><span data-stu-id="100ed-103">Using Decimation to Optimize Mixing Performance</span></span>

> [!IMPORTANT]
> <span data-ttu-id="100ed-104">L’optimisation décrite dans cette section dépend fortement du matériel sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="100ed-104">The optimization described in this section is highly dependent on the underlying hardware.</span></span> <span data-ttu-id="100ed-105">À moins que vous ne puissiez garantir le type de matériel graphique qui sera utilisé avec l’application, cela peut sérieusement nuire à l’apparence de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="100ed-105">Unless you can guarantee what type of graphics hardware will be used with the application, it may seriously degrade the appearance of the video image.</span></span>

 

<span data-ttu-id="100ed-106">La HDTV requiert beaucoup de puissance de traitement, qui, sur les systèmes les plus récents, est fournie principalement par la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="100ed-106">HDTV requires a lot of processing power, which on newer systems is provided mostly by the graphics card.</span></span> <span data-ttu-id="100ed-107">Toutefois, même si la carte graphique et le décodeur peuvent prendre en charge des résolutions de 1920 x 1080, il se peut que l’analyse de l’utilisateur ne soit pas toujours définie sur cette résolution.</span><span class="sxs-lookup"><span data-stu-id="100ed-107">But even if the graphics card and the decoder can support resolutions of 1920x1080, the user may not always have their monitor set to this resolution.</span></span> <span data-ttu-id="100ed-108">Dans ce cas, la puce graphique est requise pour créer une image 1920 x 1080, puis réduire la résolution avant de l’envoyer à la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="100ed-108">In this case, the graphics chip is required to create a 1920 x 1080 image, and then reduce the resolution before sending it to the frame buffer.</span></span>

<span data-ttu-id="100ed-109">Étant donné qu’il s’agit d’un gaspillage de la puissance de traitement, VMR offre un moyen de décimer (réduire) l’image au moment où elle est rendue sur la surface DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="100ed-109">Since this is a waste of processing power, the VMR provides a way to decimate (reduce) the image at the time it is being rendered onto the DirectDraw surface.</span></span> <span data-ttu-id="100ed-110">Cela élimine la copie de mémoire supplémentaire requise si l’image doit être redimensionnée après son rendu.</span><span class="sxs-lookup"><span data-stu-id="100ed-110">This eliminates the extra memory copy required if the image has to be resized after it has been rendered.</span></span>

<span data-ttu-id="100ed-111">**VMR-7 :** Pour activer la décimalisation, appelez [**IVMRMixerControl :: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) avec l' \_ indicateur DecimateOutput MixerPref.</span><span class="sxs-lookup"><span data-stu-id="100ed-111">**VMR-7:** To enable decimation, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_DecimateOutput flag.</span></span>

<span data-ttu-id="100ed-112">**VMR-9 :** Pour activer la décimalisation, appelez [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) avec l' \_ indicateur DecimateOutput MixerPref9.</span><span class="sxs-lookup"><span data-stu-id="100ed-112">**VMR-9:** To enable decimation, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_DecimateOutput flag.</span></span>

<span data-ttu-id="100ed-113">La méthode **SetMixingPrefs** doit être appelée avant que VMR soit connecté.</span><span class="sxs-lookup"><span data-stu-id="100ed-113">The **SetMixingPrefs** method must be called before the VMR is connected.</span></span> <span data-ttu-id="100ed-114">Les indicateurs de préférence de mixage ne peuvent pas être modifiés une fois que le graphique est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="100ed-114">The mixing preference flags cannot be changed once the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="100ed-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="100ed-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="100ed-116">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="100ed-116">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



