---
title: List-View les États de l’élément (CommCtrl. h)
description: La valeur d’état d’un élément se compose de l’état de l’élément, d’un index de masque de recouvrement facultatif et d’un index de masque d’image d’État facultatif.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525468"
---
# <a name="list-view-item-states"></a><span data-ttu-id="6d637-103">États de l’élément List-View</span><span class="sxs-lookup"><span data-stu-id="6d637-103">List-View Item States</span></span>

<span data-ttu-id="6d637-104">La valeur d’état d’un élément se compose de l’état de l’élément, d’un index de masque de recouvrement facultatif et d’un index de masque d’image d’État facultatif.</span><span class="sxs-lookup"><span data-stu-id="6d637-104">An item's state value consists of the item's state, an optional overlay mask index, and an optional state image mask index.</span></span>

<span data-ttu-id="6d637-105">L’état d’un élément détermine son apparence et ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6d637-105">An item's state determines its appearance and functionality.</span></span> <span data-ttu-id="6d637-106">L’État peut être zéro ou une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d637-106">The state can be zero or one or more of the following values:</span></span>



| <span data-ttu-id="6d637-107">Constante</span><span class="sxs-lookup"><span data-stu-id="6d637-107">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="6d637-108">Description</span><span class="sxs-lookup"><span data-stu-id="6d637-108">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <span data-ttu-id="6d637-109"><dt>**activation de LVIS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-109"><dt>**LVIS\_ACTIVATING**</dt></span></span> </dl>             | <span data-ttu-id="6d637-110">Actuellement non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6d637-110">Not currently supported.</span></span><br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="6d637-111"><dt>**LVIS \_ couper**</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-111"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="6d637-112">L’élément est marqué pour une opération couper-coller.</span><span class="sxs-lookup"><span data-stu-id="6d637-112">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="6d637-113"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-113"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="6d637-114">L’élément est mis en surbrillance en tant que cible de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="6d637-114">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="6d637-115"><dt>**LVIS \_ concentré**</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-115"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="6d637-116">L’élément a le focus, donc il est entouré d’un rectangle de focus standard.</span><span class="sxs-lookup"><span data-stu-id="6d637-116">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="6d637-117">Bien qu’un seul élément puisse être sélectionné, un seul élément peut avoir le focus.</span><span class="sxs-lookup"><span data-stu-id="6d637-117">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="6d637-118"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-118"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="6d637-119">L’index d’image de superposition de l’élément est récupéré par un masque.</span><span class="sxs-lookup"><span data-stu-id="6d637-119">The item's overlay image index is retrieved by a mask.</span></span><br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="6d637-120"><dt>**LVIS \_ sélectionné**</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-120"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="6d637-121">L'élément est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6d637-121">The item is selected.</span></span> <span data-ttu-id="6d637-122">L’apparence d’un élément sélectionné varie selon qu’il a le focus et également sur les couleurs système utilisées pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="6d637-122">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="6d637-123"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-123"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="6d637-124">L’index d’images d’état de l’élément est récupéré par un masque.</span><span class="sxs-lookup"><span data-stu-id="6d637-124">The item's state image index is retrieved by a mask.</span></span><br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="6d637-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6d637-125">Remarks</span></span>

<span data-ttu-id="6d637-126">Vous pouvez utiliser le masque **Lvis \_ OVERLAYMASK** pour isoler l’index de base un de l’image de superposition.</span><span class="sxs-lookup"><span data-stu-id="6d637-126">You can use the **LVIS\_OVERLAYMASK** mask to isolate the one-based index of the overlay image.</span></span> <span data-ttu-id="6d637-127">Vous pouvez utiliser le masque **Lvis \_ STATEIMAGEMASK** pour isoler l’index de base un de l’image d’État.</span><span class="sxs-lookup"><span data-stu-id="6d637-127">You can use the **LVIS\_STATEIMAGEMASK** mask to isolate the one-based index of the state image.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d637-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d637-128">Requirements</span></span>



| <span data-ttu-id="6d637-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d637-129">Requirement</span></span> | <span data-ttu-id="6d637-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d637-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d637-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d637-131">Header</span></span><br/> | <dl> <span data-ttu-id="6d637-132"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d637-132"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





