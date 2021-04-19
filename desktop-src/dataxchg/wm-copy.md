---
title: Message WM_COPY (winuser. h)
description: Une application envoie le \_ message de copie WM à un contrôle d’édition ou une zone de liste déroulante pour copier la sélection actuelle dans le presse-papiers au \_ format de texte cf.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY l’échange de données de message
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106542102"
---
# <a name="wm_copy-message"></a><span data-ttu-id="5069e-104">\_Message de copie WM</span><span class="sxs-lookup"><span data-stu-id="5069e-104">WM\_COPY message</span></span>

<span data-ttu-id="5069e-105">Une application envoie le message de **\_ copie WM** à un contrôle d’édition ou une zone de liste déroulante pour copier la sélection actuelle dans le presse-papiers au format de [**\_ texte CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="5069e-105">An application sends the **WM\_COPY** message to an edit control or combo box to copy the current selection to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a><span data-ttu-id="5069e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5069e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5069e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5069e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5069e-108">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5069e-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5069e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5069e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5069e-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5069e-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5069e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5069e-111">Return value</span></span>

<span data-ttu-id="5069e-112">Retourne une valeur différente de zéro en cas de réussite, sinon zéro.</span><span class="sxs-lookup"><span data-stu-id="5069e-112">Returns nonzero value on success, else zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5069e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5069e-113">Remarks</span></span>

<span data-ttu-id="5069e-114">Lorsqu’il est envoyé à une zone de liste déroulante, le message de **\_ copie WM** est géré par son contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="5069e-114">When sent to a combo box, the **WM\_COPY** message is handled by its edit control.</span></span> <span data-ttu-id="5069e-115">Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5069e-115">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5069e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5069e-116">Requirements</span></span>



| <span data-ttu-id="5069e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5069e-117">Requirement</span></span> | <span data-ttu-id="5069e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5069e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5069e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5069e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5069e-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5069e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5069e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5069e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5069e-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5069e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5069e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5069e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5069e-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5069e-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5069e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5069e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5069e-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5069e-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5069e-127">**WM- \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="5069e-127">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="5069e-128">**découpe WM \_**</span><span class="sxs-lookup"><span data-stu-id="5069e-128">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="5069e-129">**\_coller WM**</span><span class="sxs-lookup"><span data-stu-id="5069e-129">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="5069e-130">**désannulation WM \_**</span><span class="sxs-lookup"><span data-stu-id="5069e-130">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="5069e-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5069e-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5069e-132">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="5069e-132">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

