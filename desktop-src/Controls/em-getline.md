---
title: Message EM_GETLINE (winuser. h)
description: Copie une ligne de texte à partir d’un contrôle d’édition et la place dans une mémoire tampon spécifiée. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941745"
---
# <a name="em_getline-message-winuserh"></a><span data-ttu-id="bd825-105">Message EM_GETLINE (winuser. h)</span><span class="sxs-lookup"><span data-stu-id="bd825-105">EM_GETLINE message (Winuser.h)</span></span>

<span data-ttu-id="bd825-106">Copie une ligne de texte à partir d’un contrôle d’édition et la place dans une mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bd825-106">Copies a line of text from an edit control and places it in a specified buffer.</span></span> <span data-ttu-id="bd825-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="bd825-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd825-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd825-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd825-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd825-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-110">Index de base zéro de la ligne à récupérer à partir d’un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="bd825-110">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="bd825-111">La valeur zéro spécifie la ligne la plus grande.</span><span class="sxs-lookup"><span data-stu-id="bd825-111">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="bd825-112">Ce paramètre est ignoré par un contrôle d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="bd825-112">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="bd825-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd825-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd825-114">Pointeur vers la mémoire tampon qui reçoit une copie de la ligne.</span><span class="sxs-lookup"><span data-stu-id="bd825-114">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="bd825-115">Avant d’envoyer le message, définissez le premier mot de cette mémoire tampon sur la taille, dans **TCHAR** s, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bd825-115">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="bd825-116">Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="bd825-116">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="bd825-117">La taille dans le premier mot est remplacée par la ligne copiée.</span><span class="sxs-lookup"><span data-stu-id="bd825-117">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd825-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd825-118">Return value</span></span>

<span data-ttu-id="bd825-119">La valeur de retour est le nombre de **TCHAR** s copié.</span><span class="sxs-lookup"><span data-stu-id="bd825-119">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="bd825-120">La valeur de retour est égale à zéro si le numéro de ligne spécifié par le paramètre *wParam* est supérieur au nombre de lignes dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="bd825-120">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd825-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bd825-121">Remarks</span></span>

<span data-ttu-id="bd825-122">**Contrôles d’édition :** La ligne copiée ne contient pas de caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd825-122">**Edit controls:** The copied line does not contain a terminating null character.</span></span>

<span data-ttu-id="bd825-123">**Contrôles RichEdit :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bd825-123">**Rich edit controls:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="bd825-124">La ligne copiée ne contient pas de caractère null de fin, sauf si aucun texte n’a été copié.</span><span class="sxs-lookup"><span data-stu-id="bd825-124">The copied line does not contain a terminating null character, unless no text was copied.</span></span> <span data-ttu-id="bd825-125">Si aucun texte n’a été copié, le message place un caractère null au début de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bd825-125">If no text was copied, the message places a null character at the beginning of the buffer.</span></span> <span data-ttu-id="bd825-126">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="bd825-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd825-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd825-127">Requirements</span></span>



| <span data-ttu-id="bd825-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd825-128">Requirement</span></span> | <span data-ttu-id="bd825-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd825-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd825-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd825-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bd825-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd825-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bd825-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd825-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bd825-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd825-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd825-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd825-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd825-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd825-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd825-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd825-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd825-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bd825-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd825-138">**\_LINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="bd825-138">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="bd825-139">**Modifier \_ getline**</span><span class="sxs-lookup"><span data-stu-id="bd825-139">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

<span data-ttu-id="bd825-140">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="bd825-140">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bd825-141">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="bd825-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

