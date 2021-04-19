---
title: EFFECTs. currentEffectType
description: L’attribut currentEffectType spécifie ou récupère le nom du registre de la visualisation actuelle. Ce nom est un ID unique défini par l’auteur de la visualisation.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535898"
---
# <a name="effectscurrenteffecttype"></a><span data-ttu-id="3cc29-105">EFFECTs. currentEffectType</span><span class="sxs-lookup"><span data-stu-id="3cc29-105">EFFECTS.currentEffectType</span></span>

<span data-ttu-id="3cc29-106">L’attribut **currentEffectType** spécifie ou récupère le nom du registre de la visualisation actuelle.</span><span class="sxs-lookup"><span data-stu-id="3cc29-106">The **currentEffectType** attribute specifies or retrieves the registry name of the current visualization.</span></span> <span data-ttu-id="3cc29-107">Ce nom est un ID unique défini par l’auteur de la visualisation.</span><span class="sxs-lookup"><span data-stu-id="3cc29-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a><span data-ttu-id="3cc29-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="3cc29-108">Possible Values</span></span>

<span data-ttu-id="3cc29-109">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3cc29-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc29-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3cc29-110">Remarks</span></span>

<span data-ttu-id="3cc29-111">Vous pouvez utiliser cet attribut au moment de l’exécution pour modifier l’effet actuellement affiché.</span><span class="sxs-lookup"><span data-stu-id="3cc29-111">You can use this attribute at run time to change the currently displayed effect.</span></span> <span data-ttu-id="3cc29-112">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3cc29-112">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="3cc29-113">Utilisez **effectCount** pour récupérer le nombre d’effets enregistrés.</span><span class="sxs-lookup"><span data-stu-id="3cc29-113">Use **effectCount** to retrieve the count of registered effects.</span></span>
2.  <span data-ttu-id="3cc29-114">Dans une boucle, récupérez le nom de chaque effet enregistré à l’aide de **effectType**.</span><span class="sxs-lookup"><span data-stu-id="3cc29-114">In a loop, retrieve the name of each registered effect by using **effectType**.</span></span>
3.  <span data-ttu-id="3cc29-115">Spécifiez l’un des noms que vous avez récupérés pour **currentEffectType** pour définir l’effet actuel.</span><span class="sxs-lookup"><span data-stu-id="3cc29-115">Specify one of the names you retrieved for **currentEffectType** to set the current effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc29-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cc29-116">Requirements</span></span>



| <span data-ttu-id="3cc29-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cc29-117">Requirement</span></span> | <span data-ttu-id="3cc29-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cc29-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3cc29-119">Version</span><span class="sxs-lookup"><span data-stu-id="3cc29-119">Version</span></span><br/> | <span data-ttu-id="3cc29-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3cc29-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cc29-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cc29-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc29-122">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="3cc29-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="3cc29-123">**EFFECTs. currentEffect**</span><span class="sxs-lookup"><span data-stu-id="3cc29-123">**EFFECTS.currentEffect**</span></span>](effects-currenteffect.md)
</dt> <dt>

[<span data-ttu-id="3cc29-124">**EFFECTs. effectCount**</span><span class="sxs-lookup"><span data-stu-id="3cc29-124">**EFFECTS.effectCount**</span></span>](effects-effectcount.md)
</dt> <dt>

[<span data-ttu-id="3cc29-125">**EFFECTs. effectType**</span><span class="sxs-lookup"><span data-stu-id="3cc29-125">**EFFECTS.effectType**</span></span>](effects-effecttype.md)
</dt> </dl>

 

 





