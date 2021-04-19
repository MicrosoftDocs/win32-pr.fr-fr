---
title: EQUALIZERSETTINGS.gainLevels
description: L’attribut gainLevels spécifie ou récupère le niveau de gain de la bande correspondant à l’index fourni.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. gainLevels
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523938"
---
# <a name="equalizersettingsgainlevels"></a><span data-ttu-id="3c8f8-104">EQUALIZERSETTINGS.gainLevels</span><span class="sxs-lookup"><span data-stu-id="3c8f8-104">EQUALIZERSETTINGS.gainLevels</span></span>

<span data-ttu-id="3c8f8-105">L’attribut **gainLevels** spécifie ou récupère le niveau de gain de la bande correspondant à l’index fourni.</span><span class="sxs-lookup"><span data-stu-id="3c8f8-105">The **gainLevels** attribute specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a><span data-ttu-id="3c8f8-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="3c8f8-106">Possible Values</span></span>

<span data-ttu-id="3c8f8-107">Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20.</span><span class="sxs-lookup"><span data-stu-id="3c8f8-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c8f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c8f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8f8-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span><span class="sxs-lookup"><span data-stu-id="3c8f8-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span></span>
</dt> <dd>

<span data-ttu-id="3c8f8-110">**Nombre**(**long**) entre 1 et 10 indiquant l’index de la bande.</span><span class="sxs-lookup"><span data-stu-id="3c8f8-110">**Number**(**long**) between 1 and 10 indicating the index of the band.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c8f8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3c8f8-111">Remarks</span></span>

<span data-ttu-id="3c8f8-112">Cet attribut accepte un paramètre, mais sa valeur est spécifiée dans le code de script de la même façon que les autres valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="3c8f8-112">This attribute takes a parameter, but its value is specified in script code the same way as other attribute values.</span></span> <span data-ttu-id="3c8f8-113">Elle ne peut pas être spécifiée dans l’élément EQUALIZERSETTINGS et ne peut pas être utilisée avec l’attribut Listening **wmpprop** .</span><span class="sxs-lookup"><span data-stu-id="3c8f8-113">It cannot be specified in the EQUALIZERSETTINGS element, nor can it be used with the **wmpprop** listening attribute.</span></span> <span data-ttu-id="3c8f8-114">Au lieu de cela, les attributs de niveau de gain numéroté sont fournis pour ces situations.</span><span class="sxs-lookup"><span data-stu-id="3c8f8-114">Instead, the numbered gain level attributes are provided for these situations.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8f8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c8f8-115">Requirements</span></span>



| <span data-ttu-id="3c8f8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c8f8-116">Requirement</span></span> | <span data-ttu-id="3c8f8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c8f8-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3c8f8-118">Version</span><span class="sxs-lookup"><span data-stu-id="3c8f8-118">Version</span></span><br/> | <span data-ttu-id="3c8f8-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3c8f8-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c8f8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c8f8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8f8-121">**Élément EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="3c8f8-121">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="3c8f8-122">**Écoute des attributs**</span><span class="sxs-lookup"><span data-stu-id="3c8f8-122">**Listening Attributes**</span></span>](listening-attributes.md)
</dt> </dl>

 

 





