---
title: VIEW. titleBar
description: L’attribut titleBar récupère une valeur indiquant si la barre de titre de la fenêtre est affichée.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW. titleBar lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528070"
---
# <a name="viewtitlebar"></a><span data-ttu-id="b6880-104">VIEW. titleBar</span><span class="sxs-lookup"><span data-stu-id="b6880-104">VIEW.titleBar</span></span>

<span data-ttu-id="b6880-105">L’attribut **TitleBar** récupère une valeur indiquant si la barre de titre de la fenêtre est affichée.</span><span class="sxs-lookup"><span data-stu-id="b6880-105">The **titleBar** attribute retrieves a value indicating whether the window title bar is shown.</span></span>

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a><span data-ttu-id="b6880-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b6880-106">Possible Values</span></span>

<span data-ttu-id="b6880-107">Cet attribut est une **valeur booléenne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b6880-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="b6880-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6880-108">Value</span></span> | <span data-ttu-id="b6880-109">Description</span><span class="sxs-lookup"><span data-stu-id="b6880-109">Description</span></span>                             |
|-------|-----------------------------------------|
| <span data-ttu-id="b6880-110">true</span><span class="sxs-lookup"><span data-stu-id="b6880-110">true</span></span>  | <span data-ttu-id="b6880-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6880-111">Default.</span></span> <span data-ttu-id="b6880-112">La barre de titre de la fenêtre s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b6880-112">The window title bar is shown.</span></span> |
| <span data-ttu-id="b6880-113">false</span><span class="sxs-lookup"><span data-stu-id="b6880-113">false</span></span> | <span data-ttu-id="b6880-114">La barre de titre de la fenêtre n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="b6880-114">The window title bar is not shown.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="b6880-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b6880-115">Remarks</span></span>

<span data-ttu-id="b6880-116">Si la barre de titre est affichée, les boutons zone de contrôle, réduire et fermer s’affichent.</span><span class="sxs-lookup"><span data-stu-id="b6880-116">If the title bar is shown, the control box, minimize, and close buttons will be shown.</span></span> <span data-ttu-id="b6880-117">Le titre de la fenêtre sera le titre de l’élément d' **affichage** .</span><span class="sxs-lookup"><span data-stu-id="b6880-117">The title of the window will be the title of the **VIEW** element.</span></span>

<span data-ttu-id="b6880-118">Si **TitleBar** a la valeur true et que l’utilisateur tente de modifier la valeur de **Video. Zoom**, la modification ne se produit pas, sauf si l’apparence analyse la **Zoom** et prend la mesure appropriée pour se redimensionner.</span><span class="sxs-lookup"><span data-stu-id="b6880-118">If **titleBar** is set to true and the user attempts to change the value of **Video.zoom**, the change will not take place unless the skin monitors **zoom** and takes appropriate action to resize itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6880-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6880-119">Requirements</span></span>



| <span data-ttu-id="b6880-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6880-120">Requirement</span></span> | <span data-ttu-id="b6880-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6880-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b6880-122">Version</span><span class="sxs-lookup"><span data-stu-id="b6880-122">Version</span></span><br/> | <span data-ttu-id="b6880-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b6880-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6880-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6880-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6880-125">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="b6880-125">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="b6880-126">**VIEW. title**</span><span class="sxs-lookup"><span data-stu-id="b6880-126">**VIEW.title**</span></span>](view-title.md)
</dt> <dt>

[<span data-ttu-id="b6880-127">**VIDEO. Zoom**</span><span class="sxs-lookup"><span data-stu-id="b6880-127">**VIDEO.zoom**</span></span>](video-zoom.md)
</dt> </dl>

 

 





