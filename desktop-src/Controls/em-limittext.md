---
title: Message EM_LIMITTEXT (winuser. h)
description: Définit la limite de texte d’un contrôle d’édition.
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- EM_LIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf45f7ee9cfd88a25b78f0bd58911e516c146096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464902"
---
# <a name="em_limittext-message"></a><span data-ttu-id="4056a-104">\_Message LIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="4056a-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="4056a-105">Définit la limite de texte d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4056a-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="4056a-106">La limite de texte correspond à la quantité maximale de texte, dans **TCHAR** s, que l’utilisateur peut taper dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4056a-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="4056a-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="4056a-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="4056a-108">Pour les contrôles d’édition et Microsoft Rich Edit 1,0, les octets sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="4056a-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="4056a-109">Pour Microsoft Rich Edit 2,0 et versions ultérieures, les caractères sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="4056a-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="4056a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4056a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4056a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4056a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4056a-112">Nombre maximal de **TCHAR** s que l’utilisateur peut entrer.</span><span class="sxs-lookup"><span data-stu-id="4056a-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="4056a-113">Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="4056a-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="4056a-114">Ce nombre n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="4056a-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="4056a-115">**Contrôles RichEdit :** Si ce paramètre est égal à zéro, la longueur du texte est définie sur 64 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="4056a-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="4056a-116">Si ce paramètre est égal à zéro, la longueur du texte est définie sur 0x7FFFFFFE caractères pour les contrôles d’édition sur une seule ligne ou sur-1 pour les contrôles d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="4056a-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="4056a-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4056a-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4056a-118">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4056a-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4056a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4056a-119">Return value</span></span>

<span data-ttu-id="4056a-120">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4056a-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4056a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="4056a-121">Remarks</span></span>

<span data-ttu-id="4056a-122">Le **message \_ LIMITTEXT em** limite uniquement le texte que l’utilisateur peut entrer.</span><span class="sxs-lookup"><span data-stu-id="4056a-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="4056a-123">Elle n’affecte pas le texte déjà présent dans le contrôle d’édition lorsque le message est envoyé, ni la longueur du texte copié dans le contrôle d’édition par le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="4056a-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="4056a-124">Si une application utilise le message **WM \_ SETTEXT** pour placer plus de texte dans un contrôle d’édition que celui spécifié dans le message **em \_ LIMITTEXT** , l’utilisateur peut modifier tout le contenu du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4056a-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="4056a-125">Avant l’appel de **em \_ LIMITTEXT** , la limite par défaut pour la quantité de texte qu’un utilisateur peut entrer dans un contrôle d’édition est de 32 767 caractères.</span><span class="sxs-lookup"><span data-stu-id="4056a-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="4056a-126">Pour les contrôles d’édition sur une seule ligne, la limite de texte est soit 0x7FFFFFFE octets, soit la valeur du paramètre *wParam* , selon celle qui est la plus petite.</span><span class="sxs-lookup"><span data-stu-id="4056a-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="4056a-127">Pour les contrôles d’édition multilignes, cette valeur est soit-1 octet, soit la valeur du paramètre *wParam* , selon la valeur la plus petite.</span><span class="sxs-lookup"><span data-stu-id="4056a-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="4056a-128">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4056a-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4056a-129">Utilisez le message [**em \_ EXLIMITTEXT**](em-exlimittext.md) pour les valeurs de longueur de texte supérieures à 64 000.</span><span class="sxs-lookup"><span data-stu-id="4056a-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="4056a-130">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="4056a-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4056a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4056a-131">Requirements</span></span>



| <span data-ttu-id="4056a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4056a-132">Requirement</span></span> | <span data-ttu-id="4056a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4056a-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4056a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4056a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4056a-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4056a-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4056a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4056a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4056a-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4056a-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4056a-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="4056a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4056a-139"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4056a-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4056a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4056a-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="4056a-141">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4056a-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4056a-142">**\_EXLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="4056a-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="4056a-143">**Modifier \_ LimitText**</span><span class="sxs-lookup"><span data-stu-id="4056a-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="4056a-144">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="4056a-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4056a-145">**WM, \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="4056a-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

