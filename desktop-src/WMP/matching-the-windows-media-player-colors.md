---
title: Correspondance des couleurs du lecteur Windows Media
description: Correspondance des couleurs du lecteur Windows Media
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player Online stores, correspondance des couleurs du lecteur Windows Media
- magasins en ligne, correspondance des couleurs du lecteur Windows Media
- tapez 1 magasins en ligne, en faisant correspondre les couleurs du lecteur Windows Media
- tapez 2 magasins en ligne, en faisant correspondre les couleurs du lecteur Windows Media
- Windows Media Player Online stores, correspondance des couleurs du lecteur Windows Media
- magasins en ligne, correspondance des couleurs du lecteur Windows Media
- types 1 magasins en ligne, correspondance des couleurs du lecteur Windows Media
- type 2 magasins en ligne, correspondance des couleurs du lecteur Windows Media
- Windows Media Player Online stores, correspondance des couleurs pour Windows Media Player
- magasins en ligne, correspondance des couleurs pour Windows Media Player
- tapez 1 magasins en ligne, correspondance des couleurs pour Windows Media Player
- type 2 magasins en ligne, correspondance des couleurs pour le lecteur Windows Media
- correspondance des couleurs pour le lecteur Windows Media
- correspondance des couleurs du lecteur Windows Media
- Lecteur Windows Media, couleurs correspondantes
- Lecteur Windows Media, correspondance des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512462"
---
# <a name="matching-the-windows-media-player-colors"></a><span data-ttu-id="ef140-119">Correspondance des couleurs du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="ef140-119">Matching the Windows Media Player Colors</span></span>

<span data-ttu-id="ef140-120">Il est facile de faire en sorte que votre page Web de boutique en ligne corresponde au jeu de couleurs du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ef140-120">Making your online store webpage match the Windows Media Player color scheme is easy.</span></span> <span data-ttu-id="ef140-121">Gérez simplement l’événement **External. OnColorChange** .</span><span class="sxs-lookup"><span data-stu-id="ef140-121">Simply handle the **External.OnColorChange** event.</span></span> <span data-ttu-id="ef140-122">Pour spécifier une fonction pour gérer l’événement, utilisez un code semblable au suivant lors du chargement de votre page Web :</span><span class="sxs-lookup"><span data-stu-id="ef140-122">To specify a function to handle the event, use code like the following when your webpage loads:</span></span>


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



<span data-ttu-id="ef140-123">Chaque fois que l’utilisateur modifie le modèle de couleurs du lecteur Windows Media, le lecteur appellera votre fonction.</span><span class="sxs-lookup"><span data-stu-id="ef140-123">Each time the user changes the color scheme of Windows Media Player, the Player will call your function.</span></span> <span data-ttu-id="ef140-124">L’exemple suivant montre une fonction simple qui définit l’arrière-plan de la page Web pour qu’il corresponde à la propriété **External. appColorLight** :</span><span class="sxs-lookup"><span data-stu-id="ef140-124">The following example shows a simple function that sets the webpage background to match the **External.appColorLight** property:</span></span>


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



<span data-ttu-id="ef140-125">D’autres propriétés de couleur sont également disponibles pour votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="ef140-125">There are other color properties available for your use as well.</span></span> <span data-ttu-id="ef140-126">Consultez [objet externe pour les magasins en ligne de type 2](external-object-for-type-2-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="ef140-126">See [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef140-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef140-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef140-128">**External. appColorLight**</span><span class="sxs-lookup"><span data-stu-id="ef140-128">**External.appColorLight**</span></span>](external-appcolorlight.md)
</dt> <dt>

[<span data-ttu-id="ef140-129">**External. OnColorChange, événement**</span><span class="sxs-lookup"><span data-stu-id="ef140-129">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
</dt> <dt>

[<span data-ttu-id="ef140-130">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="ef140-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




