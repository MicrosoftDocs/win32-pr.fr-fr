---
title: Message EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 et ultérieur récupère le type de la prochaine action d’annulation, le cas échéant. Édition enrichie de Microsoft 1,0 ce message n’est pas pris en charge.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942560"
---
# <a name="em_getundoname-message"></a><span data-ttu-id="fafd0-104">\_Message GETUNDONAME em</span><span class="sxs-lookup"><span data-stu-id="fafd0-104">EM\_GETUNDONAME message</span></span>

<span data-ttu-id="fafd0-105">Rich Edit 2,0 et versions ultérieures de Microsoft : récupère le type de la prochaine action d’annulation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fafd0-105">Microsoft Rich Edit 2.0 and later: Retrieves the type of the next undo action, if any.</span></span>

<span data-ttu-id="fafd0-106">Édition enrichie de Microsoft 1,0 : ce message n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fafd0-106">Microsoft Rich Edit 1.0: This message is not supported.</span></span>

## <a name="parameters"></a><span data-ttu-id="fafd0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fafd0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafd0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fafd0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fafd0-109">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fafd0-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fafd0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fafd0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fafd0-111">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fafd0-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fafd0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fafd0-112">Return value</span></span>

<span data-ttu-id="fafd0-113">S’il existe une action d’annulation, la valeur retournée est une valeur d’énumération [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) qui indique le type de l’action suivante dans la file d’attente d’annulation du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fafd0-113">If there is an undo action, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's undo queue.</span></span>

<span data-ttu-id="fafd0-114">Si aucune action ne peut être annulée ou si le type de l’action d’annulation suivante est inconnu, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="fafd0-114">If there are no actions that can be undone or the type of the next undo action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fafd0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fafd0-115">Remarks</span></span>

<span data-ttu-id="fafd0-116">Les types d’actions qui peuvent être annulés ou réexécutés incluent les opérations de frappe, de suppression, de glisser-déplacer, de couper et de coller.</span><span class="sxs-lookup"><span data-stu-id="fafd0-116">The types of actions that can be undone or redone include typing, delete, drag, drop, cut, and paste operations.</span></span> <span data-ttu-id="fafd0-117">Ces informations peuvent être utiles pour les applications qui fournissent une interface utilisateur étendue pour les opérations d’annulation et de rétablissement, telles qu’une zone de liste déroulante d’actions qui peuvent être annulées.</span><span class="sxs-lookup"><span data-stu-id="fafd0-117">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of actions that can be undone.</span></span>

## <a name="requirements"></a><span data-ttu-id="fafd0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fafd0-118">Requirements</span></span>



| <span data-ttu-id="fafd0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fafd0-119">Requirement</span></span> | <span data-ttu-id="fafd0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fafd0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fafd0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fafd0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fafd0-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fafd0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fafd0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fafd0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fafd0-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fafd0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fafd0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fafd0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fafd0-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fafd0-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fafd0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fafd0-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="fafd0-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fafd0-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fafd0-129">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="fafd0-129">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="fafd0-130">**\_rétablissement em**</span><span class="sxs-lookup"><span data-stu-id="fafd0-130">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="fafd0-131">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="fafd0-131">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="fafd0-132">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="fafd0-132">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





