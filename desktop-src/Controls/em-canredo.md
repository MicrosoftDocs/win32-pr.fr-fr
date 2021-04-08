---
title: Message EM_CANREDO (RichEdit. h)
description: Détermine s’il existe des actions dans la file d’attente de restauration par progression des contrôles.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- EM_CANREDO les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843897"
---
# <a name="em_canredo-message"></a><span data-ttu-id="0b940-104">Message de la \_ CANREDO em</span><span class="sxs-lookup"><span data-stu-id="0b940-104">EM\_CANREDO message</span></span>

<span data-ttu-id="0b940-105">Détermine s’il existe des actions dans la file d’attente de restauration par progression des contrôles.</span><span class="sxs-lookup"><span data-stu-id="0b940-105">Determines whether there are any actions in the control redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b940-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b940-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b940-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b940-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b940-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0b940-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0b940-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b940-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b940-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0b940-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b940-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b940-111">Return value</span></span>

<span data-ttu-id="0b940-112">S’il y a des actions dans la file d’attente de rétablissement des contrôles, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="0b940-112">If there are actions in the control redo queue, the return value is a nonzero value.</span></span>

<span data-ttu-id="0b940-113">Si la file d’attente de restauration par progression est vide, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="0b940-113">If the redo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b940-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0b940-114">Remarks</span></span>

<span data-ttu-id="0b940-115">Pour rétablir l’opération d’annulation la plus récente, envoyez le message [**em \_ Redo**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="0b940-115">To redo the most recent undo operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b940-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b940-116">Requirements</span></span>



| <span data-ttu-id="0b940-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b940-117">Requirement</span></span> | <span data-ttu-id="0b940-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b940-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b940-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b940-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b940-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b940-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b940-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b940-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b940-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b940-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b940-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b940-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b940-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b940-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b940-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b940-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b940-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0b940-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b940-127">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="0b940-127">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="0b940-128">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="0b940-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="0b940-129">**\_rétablissement em**</span><span class="sxs-lookup"><span data-stu-id="0b940-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="0b940-130">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="0b940-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





