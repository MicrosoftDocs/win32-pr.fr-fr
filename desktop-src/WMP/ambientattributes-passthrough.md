---
title: AmbientAttributes. passThrough
description: L’attribut passThrough spécifie ou récupère une valeur indiquant si le contrôle passera tous les événements de souris au contrôle situé sous celui-ci.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Lecteur Windows Media AmbientAttributes. passThrough
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545395"
---
# <a name="ambientattributespassthrough"></a><span data-ttu-id="c2d86-104">AmbientAttributes. passThrough</span><span class="sxs-lookup"><span data-stu-id="c2d86-104">AmbientAttributes.passThrough</span></span>

<span data-ttu-id="c2d86-105">L’attribut **passThrough** spécifie ou récupère une valeur indiquant si le contrôle passera tous les événements de souris au contrôle situé sous celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c2d86-105">The **passThrough** attribute specifies or retrieves a value indicating whether the control will pass all mouse events through to the control under it.</span></span>

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a><span data-ttu-id="c2d86-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c2d86-106">Possible Values</span></span>

<span data-ttu-id="c2d86-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c2d86-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c2d86-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d86-108">Value</span></span> | <span data-ttu-id="c2d86-109">Description</span><span class="sxs-lookup"><span data-stu-id="c2d86-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="c2d86-110">true</span><span class="sxs-lookup"><span data-stu-id="c2d86-110">true</span></span>  | <span data-ttu-id="c2d86-111">Le contrôle passe des événements au contrôle situé sous celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c2d86-111">Control passes events through to the control under it.</span></span> |
| <span data-ttu-id="c2d86-112">false</span><span class="sxs-lookup"><span data-stu-id="c2d86-112">false</span></span> | <span data-ttu-id="c2d86-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2d86-113">Default.</span></span> <span data-ttu-id="c2d86-114">Le contrôle ne passe pas d’événements via.</span><span class="sxs-lookup"><span data-stu-id="c2d86-114">Control does not pass events through.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="c2d86-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c2d86-115">Remarks</span></span>

<span data-ttu-id="c2d86-116">Cet attribut est utile si, par exemple, un contrôle de texte se trouve au-dessus d’un contrôle de bouton uniquement pour fournir une étiquette.</span><span class="sxs-lookup"><span data-stu-id="c2d86-116">This attribute is useful if, for example, a text control sits on top of a button control only to provide labeling.</span></span> <span data-ttu-id="c2d86-117">Dans ce cas, les clics sur le contrôle de texte doivent être passés au contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="c2d86-117">In this case, clicks on the text control must be passed through to the button control.</span></span>

<span data-ttu-id="c2d86-118">L’attribut **passThrough** n’est pas pris en charge par les éléments **VIEW**, **subview** et **playlist** .</span><span class="sxs-lookup"><span data-stu-id="c2d86-118">The **passThrough** attribute is not supported by the **VIEW**, **SUBVIEW**, and **PLAYLIST** elements.</span></span> <span data-ttu-id="c2d86-119">Elle ne fonctionnera pas avec l’élément **vidéo** si vous utilisez la *vidéo*. **sans fenêtre** est défini sur false, ni avec l’élément **Effects** si *Effects*. **Windowed** a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="c2d86-119">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d86-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2d86-120">Requirements</span></span>



| <span data-ttu-id="c2d86-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2d86-121">Requirement</span></span> | <span data-ttu-id="c2d86-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d86-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c2d86-123">Version</span><span class="sxs-lookup"><span data-stu-id="c2d86-123">Version</span></span><br/> | <span data-ttu-id="c2d86-124">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c2d86-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2d86-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2d86-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d86-126">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="c2d86-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





