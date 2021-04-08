---
title: Message EM_SETHYPHENATEINFO (RichEdit. h)
description: Définit le mode de césure d’un contrôle RichEdit.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844129"
---
# <a name="em_sethyphenateinfo-message"></a><span data-ttu-id="e877c-104">\_Message SETHYPHENATEINFO em</span><span class="sxs-lookup"><span data-stu-id="e877c-104">EM\_SETHYPHENATEINFO message</span></span>

<span data-ttu-id="e877c-105">Définit le mode de césure d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="e877c-105">Sets the way a rich edit control does hyphenation.</span></span>

## <a name="parameters"></a><span data-ttu-id="e877c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e877c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e877c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e877c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e877c-108">Pointeur vers une structure [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .</span><span class="sxs-lookup"><span data-stu-id="e877c-108">Pointer to a [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e877c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e877c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e877c-110">Non utilisé, doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e877c-110">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e877c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e877c-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e877c-112">Pour activer la césure, le client doit appeler [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), en spécifiant à \_ ADVANCEDTYPOGRAPHY.</span><span class="sxs-lookup"><span data-stu-id="e877c-112">To enable hyphenation, the client must call [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specifying TO\_ADVANCEDTYPOGRAPHY.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e877c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e877c-113">Requirements</span></span>



| <span data-ttu-id="e877c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e877c-114">Requirement</span></span> | <span data-ttu-id="e877c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e877c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e877c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e877c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e877c-117">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e877c-117">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e877c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e877c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e877c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e877c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e877c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e877c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e877c-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e877c-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e877c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e877c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e877c-123">**\_GETHYPHENATEINFO em**</span><span class="sxs-lookup"><span data-stu-id="e877c-123">**EM\_GETHYPHENATEINFO**</span></span>](em-gethyphenateinfo.md)
</dt> </dl>

 

 





