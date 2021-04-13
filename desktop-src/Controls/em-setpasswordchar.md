---
title: Message EM_SETPASSWORDCHAR (winuser. h)
description: Définit ou supprime le caractère de mot de passe pour un contrôle d’édition. Lorsqu’un caractère de mot de passe est défini, ce caractère est affiché à la place des caractères tapés par l’utilisateur. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465054"
---
# <a name="em_setpasswordchar-message"></a><span data-ttu-id="852c1-106">\_Message SETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="852c1-106">EM\_SETPASSWORDCHAR message</span></span>

<span data-ttu-id="852c1-107">Définit ou supprime le caractère de mot de passe pour un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="852c1-107">Sets or removes the password character for an edit control.</span></span> <span data-ttu-id="852c1-108">Lorsqu’un caractère de mot de passe est défini, ce caractère est affiché à la place des caractères tapés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="852c1-108">When a password character is set, that character is displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="852c1-109">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="852c1-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="852c1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="852c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="852c1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="852c1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="852c1-112">Caractère à afficher à la place des caractères tapés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="852c1-112">The character to be displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="852c1-113">Si ce paramètre est égal à zéro, le contrôle supprime le caractère de mot de passe actuel et affiche les caractères tapés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="852c1-113">If this parameter is zero, the control removes the current password character and displays the characters typed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="852c1-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="852c1-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="852c1-115">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="852c1-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="852c1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="852c1-116">Return value</span></span>

<span data-ttu-id="852c1-117">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="852c1-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="852c1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="852c1-118">Remarks</span></span>

<span data-ttu-id="852c1-119">Lorsqu’un contrôle d’édition reçoit le message **\_ SETPASSWORDCHAR em** , le contrôle redessine tous les caractères visibles à l’aide du caractère spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="852c1-119">When an edit control receives the **EM\_SETPASSWORDCHAR** message, the control redraws all visible characters using the character specified by the *wParam* parameter.</span></span> <span data-ttu-id="852c1-120">Si *wParam* est égal à zéro, le contrôle redessine tous les caractères visibles à l’aide des caractères tapés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="852c1-120">If *wParam* is zero, the control redraws all visible characters using the characters typed by the user.</span></span>

<span data-ttu-id="852c1-121">Si un contrôle d’édition est créé avec le style [**\_ de mot de passe es**](edit-control-styles.md) , le caractère de mot de passe par défaut est défini sur un astérisque ( \* ).</span><span class="sxs-lookup"><span data-stu-id="852c1-121">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="852c1-122">Si un contrôle d’édition est créé sans le style **\_ de mot de passe es** , il n’y a pas de caractère de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="852c1-122">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="852c1-123">Le **style \_ de mot de passe es** est supprimé si un message **\_ SETPASSWORDCHAR em** est envoyé avec le paramètre *wParam* défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="852c1-123">The **ES\_PASSWORD** style is removed if an **EM\_SETPASSWORDCHAR** message is sent with the *wParam* parameter set to zero.</span></span>

<span data-ttu-id="852c1-124">**Contrôles d’édition :** Les contrôles d’édition multiligne ne prennent pas en charge le style ou les messages de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="852c1-124">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="852c1-125">**Modification riche :** Pris en charge dans Microsoft Rich Edit 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="852c1-125">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="852c1-126">Les contrôles d’édition sur une seule ligne et sur plusieurs lignes prennent en charge le style et les messages du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="852c1-126">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="852c1-127">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="852c1-127">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="852c1-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="852c1-128">Requirements</span></span>



| <span data-ttu-id="852c1-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="852c1-129">Requirement</span></span> | <span data-ttu-id="852c1-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="852c1-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="852c1-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852c1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="852c1-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="852c1-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="852c1-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852c1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="852c1-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="852c1-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="852c1-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="852c1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="852c1-136"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="852c1-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="852c1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="852c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="852c1-138">**\_GETPASSWORDCHAR em**</span><span class="sxs-lookup"><span data-stu-id="852c1-138">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
</dt> </dl>

 

 





