---
title: CUSTOMSLIDER.positionImage
description: L’attribut positionImage spécifie ou récupère l’image interactive utilisée pour déterminer l’image de position à partir du fichier image à afficher.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- Lecteur Windows Media CUSTOMSLIDER. positionImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532487"
---
# <a name="customsliderpositionimage"></a><span data-ttu-id="740f5-104">CUSTOMSLIDER.positionImage</span><span class="sxs-lookup"><span data-stu-id="740f5-104">CUSTOMSLIDER.positionImage</span></span>

<span data-ttu-id="740f5-105">L’attribut **positionImage** spécifie ou récupère l’image interactive utilisée pour déterminer l’image de position à partir du fichier image à afficher.</span><span class="sxs-lookup"><span data-stu-id="740f5-105">The **positionImage** attribute specifies or retrieves the image map used to determine which position image from the image file to display.</span></span>

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a><span data-ttu-id="740f5-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="740f5-106">Possible Values</span></span>

<span data-ttu-id="740f5-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="740f5-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="740f5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="740f5-108">Remarks</span></span>

<span data-ttu-id="740f5-109">Cet attribut est obligatoire et doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="740f5-109">This attribute is required and must be specified.</span></span>

<span data-ttu-id="740f5-110">Le **positionImage** n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="740f5-110">The **positionImage** is not displayed.</span></span> <span data-ttu-id="740f5-111">Au lieu de cela, elle sert de carte qui définit les zones interactives de l’image affichée.</span><span class="sxs-lookup"><span data-stu-id="740f5-111">Instead, it serves as a map defining the clickable regions of the displayed image.</span></span> <span data-ttu-id="740f5-112">L’image affichée est l’une des sous-images du fichier image et représente l’état réel du curseur.</span><span class="sxs-lookup"><span data-stu-id="740f5-112">The displayed image is one of the sub-images of the image file and represents the actual state of the slider.</span></span> <span data-ttu-id="740f5-113">Le **positionImage** comprend un nombre de régions de l’échelle gris égal au nombre de ces sous-images.</span><span class="sxs-lookup"><span data-stu-id="740f5-113">The **positionImage** includes a number of gray scale regions equal to the number of these sub-images.</span></span> <span data-ttu-id="740f5-114">Les sous-images doivent avoir les mêmes dimensions que le **positionImage** ou le curseur personnalisé ne fonctionnera pas correctement.</span><span class="sxs-lookup"><span data-stu-id="740f5-114">The sub-images must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span>

<span data-ttu-id="740f5-115">Vous ne pouvez pas cliquer sur une région qui n’est pas en gris.</span><span class="sxs-lookup"><span data-stu-id="740f5-115">Any region that is not in gray scale will not be clickable.</span></span> <span data-ttu-id="740f5-116">Les régions intercliquables doivent être définies sur des valeurs de couleur qui s’adaptent uniformément à la gamme de nuances de gris du noir au blanc, la première région étant le noir pur et la dernière région étant un blanc pur.</span><span class="sxs-lookup"><span data-stu-id="740f5-116">The clickable regions should be set to color values that range evenly across the gray scale spectrum from black to white, with the first region being pure black and the last region being pure white.</span></span> <span data-ttu-id="740f5-117">Les valeurs de couleur de chaque région successive doivent être incrémentées d’une valeur égale à 255 divisée par le nombre total de régions moins un, en arrondissant au nombre entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="740f5-117">The color values of each successive region should be incremented by a value equal to 255 divided by the total number of regions minus one, rounding to the nearest whole number.</span></span>

<span data-ttu-id="740f5-118">Par exemple, s’il existe six régions, l’incrément est de 51 (255 divisé par 5) et les six valeurs de mise à l’échelle de gris sont 0, 51, 102, 153, 204 et 255.</span><span class="sxs-lookup"><span data-stu-id="740f5-118">For example, if there are six regions, the increment would be 51 (255 divided by 5), and the six gray scale values would be 0, 51, 102, 153, 204, and 255.</span></span> <span data-ttu-id="740f5-119">Les valeurs de couleur hexadécimale pour les six régions seraient \# 000000, \# 333333, \# 666666, \# 999999, \# cccccc et \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="740f5-119">The hexadecimal color values for the six regions would then be \#000000, \#333333, \#666666, \#999999, \#CCCCCC, and \#FFFFFF.</span></span>

<span data-ttu-id="740f5-120">De cette façon, les régions auront une séquence dictée par leurs valeurs de couleur de l’échelle grise, et cette séquence correspondra à la séquence de sous-images dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="740f5-120">In this way, the regions will have a sequence dictated by their gray scale color values, and this sequence will correspond to the sequence of sub-images in the image file.</span></span> <span data-ttu-id="740f5-121">Quand l’utilisateur clique sur l’une des régions, la sous-image correspondante est affichée et la **valeur** du curseur personnalisé est mise à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="740f5-121">When one of the regions is clicked, the corresponding sub-image is shown and the **value** of the custom slider is updated accordingly.</span></span>

<span data-ttu-id="740f5-122">Les types de fichiers image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).</span><span class="sxs-lookup"><span data-stu-id="740f5-122">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="740f5-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="740f5-123">Examples</span></span>

<span data-ttu-id="740f5-124">Voici un exemple de curseur personnalisé **positionImage**.</span><span class="sxs-lookup"><span data-stu-id="740f5-124">The following is an example of a custom slider **positionImage**.</span></span> <span data-ttu-id="740f5-125">L’image correspondante est présentée dans la section exemple de la propriété **image** .</span><span class="sxs-lookup"><span data-stu-id="740f5-125">The corresponding image is shown in the example section of the **image** property.</span></span>

![exemple de graphique positionimage](images/dialmap.png)

<span data-ttu-id="740f5-127">Le code suivant illustre l’utilisation des attributs **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="740f5-127">The following code illustrates the use of **CUSTOMSLIDER** attributes.</span></span>


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

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
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="740f5-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="740f5-128">Requirements</span></span>



| <span data-ttu-id="740f5-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="740f5-129">Requirement</span></span> | <span data-ttu-id="740f5-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="740f5-130">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="740f5-131">Version</span><span class="sxs-lookup"><span data-stu-id="740f5-131">Version</span></span><br/> | <span data-ttu-id="740f5-132">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="740f5-132">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="740f5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="740f5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740f5-134">**Élément CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="740f5-134">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="740f5-135">**CUSTOMSLIDER. image**</span><span class="sxs-lookup"><span data-stu-id="740f5-135">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





