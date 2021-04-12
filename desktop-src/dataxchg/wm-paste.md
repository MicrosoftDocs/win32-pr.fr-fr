---
title: Message WM_PASTE (winuser. h)
description: Une application envoie un \_ message de collage WM à un contrôle d’édition ou une zone de liste déroulante pour copier le contenu actuel du presse-papiers dans le contrôle d’édition à l’emplacement actuel du signe insertion. Les données sont insérées uniquement si le presse-papiers contient des données au \_ format de texte cf.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385095"
---
# <a name="wm_paste-message"></a><span data-ttu-id="e9d74-105">\_Message de collage WM</span><span class="sxs-lookup"><span data-stu-id="e9d74-105">WM\_PASTE message</span></span>

<span data-ttu-id="e9d74-106">Une application envoie un message de **\_ Collage WM** à un contrôle d’édition ou une zone de liste déroulante pour copier le contenu actuel du presse-papiers dans le contrôle d’édition à l’emplacement actuel du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="e9d74-106">An application sends a **WM\_PASTE** message to an edit control or combo box to copy the current content of the clipboard to the edit control at the current caret position.</span></span> <span data-ttu-id="e9d74-107">Les données sont insérées uniquement si le presse-papiers contient des données au format de [**\_ texte CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d74-107">Data is inserted only if the clipboard contains data in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a><span data-ttu-id="e9d74-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9d74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9d74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9d74-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9d74-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e9d74-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9d74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9d74-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9d74-112">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e9d74-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9d74-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9d74-113">Return value</span></span>

<span data-ttu-id="e9d74-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e9d74-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9d74-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e9d74-115">Remarks</span></span>

<span data-ttu-id="e9d74-116">Lorsqu’il est envoyé à une zone de liste déroulante, le message **WM \_ Paste** est géré par son contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e9d74-116">When sent to a combo box, the **WM\_PASTE** message is handled by its edit control.</span></span> <span data-ttu-id="e9d74-117">Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d74-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d74-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9d74-118">Requirements</span></span>



| <span data-ttu-id="e9d74-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9d74-119">Requirement</span></span> | <span data-ttu-id="e9d74-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9d74-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d74-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9d74-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d74-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9d74-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9d74-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9d74-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d74-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9d74-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9d74-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9d74-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9d74-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9d74-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9d74-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9d74-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9d74-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e9d74-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9d74-129">**WM- \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="e9d74-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="e9d74-130">**\_copie WM**</span><span class="sxs-lookup"><span data-stu-id="e9d74-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="e9d74-131">**découpe WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9d74-131">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="e9d74-132">**désannulation WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9d74-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="e9d74-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e9d74-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9d74-134">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="e9d74-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

