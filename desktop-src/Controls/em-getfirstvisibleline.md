---
title: Message EM_GETFIRSTVISIBLELINE (winuser. h)
description: Obtient l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508925"
---
# <a name="em_getfirstvisibleline-message"></a><span data-ttu-id="b8eed-105">\_Message GETFIRSTVISIBLELINE em</span><span class="sxs-lookup"><span data-stu-id="b8eed-105">EM\_GETFIRSTVISIBLELINE message</span></span>

<span data-ttu-id="b8eed-106">Obtient l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="b8eed-106">Gets the zero-based index of the uppermost visible line in a multiline edit control.</span></span> <span data-ttu-id="b8eed-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="b8eed-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8eed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8eed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8eed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8eed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8eed-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b8eed-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b8eed-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8eed-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8eed-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b8eed-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8eed-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8eed-113">Return value</span></span>

<span data-ttu-id="b8eed-114">La valeur de retour est l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="b8eed-114">The return value is the zero-based index of the uppermost visible line in a multiline edit control.</span></span>

<span data-ttu-id="b8eed-115">**Contrôles d’édition :** Pour les contrôles d’édition sur une seule ligne, la valeur de retour est l’index de base zéro du premier caractère visible.</span><span class="sxs-lookup"><span data-stu-id="b8eed-115">**Edit controls:** For single-line edit controls, the return value is the zero-based index of the first visible character.</span></span>

<span data-ttu-id="b8eed-116">**Contrôles RichEdit :** Pour les contrôles RichEdit sur une seule ligne, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="b8eed-116">**Rich edit controls:** For single-line rich edit controls, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8eed-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b8eed-117">Remarks</span></span>

<span data-ttu-id="b8eed-118">Le nombre de lignes et la longueur des lignes d’un contrôle d’édition dépendent de la largeur du contrôle et du paramètre de WordWrap actuel.</span><span class="sxs-lookup"><span data-stu-id="b8eed-118">The number of lines and the length of the lines in an edit control depend on the width of the control and the current Wordwrap setting.</span></span>

<span data-ttu-id="b8eed-119">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b8eed-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b8eed-120">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="b8eed-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8eed-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8eed-121">Requirements</span></span>



| <span data-ttu-id="b8eed-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8eed-122">Requirement</span></span> | <span data-ttu-id="b8eed-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8eed-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8eed-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8eed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b8eed-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8eed-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8eed-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8eed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b8eed-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8eed-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8eed-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8eed-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8eed-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8eed-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





