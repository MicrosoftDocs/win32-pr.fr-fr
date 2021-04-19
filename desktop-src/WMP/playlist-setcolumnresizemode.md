---
title: PLAYLIST. setColumnResizeMode
description: La méthode setColumnResizeMode spécifie le mode de redimensionnement de la colonne indexée.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Lecteur Windows Media PLAYLIST. setColumnResizeMode
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530049"
---
# <a name="playlistsetcolumnresizemode"></a><span data-ttu-id="24739-104">PLAYLIST. setColumnResizeMode</span><span class="sxs-lookup"><span data-stu-id="24739-104">PLAYLIST.setColumnResizeMode</span></span>

<span data-ttu-id="24739-105">La méthode **setColumnResizeMode** spécifie le mode de redimensionnement de la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="24739-105">The **setColumnResizeMode** method specifies how the indexed column sizes itself.</span></span>

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a><span data-ttu-id="24739-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24739-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24739-107"><span id="column"></span><span id="COLUMN"></span>*chronique*</span><span class="sxs-lookup"><span data-stu-id="24739-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="24739-108">**Nombre** (**long**) indiquant l’index de la colonne à modifier.</span><span class="sxs-lookup"><span data-stu-id="24739-108">**Number** (**long**) indicating the index of the column to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="24739-109"><span id="mode"></span><span id="MODE"></span>*mode*</span><span class="sxs-lookup"><span data-stu-id="24739-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="24739-110">**Chaîne** indiquant le mode de dimensionnement.</span><span class="sxs-lookup"><span data-stu-id="24739-110">**String** indicating the sizing mode.</span></span> <span data-ttu-id="24739-111">Contient l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="24739-111">Contains one of the following values.</span></span>



| <span data-ttu-id="24739-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="24739-112">Value</span></span>          | <span data-ttu-id="24739-113">Description</span><span class="sxs-lookup"><span data-stu-id="24739-113">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24739-114">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="24739-114">AutosizeHeader</span></span> | <span data-ttu-id="24739-115">La colonne est redimensionnée pour s’adapter à toutes les données de la colonne et de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="24739-115">The column resizes to accommodate all data in both the column and the header.</span></span>                                  |
| <span data-ttu-id="24739-116">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="24739-116">AutosizeData</span></span>   | <span data-ttu-id="24739-117">La colonne est redimensionnée pour s’adapter à toutes les données de la colonne uniquement.</span><span class="sxs-lookup"><span data-stu-id="24739-117">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="24739-118">Fixe</span><span class="sxs-lookup"><span data-stu-id="24739-118">Fixed</span></span>          | <span data-ttu-id="24739-119">La colonne a une taille fixe.</span><span class="sxs-lookup"><span data-stu-id="24739-119">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="24739-120">S’étire</span><span class="sxs-lookup"><span data-stu-id="24739-120">Stretches</span></span>      | <span data-ttu-id="24739-121">La colonne se redimensionne pour utiliser l’espace restant dans l’élément de **sélection** une fois que toutes les autres colonnes sont redimensionnées.</span><span class="sxs-lookup"><span data-stu-id="24739-121">The column resizes to use the remaining space in the **PLAYLIST** element after all other columns are resized.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24739-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="24739-122">Return Value</span></span>

<span data-ttu-id="24739-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="24739-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24739-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24739-124">Requirements</span></span>



| <span data-ttu-id="24739-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24739-125">Requirement</span></span> | <span data-ttu-id="24739-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="24739-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="24739-127">Version</span><span class="sxs-lookup"><span data-stu-id="24739-127">Version</span></span><br/> | <span data-ttu-id="24739-128">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="24739-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24739-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24739-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24739-130">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="24739-130">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





