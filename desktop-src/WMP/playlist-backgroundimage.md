---
title: PLAYLIST. backgroundImage
description: L’attribut backgroundImage spécifie ou récupère l’image d’arrière-plan.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST. backgroundImage lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545543"
---
# <a name="playlistbackgroundimage"></a><span data-ttu-id="b5419-104">PLAYLIST. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="b5419-104">PLAYLIST.backgroundImage</span></span>

<span data-ttu-id="b5419-105">L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b5419-105">The **backgroundImage** attribute specifies or retrieves the background image.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="b5419-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b5419-106">Possible Values</span></span>

<span data-ttu-id="b5419-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="b5419-107">This attribute is a read/write **String** containing the name of an image file.</span></span> <span data-ttu-id="b5419-108">Il n'a aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b5419-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5419-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b5419-109">Remarks</span></span>

<span data-ttu-id="b5419-110">Si la hauteur et la largeur de l’image sont inférieures à la hauteur et à la largeur de l’élément de **sélection** , l’image est affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="b5419-110">If the image height and width are smaller than the height and width of the **PLAYLIST** element, the image is tiled.</span></span> <span data-ttu-id="b5419-111">Les formats pris en charge sont BMP, JPG, GIF et PNG.</span><span class="sxs-lookup"><span data-stu-id="b5419-111">The supported formats are BMP, JPG, GIF and PNG.</span></span>

<span data-ttu-id="b5419-112">Si vous spécifiez la valeur « gradient » pour l’image d’arrière-plan, l’arrière-plan de la sélection s’affiche sous la forme d’un dégradé de couleur.</span><span class="sxs-lookup"><span data-stu-id="b5419-112">Specifying a value of "gradient" for the background image causes the background of the playlist to display as a color gradient.</span></span> <span data-ttu-id="b5419-113">Cela signifie que la couleur d’arrière-plan transite graduellement entre les valeurs [playlist. BackgroundColor](playlist-backgroundcolor.md) (en haut de l’arrière-plan) et [playlist. statusColor](playlist-statuscolor.md) .</span><span class="sxs-lookup"><span data-stu-id="b5419-113">This means the background color gradually transitions between the [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (at the top of the background) and [PLAYLIST.statusColor](playlist-statuscolor.md) values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5419-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5419-114">Requirements</span></span>



| <span data-ttu-id="b5419-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5419-115">Requirement</span></span> | <span data-ttu-id="b5419-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5419-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5419-117">Version</span><span class="sxs-lookup"><span data-stu-id="b5419-117">Version</span></span><br/> | <span data-ttu-id="b5419-118">Lecteur Windows Media version 7,0 ou ultérieure, lecteur Windows Media 10 pour la fonctionnalité de dégradé</span><span class="sxs-lookup"><span data-stu-id="b5419-118">Windows Media Player version 7.0 or later, Windows Media Player 10 for the gradient feature</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5419-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5419-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5419-120">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="b5419-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





