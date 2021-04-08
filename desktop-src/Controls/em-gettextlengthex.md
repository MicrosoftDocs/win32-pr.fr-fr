---
title: Message EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcule la longueur du texte de différentes façons. Elle est généralement appelée avant la création d’une mémoire tampon pour recevoir le texte du contrôle.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843481"
---
# <a name="em_gettextlengthex-message"></a><span data-ttu-id="9f13f-105">\_Message GETTEXTLENGTHEX em</span><span class="sxs-lookup"><span data-stu-id="9f13f-105">EM\_GETTEXTLENGTHEX message</span></span>

<span data-ttu-id="9f13f-106">Calcule la longueur du texte de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="9f13f-106">Calculates text length in various ways.</span></span> <span data-ttu-id="9f13f-107">Elle est généralement appelée avant la création d’une mémoire tampon pour recevoir le texte du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9f13f-107">It is usually called before creating a buffer to receive the text from the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f13f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f13f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f13f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f13f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f13f-110">Pointeur vers une structure [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) qui reçoit les informations de longueur de texte.</span><span class="sxs-lookup"><span data-stu-id="9f13f-110">Pointer to a [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure that receives the text length information.</span></span>

</dd> <dt>

<span data-ttu-id="9f13f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f13f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f13f-112">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="9f13f-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f13f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f13f-113">Return value</span></span>

<span data-ttu-id="9f13f-114">Le message retourne le nombre de **TCHAR** s dans le contrôle d’édition, en fonction du paramètre des indicateurs dans la structure [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) .</span><span class="sxs-lookup"><span data-stu-id="9f13f-114">The message returns the number of **TCHAR** s in the edit control, depending on the setting of the flags in the [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure.</span></span> <span data-ttu-id="9f13f-115">Si des indicateurs incompatibles ont été définis dans le membre **Flags** , le message retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9f13f-115">If incompatible flags were set in the **flags** member, the message returns E\_INVALIDARG .</span></span>

## <a name="remarks"></a><span data-ttu-id="9f13f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9f13f-116">Remarks</span></span>

<span data-ttu-id="9f13f-117">Ce message est un moyen rapide et facile de déterminer le nombre de caractères dans la version Unicode du contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9f13f-117">This message is a fast and easy way to determine the number of characters in the Unicode version of the rich edit control.</span></span> <span data-ttu-id="9f13f-118">Toutefois, pour une page de codes cible non Unicode, vous allez potentiellement convertir en une combinaison de caractères codés sur un octet et sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="9f13f-118">However, for a non-Unicode target code page you will potentially be converting to a combination of single-byte and double-byte characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f13f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f13f-119">Requirements</span></span>



| <span data-ttu-id="9f13f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f13f-120">Requirement</span></span> | <span data-ttu-id="9f13f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f13f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f13f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f13f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f13f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f13f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f13f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f13f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f13f-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f13f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f13f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f13f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f13f-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f13f-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f13f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f13f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f13f-129">**GETTEXTLENGTHEX**</span><span class="sxs-lookup"><span data-stu-id="9f13f-129">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





