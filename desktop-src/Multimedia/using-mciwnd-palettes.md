---
title: Utilisation des palettes MCIWnd
description: Utilisation des palettes MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette macro)
- MCIWndSetPalette macro)
- MCIWndRealize macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940959"
---
# <a name="using-mciwnd-palettes"></a><span data-ttu-id="5e584-106">Utilisation des palettes MCIWnd</span><span class="sxs-lookup"><span data-stu-id="5e584-106">Using MCIWnd Palettes</span></span>

<span data-ttu-id="5e584-107">La diffusion de clips vidéo avec une profondeur de couleur de 8 bits (capacité de 256) nécessite une palette pour définir les couleurs à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5e584-107">Playing video clips with 8-bit color depth (256-color capacity) requires a palette to define the colors being used.</span></span> <span data-ttu-id="5e584-108">Parfois, la palette incluse avec un clip vidéo n’est pas la palette la plus appropriée à utiliser lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="5e584-108">Sometimes, the palette included with a video clip is not the most appropriate palette to use during playback.</span></span> <span data-ttu-id="5e584-109">Dans ce cas, MCIWnd offre trois moyens de gérer les palettes pour la lecture :</span><span class="sxs-lookup"><span data-stu-id="5e584-109">In this case, MCIWnd provides three ways to manage palettes for playback:</span></span>

-   <span data-ttu-id="5e584-110">Récupérez un handle vers la palette associée à une fenêtre MCIWnd à l’aide de la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="5e584-110">Retrieve a handle to the palette associated with an MCIWnd window by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span> <span data-ttu-id="5e584-111">La palette n’est pas nécessairement associée exclusivement à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5e584-111">The palette is not necessarily associated exclusively with the MCIWnd window.</span></span> <span data-ttu-id="5e584-112">D’autres applications peuvent accéder au handle de palette, et même l’invalider.</span><span class="sxs-lookup"><span data-stu-id="5e584-112">Other applications can access, and even invalidate, the palette handle.</span></span> <span data-ttu-id="5e584-113">Par conséquent, votre application doit anticiper l’utilisation globale de la palette et, lorsque vous avez terminé avec la palette, ne doit pas la libérer.</span><span class="sxs-lookup"><span data-stu-id="5e584-113">Consequently, your application should anticipate the global use of the palette and, when finished with the palette, should not free it.</span></span>
-   <span data-ttu-id="5e584-114">Spécifiez une nouvelle palette à utiliser avec le clip vidéo associé à une fenêtre MCIWnd à l’aide de la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="5e584-114">Specify a new palette to use with the video clip associated with an MCIWnd window by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>
-   <span data-ttu-id="5e584-115">Réalisez la palette associée à une fenêtre MCIWnd dans la palette système à l’aide de la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="5e584-115">Realize the palette associated with an MCIWnd window to the system palette by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span> <span data-ttu-id="5e584-116">Cette macro appelle la fonction [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) avec la palette associée à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5e584-116">This macro calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function with the palette associated with the MCIWnd window.</span></span> <span data-ttu-id="5e584-117">Si les gestionnaires de messages de votre application pour [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) appellent uniquement **RealizePalette** ou **MCIWndRealize**, vous devez transférer ces messages à MCIWnd si vous ne les gérez pas vous-même.</span><span class="sxs-lookup"><span data-stu-id="5e584-117">If your application message handlers for [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) call only **RealizePalette** or **MCIWndRealize**, you must forward these messages to MCIWnd if you do not handle them yourself.</span></span>

> [!Note]  
> <span data-ttu-id="5e584-118">Quand un clip vidéo avec une profondeur de couleur de 8 bits est chargé dans la fenêtre MCIWnd, la palette incluse avec ce clip remplace la palette associée à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5e584-118">When a video clip with 8-bit color depth is loaded into the MCIWnd window, the palette included with that clip replaces the palette associated with the MCIWnd window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5e584-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e584-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e584-120">Améliorations de la lecture</span><span class="sxs-lookup"><span data-stu-id="5e584-120">Playback Enhancements</span></span>](playback-enhancements.md)
</dt> </dl>

 

 