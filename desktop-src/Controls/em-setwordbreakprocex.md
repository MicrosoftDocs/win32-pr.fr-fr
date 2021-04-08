---
title: Message EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Définit la procédure de saut de mot étendu pour un contrôle RichEdit.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- EM_SETWORDBREAKPROCEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941958"
---
# <a name="em_setwordbreakprocex-message"></a><span data-ttu-id="211ff-104">\_Message SETWORDBREAKPROCEX em</span><span class="sxs-lookup"><span data-stu-id="211ff-104">EM\_SETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="211ff-105">Définit la procédure de saut de mot étendu pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="211ff-105">Sets the extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="211ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="211ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="211ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="211ff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="211ff-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="211ff-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="211ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="211ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="211ff-110">Pointeur vers une fonction [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) , ou **null** pour utiliser la procédure par défaut.</span><span class="sxs-lookup"><span data-stu-id="211ff-110">Pointer to an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function, or **NULL** to use the default procedure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="211ff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="211ff-111">Return value</span></span>

<span data-ttu-id="211ff-112">Ce message retourne l’adresse de la précédente procédure de coupure de mots étendue.</span><span class="sxs-lookup"><span data-stu-id="211ff-112">This message returns the address of the previous extended word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="211ff-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="211ff-113">Requirements</span></span>



| <span data-ttu-id="211ff-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="211ff-114">Requirement</span></span> | <span data-ttu-id="211ff-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="211ff-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="211ff-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="211ff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="211ff-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="211ff-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="211ff-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="211ff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="211ff-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="211ff-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="211ff-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="211ff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="211ff-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="211ff-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="211ff-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="211ff-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="211ff-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="211ff-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="211ff-124">**EditWordBreakProcEx**</span><span class="sxs-lookup"><span data-stu-id="211ff-124">**EditWordBreakProcEx**</span></span>](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[<span data-ttu-id="211ff-125">**\_GETWORDBREAKPROCEX em**</span><span class="sxs-lookup"><span data-stu-id="211ff-125">**EM\_GETWORDBREAKPROCEX**</span></span>](em-getwordbreakprocex.md)
</dt> </dl>

 

 





