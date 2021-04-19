---
title: SEEKSLIDER
description: Il s’agit d’un curseur prédéfini avec les valeurs par défaut suivantes. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- Lecteur Windows Media SEEKSLIDER
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528783"
---
# <a name="seekslider"></a><span data-ttu-id="5b045-105">SEEKSLIDER</span><span class="sxs-lookup"><span data-stu-id="5b045-105">SEEKSLIDER</span></span>

<span data-ttu-id="5b045-106">Il s’agit d’un **curseur** prédéfini avec les valeurs par défaut suivantes.</span><span class="sxs-lookup"><span data-stu-id="5b045-106">This is a predefined **SLIDER** with the following default values.</span></span>

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a><span data-ttu-id="5b045-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5b045-107">Remarks</span></span>

<span data-ttu-id="5b045-108">Cela crée un contrôle **Slider** qui recherche le fichier multimédia à n’importe quelle position.</span><span class="sxs-lookup"><span data-stu-id="5b045-108">This creates a **SLIDER** control that seeks the media file to any position.</span></span> <span data-ttu-id="5b045-109">Les info-bulles sont localisées.</span><span class="sxs-lookup"><span data-stu-id="5b045-109">The ToolTips are localized.</span></span> <span data-ttu-id="5b045-110">Toutes les propriétés de ce **curseur** peuvent être remplacées en les spécifiant explicitement.</span><span class="sxs-lookup"><span data-stu-id="5b045-110">All properties of this **SLIDER** can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b045-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b045-111">Requirements</span></span>



| <span data-ttu-id="5b045-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b045-112">Requirement</span></span> | <span data-ttu-id="5b045-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b045-113">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="5b045-114">Version</span><span class="sxs-lookup"><span data-stu-id="5b045-114">Version</span></span><br/> | <span data-ttu-id="5b045-115">Lecteur Windows Media 7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5b045-115">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b045-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b045-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b045-117">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="5b045-117">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





