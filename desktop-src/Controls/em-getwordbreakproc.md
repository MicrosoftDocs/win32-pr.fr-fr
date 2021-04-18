---
title: Message EM_GETWORDBREAKPROC (winuser. h)
description: Obtient l’adresse de la fonction de WordWrap en cours. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466235"
---
# <a name="em_getwordbreakproc-message"></a><span data-ttu-id="42a93-105">\_Message GETWORDBREAKPROC em</span><span class="sxs-lookup"><span data-stu-id="42a93-105">EM\_GETWORDBREAKPROC message</span></span>

<span data-ttu-id="42a93-106">Obtient l’adresse de la fonction de WordWrap en cours.</span><span class="sxs-lookup"><span data-stu-id="42a93-106">Gets the address of the current Wordwrap function.</span></span> <span data-ttu-id="42a93-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="42a93-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="42a93-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42a93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a93-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42a93-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42a93-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="42a93-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="42a93-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42a93-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42a93-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="42a93-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a93-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42a93-113">Return value</span></span>

<span data-ttu-id="42a93-114">La valeur de retour spécifie l’adresse de la fonction WordWrap définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="42a93-114">The return value specifies the address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="42a93-115">La valeur de retour est **null** si aucune fonction de WordWrap n’existe.</span><span class="sxs-lookup"><span data-stu-id="42a93-115">The return value is **NULL** if no Wordwrap function exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a93-116">Notes</span><span class="sxs-lookup"><span data-stu-id="42a93-116">Remarks</span></span>

<span data-ttu-id="42a93-117">Une fonction WordWrap analyse une mémoire tampon de texte qui contient le texte à envoyer à l’écran, en recherchant le premier mot qui ne tient pas sur la ligne d’affichage actuelle.</span><span class="sxs-lookup"><span data-stu-id="42a93-117">A Wordwrap function scans a text buffer that contains text to be sent to the display, looking for the first word that does not fit on the current display line.</span></span> <span data-ttu-id="42a93-118">La fonction WordWrap place ce mot au début de la ligne suivante à l’écran.</span><span class="sxs-lookup"><span data-stu-id="42a93-118">The wordwrap function places this word at the beginning of the next line on the display.</span></span> <span data-ttu-id="42a93-119">Une fonction WordWrap définit le point auquel le système doit couper une ligne de texte pour les contrôles d’édition multiligne, généralement à un espace qui sépare deux mots.</span><span class="sxs-lookup"><span data-stu-id="42a93-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span>

<span data-ttu-id="42a93-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="42a93-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="42a93-121">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="42a93-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42a93-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42a93-122">Requirements</span></span>



| <span data-ttu-id="42a93-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42a93-123">Requirement</span></span> | <span data-ttu-id="42a93-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="42a93-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a93-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42a93-125">Minimum supported client</span></span><br/> | <span data-ttu-id="42a93-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42a93-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42a93-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42a93-127">Minimum supported server</span></span><br/> | <span data-ttu-id="42a93-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42a93-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42a93-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="42a93-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a93-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42a93-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a93-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42a93-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="42a93-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="42a93-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="42a93-133">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="42a93-133">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="42a93-134">**\_FMTLINES em**</span><span class="sxs-lookup"><span data-stu-id="42a93-134">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="42a93-135">**\_SETWORDBREAKPROC em**</span><span class="sxs-lookup"><span data-stu-id="42a93-135">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
</dt> </dl>

 

