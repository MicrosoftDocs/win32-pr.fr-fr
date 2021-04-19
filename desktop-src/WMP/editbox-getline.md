---
title: EDITBOX. getLine
description: La méthode getLine récupère le texte de la ligne avec l’index spécifié.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- EDITBOX. getLine Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525154"
---
# <a name="editboxgetline"></a><span data-ttu-id="f1bd4-104">EDITBOX. getLine</span><span class="sxs-lookup"><span data-stu-id="f1bd4-104">EDITBOX.getLine</span></span>

<span data-ttu-id="f1bd4-105">La méthode **getline** récupère le texte de la ligne avec l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-105">The **getLine** method retrieves the text for the line with the specified index.</span></span>

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a><span data-ttu-id="f1bd4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1bd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1bd4-107"><span id="index"></span><span id="INDEX"></span>*évaluer*</span><span class="sxs-lookup"><span data-stu-id="f1bd4-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="f1bd4-108">**Nombre** (**long**) contenant l’index de la ligne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1bd4-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1bd4-109">Return Value</span></span>

<span data-ttu-id="f1bd4-110">Cette méthode retourne une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1bd4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f1bd4-111">Remarks</span></span>

<span data-ttu-id="f1bd4-112">Si l’index n’est pas valide, une chaîne vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-112">If the index is not valid, an empty string is returned.</span></span> <span data-ttu-id="f1bd4-113">Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1bd4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1bd4-114">Requirements</span></span>



| <span data-ttu-id="f1bd4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1bd4-115">Requirement</span></span> | <span data-ttu-id="f1bd4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1bd4-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="f1bd4-117">Version</span><span class="sxs-lookup"><span data-stu-id="f1bd4-117">Version</span></span><br/> | <span data-ttu-id="f1bd4-118">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f1bd4-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1bd4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1bd4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1bd4-120">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="f1bd4-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="f1bd4-121">**EDITBOX. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="f1bd4-121">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="f1bd4-122">**EDITBOX. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="f1bd4-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





