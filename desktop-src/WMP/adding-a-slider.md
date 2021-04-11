---
title: Ajout d’un curseur
description: Ajout d’un curseur
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- création d’apparences, de curseurs
- Apparences du lecteur Windows Media, curseurs
- apparences, curseurs
- curseurs dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029464"
---
# <a name="adding-a-slider"></a><span data-ttu-id="89442-107">Ajout d’un curseur</span><span class="sxs-lookup"><span data-stu-id="89442-107">Adding a Slider</span></span>

<span data-ttu-id="89442-108">Vous pouvez ajouter un curseur pour afficher la position actuelle du média et permettre également à l’utilisateur de modifier la position dans le fichier multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="89442-108">You can add a slider to show the current position of the media, and also enable the user to change the position in the current media file.</span></span>

<span data-ttu-id="89442-109">Tout d’abord, vous devez ajouter l’élément **Slider** :</span><span class="sxs-lookup"><span data-stu-id="89442-109">First you must add the **SLIDER** element:</span></span>


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



<span data-ttu-id="89442-110">Cela définit une valeur maximale en fonction de la durée du fichier multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="89442-110">This sets a maximum value based on the duration of the current media file.</span></span> <span data-ttu-id="89442-111">Cela utilise une petite image bitmap de pouce qui est simplement un carré vert de 10 pixels par 10 pixels.</span><span class="sxs-lookup"><span data-stu-id="89442-111">This uses a tiny thumb image bitmap that is just a 10 pixel by 10 pixel green square.</span></span> <span data-ttu-id="89442-112">L’arrière-plan du curseur est rouge et le premier plan est bleu.</span><span class="sxs-lookup"><span data-stu-id="89442-112">The background of the slider will be red and the foreground will be blue.</span></span> <span data-ttu-id="89442-113">Lorsque l’utilisateur fait glisser l’image Thumb vers une nouvelle position et laisse le bouton de la souris enfoncé, le média passe à cette position.</span><span class="sxs-lookup"><span data-stu-id="89442-113">When the user drags the thumb image to a new position and lets go of the mouse button, the media will change to that position.</span></span>

<span data-ttu-id="89442-114">Toutefois, le curseur ne se déplacera pas de lui-même, sauf si vous mesurez la position actuelle avec l’attribut **CurrentPosition \_ OnChange** de l’élément **Controls** , qui est incorporé dans l’élément **Player** .</span><span class="sxs-lookup"><span data-stu-id="89442-114">But the slider will not move by itself unless you measure the current position with the **currentPosition\_onchange** attribute of the **CONTROLS** element, which is embedded in the **PLAYER** element.</span></span>


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



<span data-ttu-id="89442-115">Lorsque la position du média change, cela déclenche un événement qui exécute ensuite la ligne de code qui modifie la valeur du curseur à la position actuelle du média.</span><span class="sxs-lookup"><span data-stu-id="89442-115">When the position of the media changes, this fires an event which then runs the line of code that changes the value of the slider to the current position of the media.</span></span>

<span data-ttu-id="89442-116">Vous pouvez voir une apparence de curseur de travail similaire dans la section exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="89442-116">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89442-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89442-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89442-118">**Guide de création d’apparence**</span><span class="sxs-lookup"><span data-stu-id="89442-118">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




