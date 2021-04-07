---
title: Source d’image tertiaire envoyée
description: Source d’image tertiaire envoyée
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Apparences mobiles du lecteur Windows Media, source de l’image du bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939989"
---
# <a name="pushed-tertiary-image-source"></a><span data-ttu-id="f381e-108">Source d’image tertiaire envoyée</span><span class="sxs-lookup"><span data-stu-id="f381e-108">Pushed Tertiary Image Source</span></span>

<span data-ttu-id="f381e-109">La fonction bouton PlayPauseStop exige que vous définissiez l’emplacement de l’image Push pour l’État tertiaire du bouton.</span><span class="sxs-lookup"><span data-stu-id="f381e-109">The PlayPauseStop button function requires that you define the location of the pushed image for the tertiary state of the button.</span></span> <span data-ttu-id="f381e-110">Il s’agit de l’image que les utilisateurs voient quand ils poussent le bouton PlayPauseStop lors de la diffusion en continu d’une diffusion en direct.</span><span class="sxs-lookup"><span data-stu-id="f381e-110">This will be the image users see when they push the PlayPauseStop button while streaming a live broadcast.</span></span>

<span data-ttu-id="f381e-111">Pour définir cette image, vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace.</span><span class="sxs-lookup"><span data-stu-id="f381e-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="f381e-112">Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type de bitmap à partir duquel vous dessinez.</span><span class="sxs-lookup"><span data-stu-id="f381e-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="f381e-113">Par exemple, pour définir l’image faisant l’objet d’un push pour une source d’image tertiaire, si votre image est à l’intérieur de la bitmap push, tapez :</span><span class="sxs-lookup"><span data-stu-id="f381e-113">For example, to define the pushed image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 324,0

```



<span data-ttu-id="f381e-114">Les États tertiaires ne peuvent pas avoir d’image désactivée.</span><span class="sxs-lookup"><span data-stu-id="f381e-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="f381e-115">Les images tertiaires sont supposées avoir la même largeur et la même hauteur que les images primaires et secondaires.</span><span class="sxs-lookup"><span data-stu-id="f381e-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f381e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f381e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f381e-117">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="f381e-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




