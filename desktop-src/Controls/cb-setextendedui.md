---
title: Message CB_SETEXTENDEDUI (winuser. h)
description: Une application envoie un \_ message CB SETEXTENDEDUI pour sélectionner l’interface utilisateur par défaut ou l’interface utilisateur étendue pour une zone de liste déroulante avec le \_ style déroulant CBS ou le \_ style DropDownList SCC.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465254"
---
# <a name="cb_setextendedui-message"></a><span data-ttu-id="097d1-104">\_Message SETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="097d1-104">CB\_SETEXTENDEDUI message</span></span>

<span data-ttu-id="097d1-105">Une application envoie un message **CB \_ SETEXTENDEDUI** pour sélectionner l’interface utilisateur par défaut ou l’interface utilisateur étendue pour une zone de liste déroulante avec le style [**\_ déroulant CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="097d1-105">An application sends a **CB\_SETEXTENDEDUI** message to select either the default UI or the extended UI for a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="097d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="097d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="097d1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="097d1-108">Valeur **booléenne** qui spécifie si la zone de liste déroulante utilise l’interface utilisateur étendue (**true**) ou l’interface utilisateur par défaut (**false**).</span><span class="sxs-lookup"><span data-stu-id="097d1-108">A **BOOL** that specifies whether the combo box uses the extended UI (**TRUE**) or the default UI (**FALSE**).</span></span>

</dd> <dt>

<span data-ttu-id="097d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="097d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="097d1-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="097d1-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097d1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="097d1-111">Return value</span></span>

<span data-ttu-id="097d1-112">Si l’opération a échoué, la valeur de retour est CB \_ OK.</span><span class="sxs-lookup"><span data-stu-id="097d1-112">If the operation succeeds, the return value is CB\_OKAY.</span></span> <span data-ttu-id="097d1-113">Si une erreur se produit, il s’agit de CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="097d1-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="097d1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="097d1-114">Remarks</span></span>

<span data-ttu-id="097d1-115">Par défaut, la touche F4 ouvre ou ferme la liste et la flèche vers le bas modifie la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="097d1-115">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="097d1-116">Dans l’interface utilisateur étendue, la touche F4 est désactivée et la touche de direction bas ouvre la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="097d1-116">In the extended UI, the F4 key is disabled and the DOWN ARROW key opens the drop-down list.</span></span> <span data-ttu-id="097d1-117">La roulette de la souris, qui fait normalement défiler les éléments de la liste, n’a aucun effet lorsque l’interface utilisateur étendue est définie.</span><span class="sxs-lookup"><span data-stu-id="097d1-117">The mouse wheel, which normally scrolls through the items in the list, has no effect when the extended UI is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="097d1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="097d1-118">Requirements</span></span>



| <span data-ttu-id="097d1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="097d1-119">Requirement</span></span> | <span data-ttu-id="097d1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="097d1-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="097d1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="097d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="097d1-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="097d1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="097d1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="097d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="097d1-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="097d1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="097d1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="097d1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="097d1-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="097d1-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097d1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="097d1-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="097d1-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="097d1-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="097d1-129">**\_GETEXTENDEDUI CB**</span><span class="sxs-lookup"><span data-stu-id="097d1-129">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
</dt> <dt>

<span data-ttu-id="097d1-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="097d1-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="097d1-131">Fonctionnalités de zone de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="097d1-131">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





