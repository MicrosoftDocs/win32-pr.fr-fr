---
title: Message EM_SETWORDBREAKPROC (winuser. h)
description: Remplace la fonction WordWrap par défaut d’un contrôle d’édition par une fonction WordWrap définie par l’application. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508706"
---
# <a name="em_setwordbreakproc-message"></a><span data-ttu-id="7766f-105">\_Message SETWORDBREAKPROC em</span><span class="sxs-lookup"><span data-stu-id="7766f-105">EM\_SETWORDBREAKPROC message</span></span>

<span data-ttu-id="7766f-106">Remplace la fonction WordWrap par défaut d’un contrôle d’édition par une fonction WordWrap définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="7766f-106">Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function.</span></span> <span data-ttu-id="7766f-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="7766f-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7766f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7766f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7766f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7766f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7766f-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7766f-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7766f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7766f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7766f-112">Adresse de la fonction WordWrap définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="7766f-112">The address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="7766f-113">Pour plus d’informations sur les lignes de rupture, consultez la description de la fonction de rappel [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .</span><span class="sxs-lookup"><span data-stu-id="7766f-113">For more information about breaking lines, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7766f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7766f-114">Return value</span></span>

<span data-ttu-id="7766f-115">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7766f-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7766f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7766f-116">Remarks</span></span>

<span data-ttu-id="7766f-117">Une fonction WordWrap analyse une mémoire tampon de texte qui contient du texte à envoyer à l’écran, en recherchant le premier mot qui ne tient pas sur la ligne active de l’écran.</span><span class="sxs-lookup"><span data-stu-id="7766f-117">A Wordwrap function scans a text buffer that contains text to be sent to the screen, looking for the first word that does not fit on the current screen line.</span></span> <span data-ttu-id="7766f-118">La fonction WordWrap place ce mot au début de la ligne suivante à l’écran.</span><span class="sxs-lookup"><span data-stu-id="7766f-118">The Wordwrap function places this word at the beginning of the next line on the screen.</span></span>

<span data-ttu-id="7766f-119">Une fonction WordWrap définit le point auquel le système doit couper une ligne de texte pour les contrôles d’édition multiligne, généralement à un espace qui sépare deux mots.</span><span class="sxs-lookup"><span data-stu-id="7766f-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span> <span data-ttu-id="7766f-120">Un contrôle d’édition multiligne ou à une seule ligne peut appeler cette fonction lorsque l’utilisateur appuie sur les touches de direction en combinaison avec la touche CTRL pour déplacer le signe insertion vers le mot suivant ou le mot précédent.</span><span class="sxs-lookup"><span data-stu-id="7766f-120">Either a multiline or a single-line edit control might call this function when the user presses arrow keys in combination with the CTRL key to move the caret to the next word or previous word.</span></span> <span data-ttu-id="7766f-121">La fonction WordWrap par défaut divise une ligne de texte en un espace.</span><span class="sxs-lookup"><span data-stu-id="7766f-121">The default Wordwrap function breaks a line of text at a space character.</span></span> <span data-ttu-id="7766f-122">La fonction définie par l’application peut définir le renvoi à la ligne au niveau d’un trait d’Union ou d’un caractère autre que le caractère d’espace.</span><span class="sxs-lookup"><span data-stu-id="7766f-122">The application-defined function may define the Wordwrap to occur at a hyphen or a character other than the space character.</span></span>

<span data-ttu-id="7766f-123">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7766f-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7766f-124">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="7766f-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7766f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7766f-125">Requirements</span></span>



| <span data-ttu-id="7766f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7766f-126">Requirement</span></span> | <span data-ttu-id="7766f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7766f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7766f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7766f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7766f-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7766f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7766f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7766f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7766f-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7766f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7766f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7766f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7766f-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7766f-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7766f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7766f-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="7766f-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7766f-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7766f-136">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="7766f-136">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="7766f-137">**\_FMTLINES em**</span><span class="sxs-lookup"><span data-stu-id="7766f-137">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="7766f-138">**\_GETWORDBREAKPROC em**</span><span class="sxs-lookup"><span data-stu-id="7766f-138">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
</dt> </dl>

 

