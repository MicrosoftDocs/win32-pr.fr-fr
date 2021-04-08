---
title: Message EM_LINELENGTH (winuser. h)
description: Récupère la longueur, en caractères, d’une ligne dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844045"
---
# <a name="em_linelength-message"></a><span data-ttu-id="4358b-105">\_Message LINELENGTH em</span><span class="sxs-lookup"><span data-stu-id="4358b-105">EM\_LINELENGTH message</span></span>

<span data-ttu-id="4358b-106">Récupère la longueur, en caractères, d’une ligne dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4358b-106">Retrieves the length, in characters, of a line in an edit control.</span></span> <span data-ttu-id="4358b-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="4358b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4358b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4358b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4358b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4358b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4358b-110">Index de caractère d’un caractère de la ligne dont la longueur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="4358b-110">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="4358b-111">Si ce paramètre est supérieur au nombre de caractères dans le contrôle, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="4358b-111">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="4358b-112">Ce paramètre peut être-1.</span><span class="sxs-lookup"><span data-stu-id="4358b-112">This parameter can be -1.</span></span> <span data-ttu-id="4358b-113">Dans ce cas, le message retourne le nombre de caractères non sélectionnés sur les lignes contenant les caractères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="4358b-113">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="4358b-114">Par exemple, si la sélection est étendue à partir du quatrième caractère d’une ligne jusqu’au huitième caractère à partir de la fin de la ligne suivante, la valeur de retour est 10 (trois caractères sur la première ligne et sept sur la suivante).</span><span class="sxs-lookup"><span data-stu-id="4358b-114">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="4358b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4358b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4358b-116">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4358b-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4358b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4358b-117">Return value</span></span>

<span data-ttu-id="4358b-118">Pour les contrôles d’édition multiligne, la valeur de retour est la longueur, dans **TCHAR** s, de la ligne spécifiée par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="4358b-118">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter.</span></span> <span data-ttu-id="4358b-119">Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="4358b-119">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="4358b-120">Elle n’inclut pas le caractère de retour chariot à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="4358b-120">It does not include the carriage-return character at the end of the line.</span></span>

<span data-ttu-id="4358b-121">Pour les contrôles d’édition sur une seule ligne, la valeur de retour est la longueur, dans **TCHAR** s, du texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4358b-121">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="4358b-122">Si *wParam* est supérieur au nombre de caractères dans le contrôle, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="4358b-122">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4358b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4358b-123">Remarks</span></span>

<span data-ttu-id="4358b-124">Utilisez le message [**em \_ LINEINDEX**](em-lineindex.md) pour récupérer un index de caractère pour un numéro de ligne donné au sein d’un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="4358b-124">Use the [**EM\_LINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control.</span></span>

<span data-ttu-id="4358b-125">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4358b-125">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4358b-126">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="4358b-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4358b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4358b-127">Requirements</span></span>



| <span data-ttu-id="4358b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4358b-128">Requirement</span></span> | <span data-ttu-id="4358b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4358b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4358b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4358b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4358b-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4358b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4358b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4358b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4358b-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4358b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4358b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="4358b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4358b-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4358b-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4358b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4358b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4358b-137">**\_LINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="4358b-137">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





