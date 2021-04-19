---
title: États des boutons de barre d’outils (CommCtrl. h)
description: Cette section répertorie les États qu’un bouton de barre d’outils peut avoir.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525453"
---
# <a name="toolbar-button-states"></a><span data-ttu-id="12549-103">États des boutons de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="12549-103">Toolbar Button States</span></span>

<span data-ttu-id="12549-104">Cette section répertorie les États qu’un bouton de barre d’outils peut avoir.</span><span class="sxs-lookup"><span data-stu-id="12549-104">This section lists the states a toolbar button can have.</span></span>



| <span data-ttu-id="12549-105">Constante</span><span class="sxs-lookup"><span data-stu-id="12549-105">Constant</span></span>                                                                                                                                                                              | <span data-ttu-id="12549-106">Description</span><span class="sxs-lookup"><span data-stu-id="12549-106">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <span data-ttu-id="12549-107"><dt>**TBSTATE \_ activé**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-107"><dt>**TBSTATE\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="12549-108">Le bouton a le style de [**\_ contrôle TBSTYLE**](toolbar-control-and-button-styles.md) et l’utilisateur clique dessus.</span><span class="sxs-lookup"><span data-stu-id="12549-108">The button has the [**TBSTYLE\_CHECK**](toolbar-control-and-button-styles.md) style and is being clicked.</span></span><br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <span data-ttu-id="12549-109"><dt>**TBSTATE \_ ellipses**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-109"><dt>**TBSTATE\_ELLIPSES**</dt></span></span> </dl>                | <span data-ttu-id="12549-110">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="12549-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="12549-111">Le texte du bouton est coupé et des points de suspension s’affichent.</span><span class="sxs-lookup"><span data-stu-id="12549-111">The button's text is cut off and an ellipsis is displayed.</span></span><br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <span data-ttu-id="12549-112"><dt>**TBSTATE \_ activé**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-112"><dt>**TBSTATE\_ENABLED**</dt></span></span> </dl>                   | <span data-ttu-id="12549-113">Le bouton accepte les entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12549-113">The button accepts user input.</span></span> <span data-ttu-id="12549-114">Un bouton qui n’a pas cet État est grisé.</span><span class="sxs-lookup"><span data-stu-id="12549-114">A button that does not have this state is grayed.</span></span><br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <span data-ttu-id="12549-115"><dt>**TBSTATE \_ masqué**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-115"><dt>**TBSTATE\_HIDDEN**</dt></span></span> </dl>                      | <span data-ttu-id="12549-116">Le bouton n’est pas visible et ne peut pas recevoir d’entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12549-116">The button is not visible and cannot receive user input.</span></span><br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <span data-ttu-id="12549-117"><dt>**TBSTATE \_ indéterminé**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-117"><dt>**TBSTATE\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="12549-118">Le bouton est grisé.</span><span class="sxs-lookup"><span data-stu-id="12549-118">The button is grayed.</span></span><br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <span data-ttu-id="12549-119"><dt>**TBSTATE \_ marqué**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-119"><dt>**TBSTATE\_MARKED**</dt></span></span> </dl>                      | <span data-ttu-id="12549-120">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="12549-120">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="12549-121">Le bouton est marqué.</span><span class="sxs-lookup"><span data-stu-id="12549-121">The button is marked.</span></span> <span data-ttu-id="12549-122">L’interprétation d’un élément marqué dépend de l’application.</span><span class="sxs-lookup"><span data-stu-id="12549-122">The interpretation of a marked item is dependent upon the application.</span></span> <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <span data-ttu-id="12549-123"><dt>**TBSTATE \_ enfoncé**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-123"><dt>**TBSTATE\_PRESSED**</dt></span></span> </dl>                   | <span data-ttu-id="12549-124">L’utilisateur clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="12549-124">The button is being clicked.</span></span><br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <span data-ttu-id="12549-125"><dt>**\_Retour à la ligne TBSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="12549-125"><dt>**TBSTATE\_WRAP**</dt></span></span> </dl>                            | <span data-ttu-id="12549-126">Le bouton est suivi d’un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="12549-126">The button is followed by a line break.</span></span> <span data-ttu-id="12549-127">L’état du bouton doit également être \_ activé pour TBSTATE.</span><span class="sxs-lookup"><span data-stu-id="12549-127">The button must also have the TBSTATE\_ENABLED state.</span></span><br/>                                              |



## <a name="remarks"></a><span data-ttu-id="12549-128">Notes</span><span class="sxs-lookup"><span data-stu-id="12549-128">Remarks</span></span>

<span data-ttu-id="12549-129">Une barre d’outils peut avoir une combinaison d’États.</span><span class="sxs-lookup"><span data-stu-id="12549-129">A toolbar may have a combination of states.</span></span>

## <a name="requirements"></a><span data-ttu-id="12549-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12549-130">Requirements</span></span>



| <span data-ttu-id="12549-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12549-131">Requirement</span></span> | <span data-ttu-id="12549-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="12549-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12549-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="12549-133">Header</span></span><br/> | <dl> <span data-ttu-id="12549-134"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12549-134"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





