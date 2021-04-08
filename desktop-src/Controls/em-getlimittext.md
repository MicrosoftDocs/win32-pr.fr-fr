---
title: Message EM_GETLIMITTEXT (winuser. h)
description: Obtient la limite de texte actuelle pour un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843161"
---
# <a name="em_getlimittext-message"></a><span data-ttu-id="7e6f8-105">\_Message GETLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="7e6f8-105">EM\_GETLIMITTEXT message</span></span>

<span data-ttu-id="7e6f8-106">Obtient la limite de texte actuelle pour un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-106">Gets the current text limit for an edit control.</span></span> <span data-ttu-id="7e6f8-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e6f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e6f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e6f8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e6f8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e6f8-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7e6f8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e6f8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e6f8-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e6f8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e6f8-113">Return value</span></span>

<span data-ttu-id="7e6f8-114">La valeur de retour est la limite de texte.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-114">The return value is the text limit.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e6f8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7e6f8-115">Remarks</span></span>

<span data-ttu-id="7e6f8-116">**Contrôles d’édition, édition complète 2,0 et versions ultérieures :** La limite de texte correspond à la quantité maximale de texte, dans **TCHAR** s, que le contrôle peut contenir.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-116">**Edit controls, Rich Edit 2.0 and later:** The text limit is the maximum amount of text, in **TCHAR** s, that the control can contain.</span></span> <span data-ttu-id="7e6f8-117">Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-117">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="7e6f8-118">Deux documents avec la même limite de caractères produisent la même limite de texte, même si l’un est ANSI et l’autre Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-118">Two documents with the same character limit will yield the same text limit, even if one is ANSI and the other is Unicode.</span></span>

<span data-ttu-id="7e6f8-119">**Édition enrichie 1,0 :** La limite de texte correspond à la quantité maximale de texte, en octets, que le contrôle Rich Edit peut contenir.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-119">**Rich Edit 1.0:** The text limit is the maximum amount of text, in bytes, that the rich edit control can contain.</span></span>

<span data-ttu-id="7e6f8-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7e6f8-121">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6f8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e6f8-122">Requirements</span></span>



| <span data-ttu-id="7e6f8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e6f8-123">Requirement</span></span> | <span data-ttu-id="7e6f8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e6f8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6f8-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e6f8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7e6f8-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e6f8-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7e6f8-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e6f8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7e6f8-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e6f8-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e6f8-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e6f8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e6f8-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e6f8-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e6f8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e6f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e6f8-132">**\_SETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="7e6f8-132">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 





