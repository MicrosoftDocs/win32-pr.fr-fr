---
title: Message EM_SETUNDOLIMIT (RichEdit. h)
description: Définit le nombre maximal d’actions qui peuvent être stockées dans la file d’attente d’annulation d’un contrôle RichEdit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942292"
---
# <a name="em_setundolimit-message"></a><span data-ttu-id="01d54-104">\_Message SETUNDOLIMIT em</span><span class="sxs-lookup"><span data-stu-id="01d54-104">EM\_SETUNDOLIMIT message</span></span>

<span data-ttu-id="01d54-105">Définit le nombre maximal d’actions qui peuvent être stockées dans la file d’attente d’annulation d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="01d54-105">Sets the maximum number of actions that can stored in the undo queue of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="01d54-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01d54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d54-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01d54-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01d54-108">Spécifie le nombre maximal d’actions qui peuvent être stockées dans la file d’attente d’annulation.</span><span class="sxs-lookup"><span data-stu-id="01d54-108">Specifies the maximum number of actions that can be stored in the undo queue.</span></span>

</dd> <dt>

<span data-ttu-id="01d54-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01d54-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01d54-110">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="01d54-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d54-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01d54-111">Return value</span></span>

<span data-ttu-id="01d54-112">La valeur de retour est le nouveau nombre maximal d’actions d’annulation pour le contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="01d54-112">The return value is the new maximum number of undo actions for the rich edit control.</span></span> <span data-ttu-id="01d54-113">Cette valeur peut être inférieure à *wParam* si la mémoire est limitée.</span><span class="sxs-lookup"><span data-stu-id="01d54-113">This value may be less than *wParam* if memory is limited.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d54-114">Notes</span><span class="sxs-lookup"><span data-stu-id="01d54-114">Remarks</span></span>

<span data-ttu-id="01d54-115">Par défaut, le nombre maximal d’actions dans la file d’attente d’annulation est 100.</span><span class="sxs-lookup"><span data-stu-id="01d54-115">By default, the maximum number of actions in the undo queue is 100.</span></span> <span data-ttu-id="01d54-116">Si vous augmentez ce nombre, la mémoire disponible doit être suffisante pour accueillir le nouveau nombre.</span><span class="sxs-lookup"><span data-stu-id="01d54-116">If you increase this number, there must be enough available memory to accommodate the new number.</span></span> <span data-ttu-id="01d54-117">Pour de meilleures performances, définissez la limite à la plus petite valeur possible.</span><span class="sxs-lookup"><span data-stu-id="01d54-117">For better performance, set the limit to the smallest possible value.</span></span>

<span data-ttu-id="01d54-118">La définition de la limite à zéro désactive la fonctionnalité d' **annulation** .</span><span class="sxs-lookup"><span data-stu-id="01d54-118">Setting the limit to zero disables the **Undo** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d54-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01d54-119">Requirements</span></span>



| <span data-ttu-id="01d54-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01d54-120">Requirement</span></span> | <span data-ttu-id="01d54-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="01d54-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01d54-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01d54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="01d54-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01d54-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01d54-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01d54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="01d54-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01d54-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01d54-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="01d54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="01d54-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="01d54-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01d54-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01d54-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="01d54-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="01d54-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="01d54-130">**EM- \_ CANREDO**</span><span class="sxs-lookup"><span data-stu-id="01d54-130">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="01d54-131">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="01d54-131">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="01d54-132">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="01d54-132">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="01d54-133">**\_rétablissement em**</span><span class="sxs-lookup"><span data-stu-id="01d54-133">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="01d54-134">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="01d54-134">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





