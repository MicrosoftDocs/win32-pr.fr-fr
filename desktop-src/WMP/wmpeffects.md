---
title: WMPEFFECTS
description: Il s’agit d’effets prédéfinis avec les valeurs par défaut suivantes.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- Lecteur Windows Media WMPEFFECTS
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db3e35143242c5ca7888ffc50feb006f586e68d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540539"
---
# <a name="wmpeffects"></a><span data-ttu-id="c8cb2-104">WMPEFFECTS</span><span class="sxs-lookup"><span data-stu-id="c8cb2-104">WMPEFFECTS</span></span>

<span data-ttu-id="c8cb2-105">Il s’agit d' **effets** prédéfinis avec les valeurs par défaut suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8cb2-105">This is a predefined **EFFECTS** with the following default values.</span></span>

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a><span data-ttu-id="c8cb2-106">Notes</span><span class="sxs-lookup"><span data-stu-id="c8cb2-106">Remarks</span></span>

<span data-ttu-id="c8cb2-107">Cela crée un élément **Effects** qui parcourt les présélections de visualisation lorsque l’utilisateur clique sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8cb2-107">This will create an **EFFECTS** element that will step through the visualization presets when the user clicks the control.</span></span> <span data-ttu-id="c8cb2-108">Elle étend également les visualisations lorsque le joueur est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="c8cb2-108">It will also stretch the visualizations when the player is resized.</span></span>

<span data-ttu-id="c8cb2-109">La présélection de visualisation initiale présentée est celle sélectionnée dans le menu **affichage** sous **visualisations**.</span><span class="sxs-lookup"><span data-stu-id="c8cb2-109">The initial visualization preset shown is the one selected on the **View** menu under **Visualizations**.</span></span> <span data-ttu-id="c8cb2-110">La modification de la sélection dans ce menu entraîne automatiquement la modification de la présélection affichée par cet élément lorsque le joueur est en mode apparence.</span><span class="sxs-lookup"><span data-stu-id="c8cb2-110">Changing the selection on this menu will automatically change the preset displayed by this element when the Player is in skin mode.</span></span> <span data-ttu-id="c8cb2-111">Le menu **affichage** est affiché en mode complet du lecteur ou lorsque l’attribut **View. TitleBar** a la valeur true dans une apparence.</span><span class="sxs-lookup"><span data-stu-id="c8cb2-111">The **View** menu is displayed in the full mode of the Player or when the **VIEW.titleBar** attribute is set to true in a skin.</span></span>

<span data-ttu-id="c8cb2-112">Toutes les propriétés de cet élément **Effects** peuvent être remplacées en les spécifiant explicitement.</span><span class="sxs-lookup"><span data-stu-id="c8cb2-112">All properties of this **EFFECTS** element can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8cb2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8cb2-113">Requirements</span></span>



| <span data-ttu-id="c8cb2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8cb2-114">Requirement</span></span> | <span data-ttu-id="c8cb2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8cb2-115">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="c8cb2-116">Version</span><span class="sxs-lookup"><span data-stu-id="c8cb2-116">Version</span></span><br/> | <span data-ttu-id="c8cb2-117">Lecteur Windows Media 7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c8cb2-117">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8cb2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8cb2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8cb2-119">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="c8cb2-119">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





