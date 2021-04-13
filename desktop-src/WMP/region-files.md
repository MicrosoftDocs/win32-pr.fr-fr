---
title: Fichiers de région
description: Fichiers de région
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player Mobile Skins, fichiers art
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, les fichiers de région
- Apparences mobiles du lecteur Windows Media, fichiers de région
- apparences, fichiers de région
- Fichiers de région dans les apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311113"
---
# <a name="region-files"></a><span data-ttu-id="a6d1b-110">Fichiers de région</span><span class="sxs-lookup"><span data-stu-id="a6d1b-110">Region Files</span></span>

<span data-ttu-id="a6d1b-111">Les fichiers de région sont requis si vous utilisez n’importe quel type de bouton d’accès (2PushHit, PushHit ou ToggleHit).</span><span class="sxs-lookup"><span data-stu-id="a6d1b-111">Region files are required if you use any type of hit button (2PushHit, PushHit, or ToggleHit).</span></span>

<span data-ttu-id="a6d1b-112">Les fichiers de région sont utilisés pour définir des zones qui répondent à un TAP, également appelé « hit », sur un bouton spécifique.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-112">Region files are used to define areas that will respond to a tap, also known as a hit, on a specific button.</span></span> <span data-ttu-id="a6d1b-113">Pour chaque bouton d’accès, une zone de la bitmap de région reçoit une couleur Web spécifique (telle que \# FF0000, qui est la valeur du rouge plein).</span><span class="sxs-lookup"><span data-stu-id="a6d1b-113">For each hit button, an area in the Region bitmap is given a specific Web color (such as \#FF0000, which is the value for solid red).</span></span> <span data-ttu-id="a6d1b-114">Le numéro de couleur est spécifié dans la définition du bouton de la région.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-114">The color number is specified in the region button definition.</span></span> <span data-ttu-id="a6d1b-115">Lorsque l’utilisateur affiche l’apparence, l’image du bouton est superposée sur l’arrière-plan à l’aide des coordonnées de la zone dans la bitmap de la région.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-115">When the user displays the skin, the button image is superimposed onto the background using the coordinates of the area in the Region bitmap.</span></span>

<span data-ttu-id="a6d1b-116">Par exemple, vous pouvez dessiner un cercle rouge à l’emplacement correspondant à l’emplacement du bouton suivant et le colorer en rouge ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="a6d1b-116">For example, you could draw a red circle in a location corresponding to the location of the Next button and color it solid red (\#FF0000).</span></span> <span data-ttu-id="a6d1b-117">Ensuite, dans la définition du bouton, vous pouvez affecter une valeur RVB d’accès de 255, 0, 0 (qui est l’équivalent RVB de \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="a6d1b-117">Then in the button definition, you could assign a hit RGB value of 255,0,0 (which is the RGB equivalent of \#FF0000).</span></span> <span data-ttu-id="a6d1b-118">Dans ce cas, le bouton suivant répond uniquement aux pressions (correspondances) à l’intérieur du cercle rouge.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-118">In this case, the Next button would only respond to taps (hits) inside the red circle.</span></span>

<span data-ttu-id="a6d1b-119">Les boutons d’accès sont utilisés lorsque vous souhaitez définir des formes autres que des rectangles.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-119">Hit buttons are used when you want to define shapes other than rectangles.</span></span> <span data-ttu-id="a6d1b-120">Vous devez toujours définir les coordonnées de chaque bouton afin que les images secondaires, telles que Push et Disabled, puissent être localisées correctement.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-120">You must still define the coordinates for each button so that secondary images such as Pushed and Disabled can be located correctly.</span></span> <span data-ttu-id="a6d1b-121">Dans la pratique, chaque bouton est délimité par un rectangle, et ces rectangles de limites imaginaires ne doivent pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-121">In practice, each button is bounded by a rectangle, and these imaginary boundary rectangles must not overlap.</span></span>

> [!Note]  
> <span data-ttu-id="a6d1b-122">Les fichiers d’art de région ne sont pas nécessaires dans les habillages Windows Media Player 10 mobile, car les types de boutons ne sont pas pris en charge dans le lecteur Windows Media 10 mobile ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-122">Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="a6d1b-123">L’image suivante est un fichier de région classique.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-123">The following image is a typical Region file.</span></span>

![fichier de région](images/cesdkreg.png)

<span data-ttu-id="a6d1b-125">Ce fichier définit les parties de l’apparence pour chaque bouton de type d’accès.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-125">This file defines the parts of the skin for each hit-type button.</span></span> <span data-ttu-id="a6d1b-126">Chaque couleur est identifiée par son numéro de couleur dans la section boutons du fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="a6d1b-126">Each color will be identified by its color number in the Buttons section of the skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6d1b-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6d1b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d1b-128">**Fichiers art**</span><span class="sxs-lookup"><span data-stu-id="a6d1b-128">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




