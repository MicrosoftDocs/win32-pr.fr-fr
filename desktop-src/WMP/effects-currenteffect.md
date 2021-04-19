---
title: EFFECTs. currentEffect
description: L’attribut currentEffect spécifie ou récupère la visualisation actuelle.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520836"
---
# <a name="effectscurrenteffect"></a><span data-ttu-id="f9131-104">EFFECTs. currentEffect</span><span class="sxs-lookup"><span data-stu-id="f9131-104">EFFECTS.currentEffect</span></span>

<span data-ttu-id="f9131-105">L’attribut **currentEffect** spécifie ou récupère la visualisation actuelle.</span><span class="sxs-lookup"><span data-stu-id="f9131-105">The **currentEffect** attribute specifies or retrieves the current visualization.</span></span>

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a><span data-ttu-id="f9131-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f9131-106">Possible Values</span></span>

<span data-ttu-id="f9131-107">Cet attribut est un **objet** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f9131-107">This attribute is a read/write **object**.</span></span> <span data-ttu-id="f9131-108">La valeur par défaut est la première visualisation dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="f9131-108">The default value is the first visualization in the authoring order.</span></span> <span data-ttu-id="f9131-109">Si aucune visualisation n’a été créée dans l’apparence, la valeur par défaut est la première visualisation dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f9131-109">If there are no visualizations authored in the skin, the default is the first visualization in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9131-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f9131-110">Remarks</span></span>

<span data-ttu-id="f9131-111">Vous pouvez utiliser cet objet pour accéder aux visualisations personnalisées que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="f9131-111">You can use this object to access custom visualizations you have created.</span></span> <span data-ttu-id="f9131-112">Par exemple, vous pouvez exposer une propriété par le biais de l’interface **IDispatch** dans votre visualisation.</span><span class="sxs-lookup"><span data-stu-id="f9131-112">For example, you could expose a property through the **IDispatch** interface in your visualization.</span></span> <span data-ttu-id="f9131-113">Vous pouvez ensuite modifier la valeur de la propriété à partir de votre apparence en faisant de votre visualisation l’effet actuel, puis en utilisant l’objet **currentEffect** pour définir une nouvelle valeur pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="f9131-113">You can then change the property value from your skin by making your visualization the current effect, and then using the **currentEffect** object to set a new value for the property.</span></span> <span data-ttu-id="f9131-114">Par exemple, si votre visualisation expose une propriété nommée backgroundColor, le code JScript suivant spécifie une nouvelle valeur :</span><span class="sxs-lookup"><span data-stu-id="f9131-114">For example, if your visualization exposes a property named backgroundColor, the following JScript code specifies a new value:</span></span>


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a><span data-ttu-id="f9131-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9131-115">Requirements</span></span>



| <span data-ttu-id="f9131-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9131-116">Requirement</span></span> | <span data-ttu-id="f9131-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9131-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f9131-118">Version</span><span class="sxs-lookup"><span data-stu-id="f9131-118">Version</span></span><br/> | <span data-ttu-id="f9131-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="f9131-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9131-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9131-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9131-121">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="f9131-121">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="f9131-122">**EFFECTs. currentEffectTitle**</span><span class="sxs-lookup"><span data-stu-id="f9131-122">**EFFECTS.currentEffectTitle**</span></span>](effects-currenteffecttitle.md)
</dt> <dt>

[<span data-ttu-id="f9131-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="f9131-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





