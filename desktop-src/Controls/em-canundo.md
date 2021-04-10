---
title: Message EM_CANUNDO (winuser. h)
description: Détermine s’il existe des actions dans la file d’attente d’annulation d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104503"
---
# <a name="em_canundo-message"></a><span data-ttu-id="da838-105">\_Message em CANUNDO</span><span class="sxs-lookup"><span data-stu-id="da838-105">EM\_CANUNDO message</span></span>

<span data-ttu-id="da838-106">Détermine s’il existe des actions dans la file d’attente d’annulation d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="da838-106">Determines whether there are any actions in an edit control's undo queue.</span></span> <span data-ttu-id="da838-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="da838-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="da838-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da838-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da838-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da838-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da838-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="da838-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="da838-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da838-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da838-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="da838-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da838-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da838-113">Return value</span></span>

<span data-ttu-id="da838-114">S’il y a des actions dans la file d’attente d’annulation du contrôle, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="da838-114">If there are actions in the control's undo queue, the return value is nonzero.</span></span>

<span data-ttu-id="da838-115">Si la file d’attente d’annulation est vide, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="da838-115">If the undo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="da838-116">Notes</span><span class="sxs-lookup"><span data-stu-id="da838-116">Remarks</span></span>

<span data-ttu-id="da838-117">Si la file d’attente d’annulation n’est pas vide, vous pouvez envoyer le message d' [**\_ annulation em**](em-undo.md) au contrôle pour annuler l’opération la plus récente.</span><span class="sxs-lookup"><span data-stu-id="da838-117">If the undo queue is not empty, you can send the [**EM\_UNDO**](em-undo.md) message to the control to undo the most recent operation.</span></span>

<span data-ttu-id="da838-118">**Edit Controls et Rich edit 1,0 :** La file d’attente d’annulation contient uniquement l’opération la plus récente.</span><span class="sxs-lookup"><span data-stu-id="da838-118">**Edit controls and Rich Edit 1.0:** The undo queue contains only the most recent operation.</span></span>

<span data-ttu-id="da838-119">**Édition enrichie 2,0 et versions ultérieures :** La file d’attente d’annulation peut contenir plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="da838-119">**Rich Edit 2.0 and later:** The undo queue can contain multiple operations.</span></span>

<span data-ttu-id="da838-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="da838-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="da838-121">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="da838-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da838-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da838-122">Requirements</span></span>



| <span data-ttu-id="da838-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da838-123">Requirement</span></span> | <span data-ttu-id="da838-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="da838-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da838-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da838-125">Minimum supported client</span></span><br/> | <span data-ttu-id="da838-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da838-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da838-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da838-127">Minimum supported server</span></span><br/> | <span data-ttu-id="da838-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da838-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da838-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="da838-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="da838-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da838-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da838-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da838-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da838-132">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="da838-132">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





