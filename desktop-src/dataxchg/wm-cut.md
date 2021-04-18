---
title: Message WM_CUT (winuser. h)
description: Une application envoie un \_ message de coupe WM à un contrôle d’édition ou une zone de liste déroulante pour supprimer (couper) la sélection actuelle, le cas échéant, dans le contrôle d’édition et copier le texte supprimé dans le presse-papiers au \_ format de texte cf.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT l’échange de données de message
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509314"
---
# <a name="wm_cut-message"></a><span data-ttu-id="6bde4-104">\_Message de coupure WM</span><span class="sxs-lookup"><span data-stu-id="6bde4-104">WM\_CUT message</span></span>

<span data-ttu-id="6bde4-105">Une application envoie un message de **\_ coupe WM** à un contrôle d’édition ou une zone de liste déroulante pour supprimer (couper) la sélection actuelle, le cas échéant, dans le contrôle d’édition et copier le texte supprimé dans le presse-papiers au format de [**\_ texte CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="6bde4-105">An application sends a **WM\_CUT** message to an edit control or combo box to delete (cut) the current selection, if any, in the edit control and copy the deleted text to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a><span data-ttu-id="6bde4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bde4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bde4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bde4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bde4-108">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6bde4-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6bde4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bde4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bde4-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6bde4-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bde4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6bde4-111">Return value</span></span>

<span data-ttu-id="6bde4-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6bde4-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bde4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6bde4-113">Remarks</span></span>

<span data-ttu-id="6bde4-114">La suppression effectuée par le message **WM \_ Cut** peut être annulée en envoyant le contrôle d’édition à un message d' [**\_ annulation em**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="6bde4-114">The deletion performed by the **WM\_CUT** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="6bde4-115">Pour supprimer la sélection actuelle sans placer le texte supprimé dans le presse-papiers, utilisez le message [**WM \_ Clear**](wm-clear.md) .</span><span class="sxs-lookup"><span data-stu-id="6bde4-115">To delete the current selection without placing the deleted text on the clipboard, use the [**WM\_CLEAR**](wm-clear.md) message.</span></span>

<span data-ttu-id="6bde4-116">Lorsqu’il est envoyé à une zone de liste déroulante, le message **WM \_ Cut** est géré par son contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="6bde4-116">When sent to a combo box, the **WM\_CUT** message is handled by its edit control.</span></span> <span data-ttu-id="6bde4-117">Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6bde4-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bde4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bde4-118">Requirements</span></span>



| <span data-ttu-id="6bde4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bde4-119">Requirement</span></span> | <span data-ttu-id="6bde4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bde4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bde4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bde4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6bde4-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bde4-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6bde4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bde4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6bde4-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bde4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6bde4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6bde4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bde4-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bde4-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bde4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bde4-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6bde4-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6bde4-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6bde4-129">**WM- \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="6bde4-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="6bde4-130">**\_copie WM**</span><span class="sxs-lookup"><span data-stu-id="6bde4-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="6bde4-131">**\_coller WM**</span><span class="sxs-lookup"><span data-stu-id="6bde4-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="6bde4-132">**désannulation WM \_**</span><span class="sxs-lookup"><span data-stu-id="6bde4-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="6bde4-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6bde4-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6bde4-134">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="6bde4-134">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="6bde4-135">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="6bde4-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6bde4-136">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="6bde4-136">**EM\_UNDO**</span></span>](../controls/em-undo.md)
</dt> </dl>

 

