---
title: Message CB_GETEXTENDEDUI (winuser. h)
description: Détermine si une zone de liste déroulante possède l’interface utilisateur par défaut ou l’interface utilisateur étendue.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465267"
---
# <a name="cb_getextendedui-message"></a><span data-ttu-id="175de-104">\_Message GETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="175de-104">CB\_GETEXTENDEDUI message</span></span>

<span data-ttu-id="175de-105">Détermine si une zone de liste déroulante possède l’interface utilisateur par défaut ou l’interface utilisateur étendue.</span><span class="sxs-lookup"><span data-stu-id="175de-105">Determines whether a combo box has the default user interface or the extended user interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="175de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="175de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="175de-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="175de-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="175de-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="175de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="175de-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="175de-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="175de-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175de-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="175de-111">Return value</span></span>

<span data-ttu-id="175de-112">Si la zone de liste déroulante possède l’interface utilisateur étendue, la valeur de retour est **true**. Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="175de-112">If the combo box has the extended user interface, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="175de-113">Notes</span><span class="sxs-lookup"><span data-stu-id="175de-113">Remarks</span></span>

<span data-ttu-id="175de-114">Par défaut, la touche F4 ouvre ou ferme la liste et la flèche vers le bas modifie la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="175de-114">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="175de-115">Dans une zone de liste déroulante avec l’interface utilisateur étendue, la touche F4 est désactivée et l’appui sur la touche bas ouvre la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="175de-115">In a combo box with the extended user interface, the F4 key is disabled and pressing the DOWN ARROW key opens the drop-down list.</span></span>

## <a name="requirements"></a><span data-ttu-id="175de-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="175de-116">Requirements</span></span>



| <span data-ttu-id="175de-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="175de-117">Requirement</span></span> | <span data-ttu-id="175de-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="175de-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="175de-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="175de-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="175de-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="175de-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="175de-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="175de-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="175de-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="175de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="175de-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="175de-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175de-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="175de-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="175de-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="175de-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="175de-127">**\_SETEXTENDEDUI CB**</span><span class="sxs-lookup"><span data-stu-id="175de-127">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
</dt> <dt>

<span data-ttu-id="175de-128">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="175de-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="175de-129">Fonctionnalités de zone de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="175de-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





