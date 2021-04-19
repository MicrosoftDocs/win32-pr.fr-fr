---
title: Slider. foregroundProgress
description: L’attribut foregroundProgress spécifie ou récupère la position actuelle de la barre de progression en premier plan sous la forme d’un pourcentage de la zone de curseur.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Slider. foregroundProgress lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537111"
---
# <a name="sliderforegroundprogress"></a><span data-ttu-id="39bd0-104">Slider. foregroundProgress</span><span class="sxs-lookup"><span data-stu-id="39bd0-104">SLIDER.foregroundProgress</span></span>

<span data-ttu-id="39bd0-105">L’attribut **foregroundProgress** spécifie ou récupère la position actuelle de la barre de progression en premier plan sous la forme d’un pourcentage de la zone de curseur.</span><span class="sxs-lookup"><span data-stu-id="39bd0-105">The **foregroundProgress** attribute specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="39bd0-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="39bd0-106">Possible Values</span></span>

<span data-ttu-id="39bd0-107">Cet attribut est un **nombre** en lecture/écriture (**float**) compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="39bd0-107">This attribute is a read/write **Number** (**float**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="39bd0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="39bd0-108">Remarks</span></span>

<span data-ttu-id="39bd0-109">Cet attribut est utilisé principalement pour suivre la progression du téléchargement d’un fichier multimédia tout en effectuant un suivi simultané de la position de lecture actuelle du fichier à l’aide de l’attribut **value** .</span><span class="sxs-lookup"><span data-stu-id="39bd0-109">This attribute is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span> <span data-ttu-id="39bd0-110">La position du curseur de défilement est restreinte à la zone de la progression du premier plan.</span><span class="sxs-lookup"><span data-stu-id="39bd0-110">The position of the slider thumb is constrained to the area of the foreground progress.</span></span> <span data-ttu-id="39bd0-111">Cela permet d’effectuer une recherche interactive uniquement dans la partie disponible d’un fichier de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="39bd0-111">This allows interactive seeking to take place only within the available portion of a downloading file.</span></span>

<span data-ttu-id="39bd0-112">Pour utiliser cette fonctionnalité, l’attribut **useForegroundProgress** doit avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="39bd0-112">To use this functionality, the **useForegroundProgress** attribute must be set to true.</span></span>

## <a name="examples"></a><span data-ttu-id="39bd0-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="39bd0-113">Examples</span></span>


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a><span data-ttu-id="39bd0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39bd0-114">Requirements</span></span>



| <span data-ttu-id="39bd0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39bd0-115">Requirement</span></span> | <span data-ttu-id="39bd0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="39bd0-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="39bd0-117">Version</span><span class="sxs-lookup"><span data-stu-id="39bd0-117">Version</span></span><br/> | <span data-ttu-id="39bd0-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="39bd0-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39bd0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39bd0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bd0-120">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="39bd0-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="39bd0-121">**Slider. min.**</span><span class="sxs-lookup"><span data-stu-id="39bd0-121">**SLIDER.min**</span></span>](slider-min.md)
</dt> <dt>

[<span data-ttu-id="39bd0-122">**Slider. Max**</span><span class="sxs-lookup"><span data-stu-id="39bd0-122">**SLIDER.max**</span></span>](slider-max.md)
</dt> <dt>

[<span data-ttu-id="39bd0-123">**Slider. useForegroundProgress**</span><span class="sxs-lookup"><span data-stu-id="39bd0-123">**SLIDER.useForegroundProgress**</span></span>](slider-useforegroundprogress.md)
</dt> <dt>

[<span data-ttu-id="39bd0-124">**Slider. Value**</span><span class="sxs-lookup"><span data-stu-id="39bd0-124">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





