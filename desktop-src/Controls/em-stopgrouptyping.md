---
title: Message EM_STOPGROUPTYPING (RichEdit. h)
description: Empêche un contrôle RichEdit de collecter des actions de frappe supplémentaires dans l’action d’annulation actuelle. Le contrôle stocke l’action de frappe suivante, le cas échéant, dans une nouvelle action de la file d’attente d’annulation.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741236"
---
# <a name="em_stopgrouptyping-message"></a><span data-ttu-id="36888-105">\_Message STOPGROUPTYPING em</span><span class="sxs-lookup"><span data-stu-id="36888-105">EM\_STOPGROUPTYPING message</span></span>

<span data-ttu-id="36888-106">Empêche un contrôle RichEdit de collecter des actions de frappe supplémentaires dans l’action d’annulation actuelle.</span><span class="sxs-lookup"><span data-stu-id="36888-106">Stops a rich edit control from collecting additional typing actions into the current undo action.</span></span> <span data-ttu-id="36888-107">Le contrôle stocke l’action de frappe suivante, le cas échéant, dans une nouvelle action de la file d’attente d’annulation.</span><span class="sxs-lookup"><span data-stu-id="36888-107">The control stores the next typing action, if any, into a new action in the undo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="36888-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36888-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36888-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36888-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36888-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="36888-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="36888-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36888-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36888-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="36888-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36888-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36888-113">Return value</span></span>

<span data-ttu-id="36888-114">La valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="36888-114">The return value is zero.</span></span> <span data-ttu-id="36888-115">Ce message ne peut pas échouer.</span><span class="sxs-lookup"><span data-stu-id="36888-115">This message cannot fail.</span></span>

## <a name="remarks"></a><span data-ttu-id="36888-116">Notes</span><span class="sxs-lookup"><span data-stu-id="36888-116">Remarks</span></span>

<span data-ttu-id="36888-117">Un contrôle RichEdit regroupe les actions consécutives de frappe, y compris les caractères supprimés à l’aide de la touche **retour arrière** , en une seule opération d’annulation jusqu’à ce que l’un des événements suivants se produise :</span><span class="sxs-lookup"><span data-stu-id="36888-117">A rich edit control groups consecutive typing actions, including characters deleted by using the **BackSpace** key, into a single undo action until one of the following events occurs:</span></span>

-   <span data-ttu-id="36888-118">Le contrôle reçoit un **message \_ STOPGROUPTYPING em** .</span><span class="sxs-lookup"><span data-stu-id="36888-118">The control receives an **EM\_STOPGROUPTYPING** message.</span></span>
-   <span data-ttu-id="36888-119">Le contrôle perd le focus.</span><span class="sxs-lookup"><span data-stu-id="36888-119">The control loses focus.</span></span>
-   <span data-ttu-id="36888-120">L’utilisateur déplace la sélection actuelle, soit à l’aide des touches de direction, soit en cliquant sur la souris.</span><span class="sxs-lookup"><span data-stu-id="36888-120">The user moves the current selection, either by using the arrow keys or by clicking the mouse.</span></span>
-   <span data-ttu-id="36888-121">L’utilisateur appuie sur la touche **Suppr** .</span><span class="sxs-lookup"><span data-stu-id="36888-121">The user presses the **Delete** key.</span></span>
-   <span data-ttu-id="36888-122">L’utilisateur effectue toute autre action, telle qu’une opération de collage qui n’implique **pas** de saisie.</span><span class="sxs-lookup"><span data-stu-id="36888-122">The user performs any other action, such as a paste operation that does **not** involve typing.</span></span>

<span data-ttu-id="36888-123">Vous pouvez envoyer le **message \_ STOPGROUPTYPING em** pour fractionner les actions de frappe consécutives en groupes d’annulation plus petits.</span><span class="sxs-lookup"><span data-stu-id="36888-123">You can send the **EM\_STOPGROUPTYPING** message to break consecutive typing actions into smaller undo groups.</span></span> <span data-ttu-id="36888-124">Par exemple, vous pouvez envoyer **des \_ STOPGROUPTYPING em** après chaque caractère ou à chaque saut de mot.</span><span class="sxs-lookup"><span data-stu-id="36888-124">For example, you could send **EM\_STOPGROUPTYPING** after each character or at each word break.</span></span>

## <a name="requirements"></a><span data-ttu-id="36888-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36888-125">Requirements</span></span>



| <span data-ttu-id="36888-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36888-126">Requirement</span></span> | <span data-ttu-id="36888-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="36888-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36888-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36888-128">Minimum supported client</span></span><br/> | <span data-ttu-id="36888-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36888-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36888-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36888-130">Minimum supported server</span></span><br/> | <span data-ttu-id="36888-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36888-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36888-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="36888-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="36888-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="36888-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36888-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36888-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36888-135">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="36888-135">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





