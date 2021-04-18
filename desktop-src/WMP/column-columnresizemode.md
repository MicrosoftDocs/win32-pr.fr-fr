---
title: COLUMN. columnResizeMode
description: L’attribut columnResizeMode spécifie ou récupère le mode de redimensionnement pour cette colonne.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN. columnResizeMode lecteur Windows Media
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540268"
---
# <a name="columncolumnresizemode"></a><span data-ttu-id="6138f-104">COLUMN. columnResizeMode</span><span class="sxs-lookup"><span data-stu-id="6138f-104">COLUMN.columnResizeMode</span></span>

<span data-ttu-id="6138f-105">L’attribut **columnResizeMode** spécifie ou récupère le mode de redimensionnement pour cette colonne.</span><span class="sxs-lookup"><span data-stu-id="6138f-105">The **columnResizeMode** attribute specifies or retrieves the resize mode for this column.</span></span>

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a><span data-ttu-id="6138f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="6138f-106">Possible Values</span></span>

<span data-ttu-id="6138f-107">Cet attribut est une **chaîne** en lecture/écriture contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6138f-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="6138f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6138f-108">Value</span></span>          | <span data-ttu-id="6138f-109">Description</span><span class="sxs-lookup"><span data-stu-id="6138f-109">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6138f-110">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="6138f-110">AutosizeHeader</span></span> | <span data-ttu-id="6138f-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="6138f-111">Default.</span></span> <span data-ttu-id="6138f-112">La colonne est redimensionnée pour s’adapter à toutes les données de la colonne et de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6138f-112">The column resizes to accommodate all data in both the column and the header.</span></span>                         |
| <span data-ttu-id="6138f-113">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="6138f-113">AutosizeData</span></span>   | <span data-ttu-id="6138f-114">La colonne est redimensionnée pour s’adapter à toutes les données de la colonne uniquement.</span><span class="sxs-lookup"><span data-stu-id="6138f-114">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="6138f-115">Fixe</span><span class="sxs-lookup"><span data-stu-id="6138f-115">Fixed</span></span>          | <span data-ttu-id="6138f-116">La colonne a une taille fixe.</span><span class="sxs-lookup"><span data-stu-id="6138f-116">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="6138f-117">S’étire</span><span class="sxs-lookup"><span data-stu-id="6138f-117">Stretches</span></span>      | <span data-ttu-id="6138f-118">La colonne se redimensionne pour utiliser l’espace restant dans le contrôle de **sélection** une fois que toutes les autres colonnes sont redimensionnées.</span><span class="sxs-lookup"><span data-stu-id="6138f-118">The column resizes to use the remaining space in the **PLAYLIST** control after all other columns are resized.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6138f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6138f-119">Requirements</span></span>



| <span data-ttu-id="6138f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6138f-120">Requirement</span></span> | <span data-ttu-id="6138f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6138f-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6138f-122">Version</span><span class="sxs-lookup"><span data-stu-id="6138f-122">Version</span></span><br/> | <span data-ttu-id="6138f-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6138f-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6138f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6138f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6138f-125">**Élément COLUMN**</span><span class="sxs-lookup"><span data-stu-id="6138f-125">**COLUMN Element**</span></span>](column-element.md)
</dt> </dl>

 

 





