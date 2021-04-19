---
title: EDITBOX. getLineIndex
description: La méthode getLineIndex récupère l’index de caractère du premier caractère sur la ligne avec l’index de ligne spécifié.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- EDITBOX. getLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541783"
---
# <a name="editboxgetlineindex"></a><span data-ttu-id="107e4-104">EDITBOX. getLineIndex</span><span class="sxs-lookup"><span data-stu-id="107e4-104">EDITBOX.getLineIndex</span></span>

<span data-ttu-id="107e4-105">La méthode **getLineIndex** récupère l’index de caractère du premier caractère sur la ligne avec l’index de ligne spécifié.</span><span class="sxs-lookup"><span data-stu-id="107e4-105">The **getLineIndex** method retrieves the character index of the first character on the line with the specified line index.</span></span>

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a><span data-ttu-id="107e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="107e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="107e4-107"><span id="index"></span><span id="INDEX"></span>*évaluer*</span><span class="sxs-lookup"><span data-stu-id="107e4-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="107e4-108">**Nombre** (**long**) contenant l’index de la ligne dont l’index de caractère doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="107e4-108">**Number** (**long**) containing the index of the line whose character index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="107e4-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="107e4-109">Return Value</span></span>

<span data-ttu-id="107e4-110">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="107e4-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="107e4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="107e4-111">Remarks</span></span>

<span data-ttu-id="107e4-112">Si l’index de ligne spécifié est 1, la ligne contenant le point d’insertion est utilisée.</span><span class="sxs-lookup"><span data-stu-id="107e4-112">If the specified line index is  1, the line containing the insertion point is used.</span></span>

<span data-ttu-id="107e4-113">Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.</span><span class="sxs-lookup"><span data-stu-id="107e4-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="107e4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="107e4-114">Requirements</span></span>



| <span data-ttu-id="107e4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="107e4-115">Requirement</span></span> | <span data-ttu-id="107e4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="107e4-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="107e4-117">Version</span><span class="sxs-lookup"><span data-stu-id="107e4-117">Version</span></span><br/> | <span data-ttu-id="107e4-118">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="107e4-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="107e4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="107e4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107e4-120">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="107e4-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="107e4-121">**EDITBOX. getLine**</span><span class="sxs-lookup"><span data-stu-id="107e4-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="107e4-122">**EDITBOX. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="107e4-122">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> </dl>

 

 





