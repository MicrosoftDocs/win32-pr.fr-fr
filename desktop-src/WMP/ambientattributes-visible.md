---
title: AmbientAttributes. visible
description: L’attribut visible spécifie ou récupère la visibilité du contrôle.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Lecteur Windows Media AmbientAttributes. visible
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526400"
---
# <a name="ambientattributesvisible"></a><span data-ttu-id="aa89f-104">AmbientAttributes. visible</span><span class="sxs-lookup"><span data-stu-id="aa89f-104">AmbientAttributes.visible</span></span>

<span data-ttu-id="aa89f-105">L’attribut **visible** spécifie ou récupère la visibilité du contrôle.</span><span class="sxs-lookup"><span data-stu-id="aa89f-105">The **visible** attribute specifies or retrieves the visibility for the control.</span></span>

``` syntax
        elementID.visible
```

## <a name="possible-values"></a><span data-ttu-id="aa89f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="aa89f-106">Possible Values</span></span>

<span data-ttu-id="aa89f-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="aa89f-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="aa89f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa89f-108">Value</span></span> | <span data-ttu-id="aa89f-109">Description</span><span class="sxs-lookup"><span data-stu-id="aa89f-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="aa89f-110">true</span><span class="sxs-lookup"><span data-stu-id="aa89f-110">true</span></span>  | <span data-ttu-id="aa89f-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="aa89f-111">Default.</span></span> <span data-ttu-id="aa89f-112">Le contrôle est visible.</span><span class="sxs-lookup"><span data-stu-id="aa89f-112">The control is visible.</span></span> |
| <span data-ttu-id="aa89f-113">false</span><span class="sxs-lookup"><span data-stu-id="aa89f-113">false</span></span> | <span data-ttu-id="aa89f-114">Le contrôle n'est pas visible.</span><span class="sxs-lookup"><span data-stu-id="aa89f-114">The control is not visible.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="aa89f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="aa89f-115">Remarks</span></span>

<span data-ttu-id="aa89f-116">Cet attribut est utile pour masquer des contrôles, par exemple lors du remplacement d’un bouton de pause pour un bouton de lecture.</span><span class="sxs-lookup"><span data-stu-id="aa89f-116">This attribute is useful for hiding controls, for example when swapping a pause button for a play button.</span></span>

<span data-ttu-id="aa89f-117">Si la valeur est false, le contrôle n’est pas visible et les événements de clic sont passés au contrôle situé derrière lui.</span><span class="sxs-lookup"><span data-stu-id="aa89f-117">If the value is false, the control is not visible and click events are passed to the control behind it.</span></span> <span data-ttu-id="aa89f-118">Si la valeur est true, le contrôle est visible et reçoit l’événement Click lui-même.</span><span class="sxs-lookup"><span data-stu-id="aa89f-118">If the value is true, the control is visible and receives the click event itself.</span></span>

<span data-ttu-id="aa89f-119">La valeur par défaut de l’élément **automenu** est false.</span><span class="sxs-lookup"><span data-stu-id="aa89f-119">The default value for the **AUTOMENU** element is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa89f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa89f-120">Requirements</span></span>



| <span data-ttu-id="aa89f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa89f-121">Requirement</span></span> | <span data-ttu-id="aa89f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa89f-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="aa89f-123">Version</span><span class="sxs-lookup"><span data-stu-id="aa89f-123">Version</span></span><br/> | <span data-ttu-id="aa89f-124">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="aa89f-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa89f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa89f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa89f-126">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="aa89f-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





