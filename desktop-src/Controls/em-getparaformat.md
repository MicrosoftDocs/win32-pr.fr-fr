---
title: Message EM_GETPARAFORMAT (RichEdit. h)
description: Récupère la mise en forme de paragraphe de la sélection actuelle dans un contrôle RichEdit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942665"
---
# <a name="em_getparaformat-message"></a><span data-ttu-id="3374a-104">\_Message GETPARAFORMAT em</span><span class="sxs-lookup"><span data-stu-id="3374a-104">EM\_GETPARAFORMAT message</span></span>

<span data-ttu-id="3374a-105">Récupère la mise en forme de paragraphe de la sélection actuelle dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="3374a-105">Retrieves the paragraph formatting of the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3374a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3374a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3374a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3374a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3374a-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="3374a-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3374a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3374a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3374a-110">Pointeur vers une structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) qui reçoit les attributs de mise en forme de paragraphe de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="3374a-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure that receives the paragraph formatting attributes of the current selection.</span></span>

<span data-ttu-id="3374a-111">Si plusieurs paragraphes sont sélectionnés, la structure reçoit les attributs du premier paragraphe et le membre **dwMask** spécifie les attributs qui sont cohérents dans toute la sélection.</span><span class="sxs-lookup"><span data-stu-id="3374a-111">If more than one paragraph is selected, the structure receives the attributes of the first paragraph, and the **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span>

<span data-ttu-id="3374a-112">Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , qui est une extension de la structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="3374a-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="3374a-113">Avant d’envoyer le message **\_ GETPARAFORMAT em** , définissez le membre **cbSize** de la structure pour indiquer la version de la structure.</span><span class="sxs-lookup"><span data-stu-id="3374a-113">Before sending the **EM\_GETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3374a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3374a-114">Return value</span></span>

<span data-ttu-id="3374a-115">Ce message retourne la valeur du membre **dwMask** de la structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="3374a-115">This message returns the value of the **dwMask** member of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3374a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3374a-116">Requirements</span></span>



| <span data-ttu-id="3374a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3374a-117">Requirement</span></span> | <span data-ttu-id="3374a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3374a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3374a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3374a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3374a-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3374a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3374a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3374a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3374a-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3374a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3374a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3374a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3374a-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3374a-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3374a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3374a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3374a-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3374a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3374a-127">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="3374a-127">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="3374a-128">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="3374a-128">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





