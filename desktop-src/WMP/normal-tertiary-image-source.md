---
title: Source d’image tertiaire normale
description: Source d’image tertiaire normale
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Apparences mobiles du lecteur Windows Media, source de l’image du bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380235"
---
# <a name="normal-tertiary-image-source"></a><span data-ttu-id="fcca7-108">Source d’image tertiaire normale</span><span class="sxs-lookup"><span data-stu-id="fcca7-108">Normal Tertiary Image Source</span></span>

<span data-ttu-id="fcca7-109">La fonction bouton PlayPauseStop exige que vous définissiez l’emplacement de l’image normale pour l’État tertiaire du bouton.</span><span class="sxs-lookup"><span data-stu-id="fcca7-109">The PlayPauseStop button function requires that you define the location of the normal image for the tertiary state of the button.</span></span> <span data-ttu-id="fcca7-110">Il s’agit de l’image que les utilisateurs voient après avoir appuyé sur le bouton PlayPauseStop pour commencer à diffuser en continu une diffusion en direct.</span><span class="sxs-lookup"><span data-stu-id="fcca7-110">This will be the image users see after they have pushed the PlayPauseStop button to begin streaming a live broadcast.</span></span>

<span data-ttu-id="fcca7-111">Pour définir cette image, vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace.</span><span class="sxs-lookup"><span data-stu-id="fcca7-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="fcca7-112">Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type de bitmap à partir duquel vous dessinez.</span><span class="sxs-lookup"><span data-stu-id="fcca7-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="fcca7-113">Par exemple, pour définir l’image normale pour une source d’image tertiaire, si votre image est à l’intérieur de la bitmap push, tapez :</span><span class="sxs-lookup"><span data-stu-id="fcca7-113">For example, to define the normal image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 286,0

```



<span data-ttu-id="fcca7-114">Les États tertiaires ne peuvent pas avoir d’image désactivée.</span><span class="sxs-lookup"><span data-stu-id="fcca7-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="fcca7-115">Les images tertiaires sont supposées avoir la même largeur et la même hauteur que les images primaires et secondaires.</span><span class="sxs-lookup"><span data-stu-id="fcca7-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcca7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcca7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcca7-117">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="fcca7-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




