---
title: Gestionnaire de fenêtres du Bureau
description: La fonctionnalité de composition du bureau, introduite dans Windows Vista, a modifié fondamentalement la manière dont les applications affichent les pixels à l’écran.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gestionnaire de fenêtrage (DWM), à propos de
- DWM (Gestionnaire de fenêtrage), à propos de
- Gestionnaire de fenêtrage (DWM), composition
- DWM (Gestionnaire de fenêtrage), composition
- composition du Bureau
- composition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673661"
---
# <a name="desktop-window-manager"></a><span data-ttu-id="20f7c-109">Gestionnaire de fenêtres du Bureau</span><span class="sxs-lookup"><span data-stu-id="20f7c-109">Desktop Window Manager</span></span>

<span data-ttu-id="20f7c-110">La fonctionnalité de composition du bureau, introduite dans Windows Vista, a modifié fondamentalement la manière dont les applications affichent les pixels à l’écran.</span><span class="sxs-lookup"><span data-stu-id="20f7c-110">The desktop composition feature, introduced in Windows Vista, fundamentally changed the way applications display pixels on the screen.</span></span> <span data-ttu-id="20f7c-111">Lorsque la composition du Bureau est activée, les fenêtres individuelles ne dessinent plus directement sur l’écran ou l’appareil d’affichage principal comme c’était le cas dans les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="20f7c-111">When desktop composition is enabled, individual windows no longer draw directly to the screen or primary display device as they did in previous versions of Windows.</span></span> <span data-ttu-id="20f7c-112">Au lieu de cela, leur dessin est redirigé vers des surfaces hors écran dans la mémoire vidéo, qui sont ensuite rendues dans une image de bureau et présentées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="20f7c-112">Instead, their drawing is redirected to off-screen surfaces in video memory, which are then rendered into a desktop image and presented on the display.</span></span>

<span data-ttu-id="20f7c-113">La composition du Bureau est effectuée par le Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="20f7c-113">Desktop composition is performed by the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="20f7c-114">Grâce à la composition du bureau, DWM active les effets visuels sur le bureau, ainsi que diverses fonctionnalités telles que les cadres de fenêtres en verre, les animations de transition de fenêtre 3D, Windows Flip et Windows Flip3D et la haute résolution.</span><span class="sxs-lookup"><span data-stu-id="20f7c-114">Through desktop composition, DWM enables visual effects on the desktop as well as various features such as glass window frames, 3-D window transition animations, Windows Flip and Windows Flip3D, and high resolution support.</span></span>

<span data-ttu-id="20f7c-115">Le Gestionnaire de fenêtrage s’exécute en tant que service Windows.</span><span class="sxs-lookup"><span data-stu-id="20f7c-115">The Desktop Window Manager runs as a Windows service.</span></span> <span data-ttu-id="20f7c-116">Vous pouvez l’activer et le désactiver à l’aide de l’élément outils d’administration du panneau de configuration, sous services, comme gestionnaire de sessions Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="20f7c-116">It can be enabled and disabled through the Administrative Tools Control Panel item, under Services, as Desktop Window Manager Session Manager.</span></span>

<span data-ttu-id="20f7c-117">La plupart des fonctionnalités DWM peuvent être contrôlées ou accessibles par une application via les API DWM.</span><span class="sxs-lookup"><span data-stu-id="20f7c-117">Many of the DWM features can be controlled or accessed by an application through the DWM APIs.</span></span> <span data-ttu-id="20f7c-118">La documentation suivante décrit les fonctionnalités et les exigences des API DWM.</span><span class="sxs-lookup"><span data-stu-id="20f7c-118">The following documentation describes the features and requirements of the DWM APIs.</span></span>

-   [<span data-ttu-id="20f7c-119">Vues d’ensemble de DWM</span><span class="sxs-lookup"><span data-stu-id="20f7c-119">DWM Overviews</span></span>](desktop-window-manager-overviews.md)
-   [<span data-ttu-id="20f7c-120">Exemple de code DWM</span><span class="sxs-lookup"><span data-stu-id="20f7c-120">DWM Sample Code</span></span>](dwm-samples.md)
-   [<span data-ttu-id="20f7c-121">Référence DWM</span><span class="sxs-lookup"><span data-stu-id="20f7c-121">DWM Reference</span></span>](reference.md)

 

 




