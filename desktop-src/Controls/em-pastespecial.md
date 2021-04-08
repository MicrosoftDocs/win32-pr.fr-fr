---
title: Message EM_PASTESPECIAL (RichEdit. h)
description: Colle un format de presse-papiers spécifique dans un contrôle RichEdit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843817"
---
# <a name="em_pastespecial-message"></a><span data-ttu-id="e3825-104">\_Message PASTESPECIAL em</span><span class="sxs-lookup"><span data-stu-id="e3825-104">EM\_PASTESPECIAL message</span></span>

<span data-ttu-id="e3825-105">Colle un format de presse-papiers spécifique dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="e3825-105">Pastes a specific clipboard format in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3825-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3825-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3825-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3825-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3825-108">Spécifie les [formats du presse-papiers](/windows/desktop/dataxchg/clipboard-formats).</span><span class="sxs-lookup"><span data-stu-id="e3825-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats).</span></span>

</dd> <dt>

<span data-ttu-id="e3825-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3825-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3825-110">Pointeur vers une structure [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e3825-110">Pointer to a [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) structure or **NULL**.</span></span> <span data-ttu-id="e3825-111">Si un objet est collé, la structure **REPASTESPECIAL** est remplie avec l’aspect d’affichage souhaité.</span><span class="sxs-lookup"><span data-stu-id="e3825-111">If an object is being pasted, the **REPASTESPECIAL** structure is filled in with the desired display aspect.</span></span> <span data-ttu-id="e3825-112">Si *lParam* a la **valeur null** ou si le membre **dwAspect** est égal à zéro, l’aspect d’affichage utilisé correspond au contenu du descripteur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e3825-112">If *lParam* is **NULL** or the **dwAspect** member is zero, the display aspect used will be the contents of the object descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3825-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3825-113">Return value</span></span>

<span data-ttu-id="e3825-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e3825-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3825-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3825-115">Requirements</span></span>



| <span data-ttu-id="e3825-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3825-116">Requirement</span></span> | <span data-ttu-id="e3825-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3825-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3825-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3825-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3825-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3825-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3825-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3825-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3825-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3825-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3825-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3825-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3825-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3825-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3825-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3825-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3825-125">**REPASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="e3825-125">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

