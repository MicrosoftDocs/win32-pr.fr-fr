---
title: Message EM_SETLIMITTEXT (winuser. h)
description: 'EM_SETLIMITTEXT message : définit la limite de texte d’un contrôle d’édition.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109747"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="39269-104">\_Message SETLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="39269-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="39269-105">Définit la limite de texte d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="39269-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="39269-106">La limite de texte correspond à la quantité maximale de texte, dans **TCHAR** s, que l’utilisateur peut taper dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="39269-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="39269-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="39269-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="39269-108">Pour les contrôles d’édition et Microsoft Rich Edit 1,0, les octets sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="39269-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="39269-109">Pour Microsoft Rich Edit 2,0 et versions ultérieures, les caractères sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="39269-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="39269-110">Le **message \_ SETLIMITTEXT em** est identique au message [**em \_ LIMITTEXT**](em-limittext.md) .</span><span class="sxs-lookup"><span data-stu-id="39269-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="39269-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39269-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39269-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39269-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39269-113">Nombre maximal de **TCHAR** s que l’utilisateur peut entrer.</span><span class="sxs-lookup"><span data-stu-id="39269-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="39269-114">Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="39269-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="39269-115">Ce nombre n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="39269-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="39269-116">**Contrôles RichEdit :** Si ce paramètre est égal à zéro, la longueur du texte est définie sur 64 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="39269-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="39269-117">Si ce paramètre est égal à zéro, la longueur du texte est définie sur 0x7FFFFFFE caractères pour les contrôles d’édition sur une seule ligne ou sur 1 pour les contrôles d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="39269-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="39269-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39269-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39269-119">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="39269-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39269-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="39269-120">Return value</span></span>

<span data-ttu-id="39269-121">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="39269-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39269-122">Notes </span><span class="sxs-lookup"><span data-stu-id="39269-122">Remarks</span></span>

<span data-ttu-id="39269-123">Le **message \_ SETLIMITTEXT em** limite uniquement le texte que l’utilisateur peut entrer.</span><span class="sxs-lookup"><span data-stu-id="39269-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="39269-124">Elle n’affecte pas le texte déjà présent dans le contrôle d’édition lorsque le message est envoyé, ni la longueur du texte copié dans le contrôle d’édition par le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="39269-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="39269-125">Si une application utilise le message **WM \_ SETTEXT** pour placer plus de texte dans un contrôle d’édition que celui spécifié dans le message **em \_ SETLIMITTEXT** , l’utilisateur peut modifier tout le contenu du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="39269-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="39269-126">Avant l’appel de **em \_ SETLIMITTEXT** , la limite par défaut pour la quantité de texte qu’un utilisateur peut entrer dans un contrôle d’édition est de 32 767 caractères.</span><span class="sxs-lookup"><span data-stu-id="39269-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="39269-127">Pour les contrôles d’édition sur une seule ligne, la limite de texte est soit 0x7FFFFFFE octets, soit la valeur du paramètre *wParam* , selon celle qui est la plus petite.</span><span class="sxs-lookup"><span data-stu-id="39269-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="39269-128">Pour les contrôles d’édition multiligne, cette valeur est soit 1 octet, soit la valeur du paramètre *wParam* , selon celle qui est la plus petite.</span><span class="sxs-lookup"><span data-stu-id="39269-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="39269-129">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="39269-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="39269-130">Utilisez le message [**em \_ EXLIMITTEXT**](em-exlimittext.md) pour les valeurs de longueur de texte supérieures à 64 000.</span><span class="sxs-lookup"><span data-stu-id="39269-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="39269-131">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="39269-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39269-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39269-132">Requirements</span></span>



| <span data-ttu-id="39269-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39269-133">Requirement</span></span> | <span data-ttu-id="39269-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="39269-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39269-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39269-135">Minimum supported client</span></span><br/> | <span data-ttu-id="39269-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39269-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39269-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39269-137">Minimum supported server</span></span><br/> | <span data-ttu-id="39269-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39269-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39269-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="39269-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="39269-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39269-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39269-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39269-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39269-142">**\_GETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="39269-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 

