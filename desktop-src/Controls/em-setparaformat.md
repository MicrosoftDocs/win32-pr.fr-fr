---
title: Message EM_SETPARAFORMAT (RichEdit. h)
description: Définit la mise en forme de paragraphe pour la sélection actuelle dans un contrôle RichEdit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465055"
---
# <a name="em_setparaformat-message"></a><span data-ttu-id="51caa-104">\_Message SETPARAFORMAT em</span><span class="sxs-lookup"><span data-stu-id="51caa-104">EM\_SETPARAFORMAT message</span></span>

<span data-ttu-id="51caa-105">Définit la mise en forme de paragraphe pour la sélection actuelle dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="51caa-105">Sets the paragraph formatting for the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="51caa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51caa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51caa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51caa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51caa-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="51caa-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="51caa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51caa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51caa-110">Pointeur vers une structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) spécifiant les nouveaux attributs de mise en forme de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="51caa-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure specifying the new paragraph formatting attributes.</span></span> <span data-ttu-id="51caa-111">Seuls les attributs spécifiés par le membre **dwMask** sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="51caa-111">Only the attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="51caa-112">Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , qui est une extension de la structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="51caa-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="51caa-113">Avant d’envoyer le message **\_ SETPARAFORMAT em** , définissez le membre **cbSize** de la structure pour indiquer la version de la structure.</span><span class="sxs-lookup"><span data-stu-id="51caa-113">Before sending the **EM\_SETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51caa-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51caa-114">Return value</span></span>

<span data-ttu-id="51caa-115">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="51caa-115">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="51caa-116">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="51caa-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="51caa-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51caa-117">Requirements</span></span>



| <span data-ttu-id="51caa-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51caa-118">Requirement</span></span> | <span data-ttu-id="51caa-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="51caa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51caa-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51caa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51caa-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51caa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51caa-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51caa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51caa-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51caa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51caa-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="51caa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="51caa-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="51caa-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51caa-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51caa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="51caa-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="51caa-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51caa-128">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="51caa-128">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="51caa-129">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="51caa-129">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





