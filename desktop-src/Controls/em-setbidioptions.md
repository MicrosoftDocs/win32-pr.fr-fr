---
title: Message EM_SETBIDIOPTIONS (RichEdit. h)
description: Le \_ message em SETBIDIOPTIONS définit l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105592"
---
# <a name="em_setbidioptions-message"></a><span data-ttu-id="92099-104">\_Message SETBIDIOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="92099-104">EM\_SETBIDIOPTIONS message</span></span>

<span data-ttu-id="92099-105">Le message **em \_ SETBIDIOPTIONS** définit l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="92099-105">The **EM\_SETBIDIOPTIONS** message sets the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="92099-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92099-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92099-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92099-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92099-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="92099-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="92099-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92099-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92099-110">Pointeur vers une structure [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) qui indique comment définir l’état des options bidirectionnelles dans le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="92099-110">Pointer to a [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that indicates how to set the state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92099-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92099-111">Return value</span></span>

<span data-ttu-id="92099-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="92099-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92099-113">Notes</span><span class="sxs-lookup"><span data-stu-id="92099-113">Remarks</span></span>

<span data-ttu-id="92099-114">Le contrôle RichEdit doit être en mode texte brut ou **em \_ SETBIDIOPTIONS** ne fera rien.</span><span class="sxs-lookup"><span data-stu-id="92099-114">The rich edit control must be in plain text mode or **EM\_SETBIDIOPTIONS** will not do anything.</span></span>

<span data-ttu-id="92099-115">Dans les contrôles de texte brut, **em \_ SETBIDIOPTIONS** détermine automatiquement l’orientation et/ou l’alignement des paragraphes en fonction des règles de contexte.</span><span class="sxs-lookup"><span data-stu-id="92099-115">In plain text controls, **EM\_SETBIDIOPTIONS** automatically determines the paragraph direction and/or alignment based on the context rules.</span></span> <span data-ttu-id="92099-116">Ces règles indique que la direction et/ou l’alignement sont dérivés du premier caractère fort dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="92099-116">These rules state that the direction and/or alignment is derived from the first strong character in the control.</span></span> <span data-ttu-id="92099-117">Un caractère fort est un caractère à partir duquel la direction du texte peut être déterminée (consultez Unicode standard version 2,0).</span><span class="sxs-lookup"><span data-stu-id="92099-117">A strong character is one from which text direction can be determined (see Unicode Standard version 2.0).</span></span> <span data-ttu-id="92099-118">La direction du paragraphe et/ou l’alignement sont appliqués au format par défaut.</span><span class="sxs-lookup"><span data-stu-id="92099-118">The paragraph direction and/or alignment is applied to the default format.</span></span>

<span data-ttu-id="92099-119">**Em \_ SETBIDIOPTIONS** fait uniquement passer le format de paragraphe par défaut à RTL (de droite à gauche) s’il trouve un caractère RTL,</span><span class="sxs-lookup"><span data-stu-id="92099-119">**EM\_SETBIDIOPTIONS** only switches the default paragraph format to RTL (right to left) if it finds an RTL character,</span></span>

## <a name="requirements"></a><span data-ttu-id="92099-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92099-120">Requirements</span></span>



| <span data-ttu-id="92099-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92099-121">Requirement</span></span> | <span data-ttu-id="92099-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="92099-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92099-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92099-123">Minimum supported client</span></span><br/> | <span data-ttu-id="92099-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92099-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92099-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92099-125">Minimum supported server</span></span><br/> | <span data-ttu-id="92099-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92099-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92099-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="92099-127">Redistributable</span></span><br/>          | <span data-ttu-id="92099-128">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="92099-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="92099-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="92099-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="92099-130"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="92099-130"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92099-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92099-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="92099-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="92099-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="92099-133">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="92099-133">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="92099-134">**\_GETBIDIOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="92099-134">**EM\_GETBIDIOPTIONS**</span></span>](em-getbidioptions.md)
</dt> </dl>

 

 





