---
title: EFFECTs. effectType
description: La méthode effectType récupère le nom du registre de la visualisation avec l’index de Registre spécifié. Ce nom est un ID unique défini par l’auteur de la visualisation.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTs. effectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528741"
---
# <a name="effectseffecttype"></a><span data-ttu-id="f51ad-105">EFFECTs. effectType</span><span class="sxs-lookup"><span data-stu-id="f51ad-105">EFFECTS.effectType</span></span>

<span data-ttu-id="f51ad-106">La méthode **effectType** récupère le nom du registre de la visualisation avec l’index de Registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="f51ad-106">The **effectType** method retrieves the registry name of the visualization with the specified registry index.</span></span> <span data-ttu-id="f51ad-107">Ce nom est un ID unique défini par l’auteur de la visualisation.</span><span class="sxs-lookup"><span data-stu-id="f51ad-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a><span data-ttu-id="f51ad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f51ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f51ad-109"><span id="index"></span><span id="INDEX"></span>*évaluer*</span><span class="sxs-lookup"><span data-stu-id="f51ad-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="f51ad-110">**Nombre** (**long**) contenant l’index du registre d’une visualisation.</span><span class="sxs-lookup"><span data-stu-id="f51ad-110">**Number** (**long**) containing the registry index of a visualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f51ad-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f51ad-111">Return Value</span></span>

<span data-ttu-id="f51ad-112">Cette méthode retourne une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="f51ad-112">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f51ad-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f51ad-113">Remarks</span></span>

<span data-ttu-id="f51ad-114">Cette méthode est utile pour basculer entre les visualisations dans le script.</span><span class="sxs-lookup"><span data-stu-id="f51ad-114">This method is useful for switching between visualizations in script.</span></span> <span data-ttu-id="f51ad-115">Une interface utilisateur peut afficher le jeu de titres, mais lorsque l’utilisateur en sélectionne un, le script doit utiliser **currentEffectType** pour basculer les visualisations.</span><span class="sxs-lookup"><span data-stu-id="f51ad-115">A user interface could display the set of titles, but when the user selects one, the script must use **currentEffectType** to switch visualizations.</span></span>

## <a name="requirements"></a><span data-ttu-id="f51ad-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f51ad-116">Requirements</span></span>



| <span data-ttu-id="f51ad-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f51ad-117">Requirement</span></span> | <span data-ttu-id="f51ad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f51ad-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f51ad-119">Version</span><span class="sxs-lookup"><span data-stu-id="f51ad-119">Version</span></span><br/> | <span data-ttu-id="f51ad-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f51ad-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f51ad-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f51ad-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51ad-122">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="f51ad-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="f51ad-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="f51ad-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





