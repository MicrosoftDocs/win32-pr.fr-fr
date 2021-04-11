---
title: Source d’image secondaire faisant l’objet d’un push
description: Source d’image secondaire faisant l’objet d’un push
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Apparences mobiles du lecteur Windows Media, source de l’image du bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029285"
---
# <a name="pushed-secondary-image-source"></a><span data-ttu-id="8041d-108">Source d’image secondaire faisant l’objet d’un push</span><span class="sxs-lookup"><span data-stu-id="8041d-108">Pushed Secondary Image Source</span></span>

<span data-ttu-id="8041d-109">Selon la fonction Button, vous devrez peut-être définir l’emplacement de l’image Poussée pour l’état secondaire du bouton.</span><span class="sxs-lookup"><span data-stu-id="8041d-109">Depending on the button function, you may need to define the location of the pushed image for the secondary state of the button.</span></span> <span data-ttu-id="8041d-110">Il s’agit de l’image que les utilisateurs voient lorsqu’ils poussent le bouton de fonction PlayPause la deuxième fois.</span><span class="sxs-lookup"><span data-stu-id="8041d-110">This will be the image users see when they push a PlayPause function button the second time.</span></span>

<span data-ttu-id="8041d-111">Pour définir cette image, vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace.</span><span class="sxs-lookup"><span data-stu-id="8041d-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="8041d-112">Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type d’image à partir duquel vous dessinez.</span><span class="sxs-lookup"><span data-stu-id="8041d-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the image type you are drawing from.</span></span>

<span data-ttu-id="8041d-113">Par exemple, pour définir l’image de Push pour une source d’image secondaire, si votre image est à l’intérieur de la bitmap push, tapez :</span><span class="sxs-lookup"><span data-stu-id="8041d-113">For example, to define the Pushed image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 248,0

```



<span data-ttu-id="8041d-114">Les États secondaires ne peuvent pas avoir d’image désactivée.</span><span class="sxs-lookup"><span data-stu-id="8041d-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="8041d-115">Les images secondaires sont supposées avoir la même largeur et la même hauteur que l’image principale.</span><span class="sxs-lookup"><span data-stu-id="8041d-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8041d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8041d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8041d-117">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="8041d-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




