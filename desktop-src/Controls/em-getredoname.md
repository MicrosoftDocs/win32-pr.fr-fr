---
title: Message EM_GETREDONAME (RichEdit. h)
description: Récupère le type de l’action suivante, le cas échéant, dans la file d’attente de restauration par progression du contrôle RichEdit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942240"
---
# <a name="em_getredoname-message"></a><span data-ttu-id="b6837-104">\_Message GETREDONAME em</span><span class="sxs-lookup"><span data-stu-id="b6837-104">EM\_GETREDONAME message</span></span>

<span data-ttu-id="b6837-105">Récupère le type de l’action suivante, le cas échéant, dans la file d’attente de restauration par progression du contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="b6837-105">Retrieves the type of the next action, if any, in the rich edit control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6837-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6837-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6837-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6837-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b6837-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6837-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6837-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6837-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b6837-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6837-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6837-111">Return value</span></span>

<span data-ttu-id="b6837-112">Si la file d’attente de restauration par progression pour le contrôle n’est pas vide, la valeur retournée est une valeur d’énumération [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) qui indique le type de l’action suivante dans la file d’attente de restauration par progression du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b6837-112">If the redo queue for the control is not empty, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's redo queue.</span></span>

<span data-ttu-id="b6837-113">S’il n’y a pas d’actions rétablies ou si le type de l’action retablie suivante est inconnu, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="b6837-113">If there are no redoable actions or the type of the next redoable action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6837-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b6837-114">Remarks</span></span>

<span data-ttu-id="b6837-115">Les types d’actions qui peuvent être annulés ou réexécutés incluent les opérations de frappe, de suppression, de glisser-déplacer, de couper et de coller.</span><span class="sxs-lookup"><span data-stu-id="b6837-115">The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations.</span></span> <span data-ttu-id="b6837-116">Ces informations peuvent être utiles pour les applications qui fournissent une interface utilisateur étendue pour les opérations d’annulation et de rétablissement, telles qu’une zone de liste déroulante d’actions rétablies.</span><span class="sxs-lookup"><span data-stu-id="b6837-116">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of redoable actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6837-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6837-117">Requirements</span></span>



| <span data-ttu-id="b6837-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6837-118">Requirement</span></span> | <span data-ttu-id="b6837-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6837-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6837-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6837-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6837-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6837-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6837-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6837-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6837-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6837-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6837-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6837-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6837-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6837-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6837-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6837-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6837-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b6837-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6837-128">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="b6837-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="b6837-129">**\_rétablissement em**</span><span class="sxs-lookup"><span data-stu-id="b6837-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="b6837-130">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="b6837-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="b6837-131">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="b6837-131">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





