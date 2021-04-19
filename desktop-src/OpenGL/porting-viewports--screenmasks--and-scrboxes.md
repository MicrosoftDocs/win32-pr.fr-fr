---
title: Portage des Viewports, Screenmasks et Scrboxes
description: Les fonctions de fenêtre d’affichage du code IRIS suivantes n’ont pas d’équivalent OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Portage de l’IRIS dans le GL, fonctions de fenêtre d’affichage
- Portage à partir de IRIS GL, fonctions Viewport
- portage vers OpenGL à partir de l’IRIS GL, fonctions Viewport
- Portage OpenGL à partir de IRIS GL, fonctions Viewport
- fonctions de fenêtre d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510812"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a><span data-ttu-id="70d31-108">Portage des Viewports, Screenmasks et Scrboxes</span><span class="sxs-lookup"><span data-stu-id="70d31-108">Porting Viewports, Screenmasks, and Scrboxes</span></span>

<span data-ttu-id="70d31-109">Les fonctions de fenêtre d’affichage du code IRIS suivantes n’ont pas d’équivalent OpenGL :</span><span class="sxs-lookup"><span data-stu-id="70d31-109">The following IRIS GL viewport functions have no OpenGL equivalent:</span></span>

-   <span data-ttu-id="70d31-110">**reshapeviewport**</span><span class="sxs-lookup"><span data-stu-id="70d31-110">**reshapeviewport**</span></span>
-   <span data-ttu-id="70d31-111">**scrbox**</span><span class="sxs-lookup"><span data-stu-id="70d31-111">**scrbox**</span></span>
-   <span data-ttu-id="70d31-112">**getscrbox**</span><span class="sxs-lookup"><span data-stu-id="70d31-112">**getscrbox**</span></span>

<span data-ttu-id="70d31-113">Avec la fonction IRIS GL **Viewport** , vous spécifiez les coordonnées x (en pixels) de gauche et de droite d’un rectangle de fenêtre d’affichage et les coordonnées y pour le haut et le bas.</span><span class="sxs-lookup"><span data-stu-id="70d31-113">With the IRIS GL **viewport** function, you specify the x coordinates (in pixels) for the left and right of a viewport rectangle and the y coordinates for the top and bottom.</span></span> <span data-ttu-id="70d31-114">Toutefois, avec la fonction OpenGL [**glViewport**](glviewport.md) , vous spécifiez les coordonnées x et y (en pixels) du coin inférieur gauche du rectangle de la fenêtre d’affichage, ainsi que sa largeur et sa hauteur.</span><span class="sxs-lookup"><span data-stu-id="70d31-114">With the OpenGL [**glViewport**](glviewport.md) function, however, you specify the x and y coordinates (in pixels) of the lower-left corner of the viewport rectangle along with its width and height.</span></span>

<span data-ttu-id="70d31-115">Le tableau suivant répertorie les fonctions de fenêtre d’affichage du GL d’IRIS et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="70d31-115">The following table lists IRIS GL viewport functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="70d31-116">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="70d31-116">IRIS GL function</span></span>                          | <span data-ttu-id="70d31-117">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="70d31-117">OpenGL function</span></span>                                                                                         | <span data-ttu-id="70d31-118">Signification</span><span class="sxs-lookup"><span data-stu-id="70d31-118">Meaning</span></span>                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="70d31-119">**fenêtre d’affichage** (gauche, droite, bas, haut)</span><span class="sxs-lookup"><span data-stu-id="70d31-119">**viewport** ( left, right, bottom, top )</span></span> | <span data-ttu-id="70d31-120">[**glViewport**](glviewport.md) (x, y, largeur, hauteur)</span><span class="sxs-lookup"><span data-stu-id="70d31-120">[**glViewport**](glviewport.md) ( x, y, width, height )</span></span>                                                | <span data-ttu-id="70d31-121">Définit la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="70d31-121">Sets the viewport.</span></span>           |
| <span data-ttu-id="70d31-122">**popviewportpushviewport**</span><span class="sxs-lookup"><span data-stu-id="70d31-122">**popviewportpushviewport**</span></span><br/>    | <span data-ttu-id="70d31-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( \_ bit de fenêtre d’affichage GL \_ )</span><span class="sxs-lookup"><span data-stu-id="70d31-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL\_VIEWPORT\_BIT )</span></span><br/> | <span data-ttu-id="70d31-124">Exécute un push sur la pile et le dépile.</span><span class="sxs-lookup"><span data-stu-id="70d31-124">Pushes and pops the stack.</span></span>   |
| <span data-ttu-id="70d31-125">**getviewport**</span><span class="sxs-lookup"><span data-stu-id="70d31-125">**getviewport**</span></span>                           | <span data-ttu-id="70d31-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ fenêtre d’affichage GL)</span><span class="sxs-lookup"><span data-stu-id="70d31-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_VIEWPORT )</span></span>               | <span data-ttu-id="70d31-127">Retourne les dimensions de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="70d31-127">Returns viewport dimensions.</span></span> |



 

<span data-ttu-id="70d31-128">??</span><span class="sxs-lookup"><span data-stu-id="70d31-128">??</span></span>

 

 





