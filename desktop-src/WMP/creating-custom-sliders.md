---
title: Création de curseurs personnalisés
description: Création de curseurs personnalisés
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- création d’apparences, de curseurs
- Apparences du lecteur Windows Media, curseurs
- apparences, curseurs
- curseurs dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507331"
---
# <a name="creating-custom-sliders"></a><span data-ttu-id="0c114-107">Création de curseurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="0c114-107">Creating Custom Sliders</span></span>

<span data-ttu-id="0c114-108">Vous pouvez créer des curseurs personnalisés dans n’importe quelle forme de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0c114-108">You can create custom sliders in any shape you want.</span></span> <span data-ttu-id="0c114-109">Pour cet exemple, un simple bandeau est choisi, mais la forme réelle peut être n’importe quoi.</span><span class="sxs-lookup"><span data-stu-id="0c114-109">For this example, a simple strip is chosen, but the actual shape can be anything.</span></span> <span data-ttu-id="0c114-110">Voici le code de l’élément **CUSTOMSLIDER** :</span><span class="sxs-lookup"><span data-stu-id="0c114-110">Here is the code for the **CUSTOMSLIDER** element:</span></span>


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



<span data-ttu-id="0c114-111">Cela permet de définir une valeur initiale pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="0c114-111">This sets up an initial value for the slider.</span></span> <span data-ttu-id="0c114-112">Deux nouvelles bitmaps sont introduites.</span><span class="sxs-lookup"><span data-stu-id="0c114-112">Two new bitmaps are introduced.</span></span> <span data-ttu-id="0c114-113">L’une est la bitmap en nuances de gris (slider.bmp) qui définit les valeurs qui seront utilisées lorsque vous cliquez sur, et l’autre (slider.bmp) qui détermine l’image qui sera affichée lorsqu’un clic est effectué sur une partie particulière de la nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="0c114-113">One is the grayscale bitmap (slider.bmp) that defines which values will be used when clicked on, and the other (slider.bmp) that determines which image will be shown when a particular portion of the grayscale is clicked on.</span></span>

<span data-ttu-id="0c114-114">La valeur initiale est déterminée par l’écoute du volume avec wmpprop, puis le volume peut être modifié lorsque l’utilisateur clique sur une partie du curseur qui déclenche une modification de la valeur.</span><span class="sxs-lookup"><span data-stu-id="0c114-114">The initial value is determined by listening to the volume with wmpprop and then the volume can be changed when the user clicks on a portion of the slider that triggers a change in value.</span></span>

<span data-ttu-id="0c114-115">Vous pouvez voir une apparence de curseur de travail similaire dans la section exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="0c114-115">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c114-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c114-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c114-117">**Guide de création d’apparence**</span><span class="sxs-lookup"><span data-stu-id="0c114-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




