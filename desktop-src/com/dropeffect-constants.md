---
title: Constantes DROPEFFECT (OleIdl. h)
description: Représente des informations sur les effets d’une opération de glisser-déplacer.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509750"
---
# <a name="dropeffect-constants"></a><span data-ttu-id="bebbd-103">Constantes DROPEFFECT</span><span class="sxs-lookup"><span data-stu-id="bebbd-103">DROPEFFECT Constants</span></span>

<span data-ttu-id="bebbd-104">Représente des informations sur les effets d’une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="bebbd-104">Represents information about the effects of a drag-and-drop operation.</span></span> <span data-ttu-id="bebbd-105">La fonction [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) et la plupart des méthodes dans [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) et [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) utilisent les valeurs de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="bebbd-105">The [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function and many of the methods in the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) use the values of this enumeration.</span></span>



| <span data-ttu-id="bebbd-106">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="bebbd-106">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="bebbd-107">Description</span><span class="sxs-lookup"><span data-stu-id="bebbd-107">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <span data-ttu-id="bebbd-108"><dt>**DROPEFFECT \_ AUCUN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bebbd-108"><dt>**DROPEFFECT\_NONE**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="bebbd-109">La cible de dépôt ne peut pas accepter les données.</span><span class="sxs-lookup"><span data-stu-id="bebbd-109">Drop target cannot accept the data.</span></span><br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <span data-ttu-id="bebbd-110"><dt>**DROPEFFECT \_ COPIE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bebbd-110"><dt>**DROPEFFECT\_COPY**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="bebbd-111">Déposer les résultats dans une copie.</span><span class="sxs-lookup"><span data-stu-id="bebbd-111">Drop results in a copy.</span></span> <span data-ttu-id="bebbd-112">Les données d’origine ne sont pas touchées par la source de glissement.</span><span class="sxs-lookup"><span data-stu-id="bebbd-112">The original data is untouched by the drag source.</span></span><br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <span data-ttu-id="bebbd-113"><dt>**DROPEFFECT \_ DÉPLACER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bebbd-113"><dt>**DROPEFFECT\_MOVE**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="bebbd-114">La source de glissement doit supprimer les données.</span><span class="sxs-lookup"><span data-stu-id="bebbd-114">Drag source should remove the data.</span></span> <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <span data-ttu-id="bebbd-115"><dt>**DROPEFFECT \_ LIEN**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bebbd-115"><dt>**DROPEFFECT\_LINK**</dt> <dt>4</dt></span></span> </dl>                | <span data-ttu-id="bebbd-116">La source de glissement doit créer un lien vers les données d’origine.</span><span class="sxs-lookup"><span data-stu-id="bebbd-116">Drag source should create a link to the original data.</span></span><br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <span data-ttu-id="bebbd-117"><dt>**DROPEFFECT \_ SCROLL**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="bebbd-117"><dt>**DROPEFFECT\_SCROLL**</dt> <dt>0x80000000</dt></span></span> </dl> | <span data-ttu-id="bebbd-118">Le défilement est sur le début ou se produit actuellement dans la cible.</span><span class="sxs-lookup"><span data-stu-id="bebbd-118">Scrolling is about to start or is currently occurring in the target.</span></span> <span data-ttu-id="bebbd-119">Cette valeur est utilisée en plus des autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="bebbd-119">This value is used in addition to the other values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bebbd-120">Notes</span><span class="sxs-lookup"><span data-stu-id="bebbd-120">Remarks</span></span>

<span data-ttu-id="bebbd-121">Votre application doit toujours masquer les valeurs de l’énumération **DROPEFFECT** pour garantir la compatibilité avec les futures implémentations.</span><span class="sxs-lookup"><span data-stu-id="bebbd-121">Your application should always mask values from the **DROPEFFECT** enumeration to ensure compatibility with future implementations.</span></span> <span data-ttu-id="bebbd-122">Actuellement, seules certaines positions dans une valeur **DROPEFFECT** ont une signification.</span><span class="sxs-lookup"><span data-stu-id="bebbd-122">Presently, only some of the positions in a **DROPEFFECT** value have meaning.</span></span> <span data-ttu-id="bebbd-123">À l’avenir, d’autres interprétations pour le service bits seront ajoutées.</span><span class="sxs-lookup"><span data-stu-id="bebbd-123">In the future, more interpretations for the bits will be added.</span></span> <span data-ttu-id="bebbd-124">Les sources de glissement et les cibles de dépôt doivent masquer soigneusement ces valeurs avant la comparaison.</span><span class="sxs-lookup"><span data-stu-id="bebbd-124">Drag sources and drop targets should carefully mask these values appropriately before comparing.</span></span> <span data-ttu-id="bebbd-125">Ils ne doivent jamais comparer un **DROPEFFECT** à une copie DROPEFFECT, par exemple, \_ en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="bebbd-125">They should never compare a **DROPEFFECT** against, say, DROPEFFECT\_COPY by doing the following:</span></span>

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

<span data-ttu-id="bebbd-126">Au lieu de cela, l’application doit toujours masquer la valeur ou les valeurs recherchées en utilisant l’une des techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bebbd-126">Instead, the application should always mask for the value or values being sought as using one of the following techniques:</span></span>

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

<span data-ttu-id="bebbd-127">Cela permet de définir de nouveaux effets de suppression, tout en préservant la compatibilité descendante avec le code existant.</span><span class="sxs-lookup"><span data-stu-id="bebbd-127">This allows for the definition of new drop effects, while preserving backward compatibility with existing code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bebbd-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bebbd-128">Requirements</span></span>



| <span data-ttu-id="bebbd-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bebbd-129">Requirement</span></span> | <span data-ttu-id="bebbd-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="bebbd-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bebbd-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bebbd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bebbd-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bebbd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bebbd-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bebbd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bebbd-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bebbd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bebbd-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="bebbd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bebbd-136"><dt>OleIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bebbd-136"><dt>OleIdl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bebbd-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bebbd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebbd-138">**DoDragDrop**</span><span class="sxs-lookup"><span data-stu-id="bebbd-138">**DoDragDrop**</span></span>](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[<span data-ttu-id="bebbd-139">**IDropSource**</span><span class="sxs-lookup"><span data-stu-id="bebbd-139">**IDropSource**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[<span data-ttu-id="bebbd-140">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="bebbd-140">**IDropTarget**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





