---
title: Problèmes spéciaux de Portage du GL IRIS
description: Problèmes spéciaux de Portage du GL IRIS
ms.assetid: dcf7967a-2867-4443-a1c8-8335c6fe016a
keywords:
- OpenGL sur Windows, Portage du GL IRIS
- portage vers OpenGL, IRIS GL
- Portage OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1273a873f3a39a5d237f9a5845a72f87156e001c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106541156"
---
# <a name="special-iris-gl-porting-issues"></a><span data-ttu-id="90c2c-106">Problèmes spéciaux de Portage du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="90c2c-106">Special IRIS GL Porting Issues</span></span>

<span data-ttu-id="90c2c-107">Les rubriques suivantes décrivent les techniques permettant de porter des parties spécifiques de votre code IRIS GL vers du code OpenGL.</span><span class="sxs-lookup"><span data-stu-id="90c2c-107">The following topics describe techniques for porting specific parts of your IRIS GL code to OpenGL code.</span></span>

-   [<span data-ttu-id="90c2c-108">Portage greset</span><span class="sxs-lookup"><span data-stu-id="90c2c-108">Porting greset</span></span>](porting-greset.md)
-   [<span data-ttu-id="90c2c-109">Portage des fonctions de « récupération » de l’IRIS GL</span><span class="sxs-lookup"><span data-stu-id="90c2c-109">Porting IRIS GL "Get" Functions</span></span>](porting-iris-gl-get-functions.md)
-   [<span data-ttu-id="90c2c-110">Portage de code nécessitant une position graphique actuelle</span><span class="sxs-lookup"><span data-stu-id="90c2c-110">Porting Code that Requires a Current Graphics Position</span></span>](porting-code-that-requires-a-current-graphics-position.md)
-   [<span data-ttu-id="90c2c-111">Portage des fonctions de dessin</span><span class="sxs-lookup"><span data-stu-id="90c2c-111">Porting Drawing Functions</span></span>](porting-drawing-functions.md)
-   [<span data-ttu-id="90c2c-112">Portage de la couleur, de l’ombrage et du code Writemask</span><span class="sxs-lookup"><span data-stu-id="90c2c-112">Porting Color, Shading, and Writemask Code</span></span>](porting-color--shading--and-writemask-code.md)
-   [<span data-ttu-id="90c2c-113">Portage des opérations de pixels</span><span class="sxs-lookup"><span data-stu-id="90c2c-113">Porting Pixel Operations</span></span>](porting-pixel-operations.md)
-   [<span data-ttu-id="90c2c-114">Cueing de profondeur de Portage et commandes de brouillard</span><span class="sxs-lookup"><span data-stu-id="90c2c-114">Porting Depth Cueing and Fog Commands</span></span>](porting-depth-cueing-and-fog-commands.md)
-   [<span data-ttu-id="90c2c-115">Portage des fonctions de courbe et de surface</span><span class="sxs-lookup"><span data-stu-id="90c2c-115">Porting Curve and Surface Functions</span></span>](porting-curve-and-surface-functions.md)
-   [<span data-ttu-id="90c2c-116">Portage de fonctions d’anticrénelage</span><span class="sxs-lookup"><span data-stu-id="90c2c-116">Porting Antialiasing Functions</span></span>](porting-antialiasing-functions.md)
-   [<span data-ttu-id="90c2c-117">Portage des appels de tampon d’accumulation</span><span class="sxs-lookup"><span data-stu-id="90c2c-117">Porting Accumulation Buffer Calls</span></span>](porting-accumulation-buffer-calls.md)
-   [<span data-ttu-id="90c2c-118">Portage des appels au plan du gabarit</span><span class="sxs-lookup"><span data-stu-id="90c2c-118">Porting Stencil Plane Calls</span></span>](porting-stencil-plane-calls.md)
-   [<span data-ttu-id="90c2c-119">Portage des listes d’affichage</span><span class="sxs-lookup"><span data-stu-id="90c2c-119">Porting Display Lists</span></span>](porting-display-lists.md)
-   [<span data-ttu-id="90c2c-120">Portage des ensembles de paramètres, des liaisons et des ensembles</span><span class="sxs-lookup"><span data-stu-id="90c2c-120">Porting Defs, Binds, and Sets</span></span>](porting-defs--binds--and-sets.md)
-   [<span data-ttu-id="90c2c-121">Portage des fonctions d’éclairage et de matériaux</span><span class="sxs-lookup"><span data-stu-id="90c2c-121">Porting Lighting and Materials Functions</span></span>](porting-lighting-and-materials-functions.md)
-   [<span data-ttu-id="90c2c-122">Portage des fonctions de texture</span><span class="sxs-lookup"><span data-stu-id="90c2c-122">Porting Texture Functions</span></span>](porting-texture-functions.md)
-   [<span data-ttu-id="90c2c-123">Fonctions de sélection du Portage</span><span class="sxs-lookup"><span data-stu-id="90c2c-123">Porting Picking Functions</span></span>](porting-picking-functions.md)
-   [<span data-ttu-id="90c2c-124">Portage des fonctions de commentaires</span><span class="sxs-lookup"><span data-stu-id="90c2c-124">Porting Feedback Functions</span></span>](porting-feedback-functions.md)

 

 




