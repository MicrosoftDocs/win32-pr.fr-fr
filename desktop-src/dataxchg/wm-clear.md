---
title: Message WM_CLEAR (winuser. h)
description: Une application envoie un \_ message WM Clear à un contrôle Edit ou à une zone de liste modifiable pour supprimer (effacer) la sélection actuelle, le cas échéant, du contrôle d’édition.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR l’échange de données de message
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512811"
---
# <a name="wm_clear-message"></a><span data-ttu-id="57994-104">\_Message d’effacement WM</span><span class="sxs-lookup"><span data-stu-id="57994-104">WM\_CLEAR message</span></span>

<span data-ttu-id="57994-105">Une application envoie un message **WM \_ Clear** à un contrôle Edit ou à une zone de liste modifiable pour supprimer (effacer) la sélection actuelle, le cas échéant, du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="57994-105">An application sends a **WM\_CLEAR** message to an edit control or combo box to delete (clear) the current selection, if any, from the edit control.</span></span>


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a><span data-ttu-id="57994-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57994-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57994-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57994-108">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="57994-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57994-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57994-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57994-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="57994-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57994-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57994-111">Return value</span></span>

<span data-ttu-id="57994-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="57994-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57994-113">Notes</span><span class="sxs-lookup"><span data-stu-id="57994-113">Remarks</span></span>

<span data-ttu-id="57994-114">La suppression effectuée par le message **WM \_ Clear** peut être annulée en envoyant le contrôle d’édition à un message d' [**\_ annulation em**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="57994-114">The deletion performed by the **WM\_CLEAR** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="57994-115">Pour supprimer la sélection actuelle et placer le contenu supprimé dans le presse-papiers, utilisez le message « [**WM \_ Cut**](wm-cut.md) ».</span><span class="sxs-lookup"><span data-stu-id="57994-115">To delete the current selection and place the deleted content on the clipboard, use the [**WM\_CUT**](wm-cut.md) message.</span></span>

<span data-ttu-id="57994-116">Lorsqu’il est envoyé à une zone de liste déroulante, le message **WM \_ Clear** est géré par son contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="57994-116">When sent to a combo box, the **WM\_CLEAR** message is handled by its edit control.</span></span> <span data-ttu-id="57994-117">Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="57994-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="57994-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57994-118">Requirements</span></span>



| <span data-ttu-id="57994-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57994-119">Requirement</span></span> | <span data-ttu-id="57994-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="57994-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57994-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57994-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57994-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57994-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="57994-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57994-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57994-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57994-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57994-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="57994-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="57994-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57994-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57994-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57994-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="57994-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="57994-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57994-129">**\_copie WM**</span><span class="sxs-lookup"><span data-stu-id="57994-129">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="57994-130">**découpe WM \_**</span><span class="sxs-lookup"><span data-stu-id="57994-130">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="57994-131">**\_coller WM**</span><span class="sxs-lookup"><span data-stu-id="57994-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="57994-132">**désannulation WM \_**</span><span class="sxs-lookup"><span data-stu-id="57994-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="57994-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="57994-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57994-134">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="57994-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

