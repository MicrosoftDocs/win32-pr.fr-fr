---
title: Message EM_REDO (RichEdit. h)
description: Envoie un \_ message de rétablissement em à un contrôle RichEdit pour rétablir l’action suivante dans la file d’attente de restauration par progression du contrôle.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465898"
---
# <a name="em_redo-message"></a><span data-ttu-id="5cf71-104">\_Message de rétablissement em</span><span class="sxs-lookup"><span data-stu-id="5cf71-104">EM\_REDO message</span></span>

<span data-ttu-id="5cf71-105">Envoie un message de **\_ rétablissement em** à un contrôle RichEdit pour rétablir l’action suivante dans la file d’attente de restauration par progression du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5cf71-105">Sends an **EM\_REDO** message to a rich edit control to redo the next action in the control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cf71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cf71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cf71-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cf71-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf71-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5cf71-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5cf71-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cf71-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf71-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5cf71-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cf71-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5cf71-111">Return value</span></span>

<span data-ttu-id="5cf71-112">Si l’opération de **rétablissement** échoue, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5cf71-112">If the **Redo** operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5cf71-113">Si l’opération de **rétablissement** échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="5cf71-113">If the **Redo** operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf71-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5cf71-114">Remarks</span></span>

<span data-ttu-id="5cf71-115">Pour déterminer s’il existe des actions dans la file d’attente de restauration par progression du contrôle, envoyez le message de la valeur [**em \_**](em-canredo.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf71-115">To determine whether there are any actions in the control's redo queue, send the [**EM\_CANREDO**](em-canredo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf71-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cf71-116">Requirements</span></span>



| <span data-ttu-id="5cf71-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cf71-117">Requirement</span></span> | <span data-ttu-id="5cf71-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cf71-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf71-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cf71-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf71-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cf71-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cf71-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cf71-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf71-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cf71-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cf71-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cf71-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cf71-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cf71-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf71-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cf71-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5cf71-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5cf71-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5cf71-127">**EM- \_ CANREDO**</span><span class="sxs-lookup"><span data-stu-id="5cf71-127">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="5cf71-128">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="5cf71-128">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="5cf71-129">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="5cf71-129">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="5cf71-130">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="5cf71-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





