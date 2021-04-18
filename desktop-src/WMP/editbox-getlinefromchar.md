---
title: EDITBOX. getLineFromChar
description: La méthode getLineFromChar récupère l’index de ligne pour l’index de caractère spécifié.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EDITBOX. getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526496"
---
# <a name="editboxgetlinefromchar"></a><span data-ttu-id="61dc7-104">EDITBOX. getLineFromChar</span><span class="sxs-lookup"><span data-stu-id="61dc7-104">EDITBOX.getLineFromChar</span></span>

<span data-ttu-id="61dc7-105">La méthode **getLineFromChar** récupère l’index de ligne pour l’index de caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="61dc7-105">The **getLineFromChar** method retrieves the line index for the specified character index.</span></span>

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a><span data-ttu-id="61dc7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61dc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61dc7-107"><span id="index"></span><span id="INDEX"></span>*évaluer*</span><span class="sxs-lookup"><span data-stu-id="61dc7-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="61dc7-108">**Nombre** (**long**) contenant l’index du caractère dont l’index de ligne doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="61dc7-108">**Number** (**long**) containing the index of the character whose line index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61dc7-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="61dc7-109">Return Value</span></span>

<span data-ttu-id="61dc7-110">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="61dc7-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="61dc7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="61dc7-111">Remarks</span></span>

<span data-ttu-id="61dc7-112">Si la position de caractère spécifiée est 1, cette méthode récupère l’index de ligne de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="61dc7-112">If the specified character position is  1, this method retrieves the line index of the current line.</span></span>

<span data-ttu-id="61dc7-113">Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.</span><span class="sxs-lookup"><span data-stu-id="61dc7-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="61dc7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61dc7-114">Requirements</span></span>



| <span data-ttu-id="61dc7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61dc7-115">Requirement</span></span> | <span data-ttu-id="61dc7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="61dc7-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="61dc7-117">Version</span><span class="sxs-lookup"><span data-stu-id="61dc7-117">Version</span></span><br/> | <span data-ttu-id="61dc7-118">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="61dc7-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61dc7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61dc7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61dc7-120">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="61dc7-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="61dc7-121">**EDITBOX. getLine**</span><span class="sxs-lookup"><span data-stu-id="61dc7-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="61dc7-122">**EDITBOX. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="61dc7-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





