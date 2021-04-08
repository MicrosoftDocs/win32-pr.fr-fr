---
title: Message EM_GETPASSWORDCHAR (winuser. h)
description: Obtient le caractère de mot de passe qu’un contrôle d’édition affiche lorsque l’utilisateur entre du texte. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844134"
---
# <a name="em_getpasswordchar-message"></a><span data-ttu-id="fd3a0-105">\_Message GETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="fd3a0-105">EM\_GETPASSWORDCHAR message</span></span>

<span data-ttu-id="fd3a0-106">Obtient le caractère de mot de passe qu’un contrôle d’édition affiche lorsque l’utilisateur entre du texte.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-106">Gets the password character that an edit control displays when the user enters text.</span></span> <span data-ttu-id="fd3a0-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd3a0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd3a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd3a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd3a0-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd3a0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd3a0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd3a0-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3a0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd3a0-113">Return value</span></span>

<span data-ttu-id="fd3a0-114">La valeur de retour spécifie le caractère à afficher à la place des caractères tapés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-114">The return value specifies the character to be displayed in place of any characters typed by the user.</span></span> <span data-ttu-id="fd3a0-115">Si la valeur de retour est **null**, il n’y a pas de caractère de mot de passe et le contrôle affiche les caractères tapés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-115">If the return value is **NULL**, there is no password character, and the control displays the characters typed by the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3a0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fd3a0-116">Remarks</span></span>

<span data-ttu-id="fd3a0-117">Si un contrôle d’édition est créé avec le style [**\_ de mot de passe es**](edit-control-styles.md) , le caractère de mot de passe par défaut est défini sur un astérisque ( \* ).</span><span class="sxs-lookup"><span data-stu-id="fd3a0-117">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="fd3a0-118">Si un contrôle d’édition est créé sans le style **\_ de mot de passe es** , il n’y a pas de caractère de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-118">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="fd3a0-119">Pour modifier le mot de passe, envoyez le message [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3a0-119">To change the password character, send the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message.</span></span>

<span data-ttu-id="fd3a0-120">**Contrôles d’édition :** Les contrôles d’édition multiligne ne prennent pas en charge le style ou les messages de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-120">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="fd3a0-121">**Modification riche :** Pris en charge dans Microsoft Rich Edit 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-121">**Rich edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="fd3a0-122">Les contrôles d’édition sur une seule ligne et sur plusieurs lignes prennent en charge le style et les messages du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-122">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="fd3a0-123">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="fd3a0-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3a0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd3a0-124">Requirements</span></span>



| <span data-ttu-id="fd3a0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd3a0-125">Requirement</span></span> | <span data-ttu-id="fd3a0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd3a0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3a0-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd3a0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3a0-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd3a0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fd3a0-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd3a0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3a0-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd3a0-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fd3a0-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd3a0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd3a0-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd3a0-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd3a0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd3a0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3a0-134">**\_SETPASSWORDCHAR em**</span><span class="sxs-lookup"><span data-stu-id="fd3a0-134">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
</dt> </dl>

 

 





