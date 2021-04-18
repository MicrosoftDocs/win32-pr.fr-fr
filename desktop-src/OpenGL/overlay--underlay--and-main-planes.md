---
title: Superposition, Underlay et plans principaux
description: Vous pouvez utiliser des plans de couche matérielle (plans superposés et Underlay) dans vos applications.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL sur Windows, plans de couche matérielle
- plans de couche matérielle OpenGL
- plans de recouvrement OpenGL
- Underlay plans OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509384"
---
# <a name="overlay-underlay-and-main-planes"></a><span data-ttu-id="d4d51-107">Superposition, Underlay et plans principaux</span><span class="sxs-lookup"><span data-stu-id="d4d51-107">Overlay, Underlay, and Main Planes</span></span>

<span data-ttu-id="d4d51-108">Vous pouvez utiliser des plans de couche matérielle (plans superposés et Underlay) dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="d4d51-108">You can use hardware layer planes (overlay and underlay planes) in your applications.</span></span> <span data-ttu-id="d4d51-109">Avec Windows, les formats de pixel décrivent les configurations en pixels d’un périphérique graphique.</span><span class="sxs-lookup"><span data-stu-id="d4d51-109">With Windows, pixel formats describe the pixel configurations of a graphics device.</span></span> <span data-ttu-id="d4d51-110">Chaque format de pixel décrit la profondeur et d’autres caractéristiques des mémoires tampons de couleur principales et décrit des mémoires tampons supplémentaires (par exemple, profondeur, accumulation, stencil et auxiliaire) utilisées par le plan principal.</span><span class="sxs-lookup"><span data-stu-id="d4d51-110">Each pixel format describes the depth and other characteristics of the main color buffers and describes additional buffers (such as depth, accumulation, stencil, and auxiliary) that the main plane uses.</span></span> <span data-ttu-id="d4d51-111">Les formats de pixel sont maintenant étendus pour inclure les mémoires tampons de superposition et Underlay.</span><span class="sxs-lookup"><span data-stu-id="d4d51-111">Pixel formats are now extended to include overlay and underlay buffers.</span></span>

<span data-ttu-id="d4d51-112">Les plans de couche ont toujours une mémoire tampon de couleur frontale et peuvent également inclure des tampons de couleur d’arrière-plan et de couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="d4d51-112">Layer planes always have a front-left color buffer and also can include front-right and back color buffers.</span></span> <span data-ttu-id="d4d51-113">Chaque plan de couche a un contexte de rendu spécifique à afficher dans les mémoires tampons de couche.</span><span class="sxs-lookup"><span data-stu-id="d4d51-113">Each layer plane has a specific rendering context to render into the layer buffers.</span></span> <span data-ttu-id="d4d51-114">Vous ne pouvez pas utiliser de fonctions de dessin GDI dans des plans de couche.</span><span class="sxs-lookup"><span data-stu-id="d4d51-114">You cannot use GDI drawing functions in layer planes.</span></span>

<span data-ttu-id="d4d51-115">Une fenêtre gère les tampons de couleur des plans de couche de la même manière qu’elle gère les tampons de couleur plan principal.</span><span class="sxs-lookup"><span data-stu-id="d4d51-115">A window manages the color buffers of layer planes similarly to the way it manages main-plane color buffers.</span></span> <span data-ttu-id="d4d51-116">Vous pouvez afficher plusieurs fenêtres avec des plans de superposition et/ou de Underlay en même temps.</span><span class="sxs-lookup"><span data-stu-id="d4d51-116">You can display multiple windows with overlay and/or underlay planes at the same time.</span></span> <span data-ttu-id="d4d51-117">Vous ne pouvez pas avoir des fenêtres de recouvrement flottantes qui peuvent se déplacer sur n’importe quelle fenêtre du plan de dessin principal.</span><span class="sxs-lookup"><span data-stu-id="d4d51-117">You cannot have free-floating overlay windows that can move over any window in the main drawing plane.</span></span> <span data-ttu-id="d4d51-118">En outre, étant donné que les plans sous-jacents sont obscurcis dans une fenêtre à tout moment, vous ne pouvez pas utiliser de plans contextuels matériels qui n’ont pas de couleur transparente.</span><span class="sxs-lookup"><span data-stu-id="d4d51-118">In addition, because it would obscure underlying planes in a window at all times, you cannot use hardware pop-up planes that have no transparent color.</span></span>

<span data-ttu-id="d4d51-119">Chaque plan de couche dans une fenêtre est associé à une palette.</span><span class="sxs-lookup"><span data-stu-id="d4d51-119">Each layer plane in a window has an associated palette.</span></span> <span data-ttu-id="d4d51-120">Vous pouvez définir la palette d’un plan de couche d’index de couleurs, mais la palette d’un plan de couleurs RVBA est fixe.</span><span class="sxs-lookup"><span data-stu-id="d4d51-120">You can set the palette of a color-index layer plane, but the palette of an RGBA color plane is fixed.</span></span> <span data-ttu-id="d4d51-121">Vous devez vous rendre compte de la palette appropriée lorsqu’une fenêtre se trouve au premier plan.</span><span class="sxs-lookup"><span data-stu-id="d4d51-121">You must realize the appropriate palette when a window is in the foreground.</span></span> <span data-ttu-id="d4d51-122">Les plans de couche ont une couleur ou un index de pixel transparent qui permet d’afficher tous les plans de la couche sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="d4d51-122">Layer planes have a transparent pixel color or index that enables any underlying layer planes to show through.</span></span>

<span data-ttu-id="d4d51-123">Vous pouvez copier l’état d’un contexte de rendu dans un autre contexte de rendu dans un plan de couche distinct.</span><span class="sxs-lookup"><span data-stu-id="d4d51-123">You can copy the state of a rendering context to another rendering context in a separate layer plane.</span></span> <span data-ttu-id="d4d51-124">Vous pouvez également partager des listes d’affichage entre des contextes de rendu dans différents plans de couche.</span><span class="sxs-lookup"><span data-stu-id="d4d51-124">You can also share display lists among rendering contexts in different layer planes.</span></span>

<span data-ttu-id="d4d51-125">Les fonctions suivantes sont utilisées avec les plans de couche :</span><span class="sxs-lookup"><span data-stu-id="d4d51-125">The following functions are used with layer planes:</span></span>

-   [<span data-ttu-id="d4d51-126">**wglCopyContext**</span><span class="sxs-lookup"><span data-stu-id="d4d51-126">**wglCopyContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [<span data-ttu-id="d4d51-127">**wglCreateLayerContext**</span><span class="sxs-lookup"><span data-stu-id="d4d51-127">**wglCreateLayerContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [<span data-ttu-id="d4d51-128">**wglDescribeLayerPlane**</span><span class="sxs-lookup"><span data-stu-id="d4d51-128">**wglDescribeLayerPlane**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [<span data-ttu-id="d4d51-129">**wglGetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="d4d51-129">**wglGetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [<span data-ttu-id="d4d51-130">**wglRealizeLayerPalette**</span><span class="sxs-lookup"><span data-stu-id="d4d51-130">**wglRealizeLayerPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [<span data-ttu-id="d4d51-131">**wglSetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="d4d51-131">**wglSetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [<span data-ttu-id="d4d51-132">**wglSwapLayerBuffers**</span><span class="sxs-lookup"><span data-stu-id="d4d51-132">**wglSwapLayerBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




