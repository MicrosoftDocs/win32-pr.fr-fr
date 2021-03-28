---
description: En plus de la région de mise à jour, chaque fenêtre possède une zone visible qui définit la partie de la fenêtre visible par l’utilisateur.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Régions de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034902"
---
# <a name="window-regions"></a><span data-ttu-id="e598f-103">Régions de fenêtre</span><span class="sxs-lookup"><span data-stu-id="e598f-103">Window Regions</span></span>

<span data-ttu-id="e598f-104">En plus de la région de mise à jour, chaque fenêtre possède une *zone visible* qui définit la partie de la fenêtre visible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e598f-104">In addition to the update region, every window has a *visible region* that defines the window portion visible to the user.</span></span> <span data-ttu-id="e598f-105">Le système modifie la zone visible pour la fenêtre chaque fois que la fenêtre change de taille ou lorsqu’une autre fenêtre est déplacée de telle sorte qu’elle masque ou expose une partie de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e598f-105">The system changes the visible region for the window whenever the window changes size or whenever another window is moved such that it obscures or exposes a portion of the window.</span></span> <span data-ttu-id="e598f-106">Les applications ne peuvent pas modifier directement la région visible, mais le système utilise automatiquement la région visible pour créer la zone de découpage pour tout contexte de périphérique d’affichage récupéré pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e598f-106">Applications cannot change the visible region directly, but the system automatically uses the visible region to create the clipping region for any display device context retrieved for the window.</span></span>

<span data-ttu-id="e598f-107">La *zone de découpage* détermine où le système autorise le dessin.</span><span class="sxs-lookup"><span data-stu-id="e598f-107">The *clipping region* determines where the system permits drawing.</span></span> <span data-ttu-id="e598f-108">Lorsque l’application récupère un contexte de périphérique d’affichage à l’aide de la fonction [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , le système définit la zone de découpage pour le contexte de périphérique sur l’intersection de la région visible et de la région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e598f-108">When the application retrieves a display device context using the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, the system sets the clipping region for the device context to the intersection of the visible region and the update region.</span></span> <span data-ttu-id="e598f-109">Les applications peuvent modifier la zone de découpage à l’aide de fonctions telles que [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) et [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), afin de limiter davantage le dessin à une partie particulière de la zone de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e598f-109">Applications can change the clipping region by using functions such as [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) and [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), to further limit drawing to a particular portion of the update area.</span></span>

<span data-ttu-id="e598f-110">Les \_ styles WS CLIPCHILDREN et WS \_ CLIPSIBLINGS spécifient plus en détail la façon dont le système calcule la région visible pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e598f-110">The WS\_CLIPCHILDREN and WS\_CLIPSIBLINGS styles further specify how the system calculates the visible region for a window.</span></span> <span data-ttu-id="e598f-111">Si une fenêtre possède un ou plusieurs de ces styles, la zone visible exclut les fenêtres enfants ou sœurs (Windows ayant la même fenêtre parente).</span><span class="sxs-lookup"><span data-stu-id="e598f-111">If a window has one or both of these styles, the visible region excludes any child window or sibling windows (windows having the same parent window).</span></span> <span data-ttu-id="e598f-112">Par conséquent, le dessin qui pourrait entraîner une intrusion dans ces fenêtres sera toujours coupé.</span><span class="sxs-lookup"><span data-stu-id="e598f-112">Therefore, drawing that would otherwise intrude in these windows will always be clipped.</span></span>

 

 



