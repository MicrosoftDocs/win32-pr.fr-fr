---
title: Ajout de visualisations
description: Ajout de visualisations
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- création d’apparences, visualisations
- Apparences du lecteur Windows Media, visualisations
- apparences, visualisations
- visualisations, apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673390"
---
# <a name="adding-visualizations"></a><span data-ttu-id="ed5b0-107">Ajout de visualisations</span><span class="sxs-lookup"><span data-stu-id="ed5b0-107">Adding Visualizations</span></span>

<span data-ttu-id="ed5b0-108">Vous pouvez ajouter une fenêtre de visualisation de la même façon que vous avez ajouté une fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="ed5b0-108">You can add a visualization window the same way you added a video window.</span></span> <span data-ttu-id="ed5b0-109">La même apparence peut être utilisée, mais un élément **Effects** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ed5b0-109">The same skin can be used, but an **EFFECTS** element is used.</span></span>

<span data-ttu-id="ed5b0-110">Tout d’abord, vous devez ajouter l’élément **Effects** et lui attribuer un ID et une taille :</span><span class="sxs-lookup"><span data-stu-id="ed5b0-110">First you must add the **EFFECTS** element and give it an ID and size:</span></span>


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



<span data-ttu-id="ed5b0-111">Vous pouvez ensuite assigner les deux boutons une chaîne de code de visualisation précédente et suivante :</span><span class="sxs-lookup"><span data-stu-id="ed5b0-111">Then you can assign the two buttons a previous and next visualization code string:</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



<span data-ttu-id="ed5b0-112">Les couches et les bitmaps étaient les mêmes que celles utilisées dans l’exemple de vidéo, à la différence près que la flèche de lecture a été copiée et retournée horizontalement.</span><span class="sxs-lookup"><span data-stu-id="ed5b0-112">The layers and bitmaps were the same ones used in the video example, except that the play arrow was copied and flipped horizontally.</span></span>

<span data-ttu-id="ed5b0-113">Enfin, un simple élément **Player** avec l’attribut **URL** a été ajouté pour choisir une chanson à lire.</span><span class="sxs-lookup"><span data-stu-id="ed5b0-113">Finally, a simple **PLAYER** element with the **URL** attribute was added to choose a song to play.</span></span>


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



<span data-ttu-id="ed5b0-114">Vous pouvez voir une apparence de visualisation de travail similaire dans la section exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="ed5b0-114">You can see a similar working visualization skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed5b0-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed5b0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed5b0-116">**Guide de création d’apparence**</span><span class="sxs-lookup"><span data-stu-id="ed5b0-116">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




