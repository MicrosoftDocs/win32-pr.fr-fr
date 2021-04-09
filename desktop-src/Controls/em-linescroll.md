---
title: Message EM_LINESCROLL (winuser. h)
description: Fait défiler le texte dans un contrôle d’édition multiligne.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033055"
---
# <a name="em_linescroll-message"></a><span data-ttu-id="9140e-104">\_Message LINESCROLL em</span><span class="sxs-lookup"><span data-stu-id="9140e-104">EM\_LINESCROLL message</span></span>

<span data-ttu-id="9140e-105">Fait défiler le texte dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="9140e-105">Scrolls the text in a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9140e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9140e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9140e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9140e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9140e-108">**Contrôles d’édition :** Nombre de caractères à faire défiler horizontalement.</span><span class="sxs-lookup"><span data-stu-id="9140e-108">**Edit controls:** The number of characters to scroll horizontally.</span></span>

<span data-ttu-id="9140e-109">**Contrôles RichEdit :** Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="9140e-109">**Rich edit controls:** This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9140e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9140e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9140e-111">Nombre de lignes à faire défiler verticalement.</span><span class="sxs-lookup"><span data-stu-id="9140e-111">The number of lines to scroll vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9140e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9140e-112">Return value</span></span>

<span data-ttu-id="9140e-113">Si le message est envoyé à un contrôle d’édition multiligne, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="9140e-113">If the message is sent to a multiline edit control, the return value is **TRUE**.</span></span>

<span data-ttu-id="9140e-114">Si le message est envoyé à un contrôle d’édition sur une seule ligne, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="9140e-114">If the message is sent to a single-line edit control, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9140e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9140e-115">Remarks</span></span>

<span data-ttu-id="9140e-116">Le contrôle ne défile pas verticalement après la dernière ligne de texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="9140e-116">The control does not scroll vertically past the last line of text in the edit control.</span></span> <span data-ttu-id="9140e-117">Si la ligne actuelle plus le nombre de lignes spécifié par le paramètre *lParam* dépasse le nombre total de lignes dans le contrôle d’édition, la valeur est ajustée de sorte que la dernière ligne du contrôle d’édition soit défilante en haut de la fenêtre Modifier-contrôle.</span><span class="sxs-lookup"><span data-stu-id="9140e-117">If the current line plus the number of lines specified by the *lParam* parameter exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.</span></span>

<span data-ttu-id="9140e-118">**Contrôles d’édition :** Le **message \_ LINESCROLL em** fait défiler le texte verticalement ou horizontalement dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="9140e-118">**Edit controls:** The **EM\_LINESCROLL** message scrolls the text vertically or horizontally in a multiline edit control.</span></span> <span data-ttu-id="9140e-119">Le **message \_ LINESCROLL em** peut être utilisé pour faire défiler horizontalement le dernier caractère d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="9140e-119">The **EM\_LINESCROLL** message can be used to scroll horizontally past the last character of any line.</span></span>

<span data-ttu-id="9140e-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9140e-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9140e-121">Le **message \_ LINESCROLL em** fait défiler le texte verticalement dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="9140e-121">The **EM\_LINESCROLL** message scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="9140e-122">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="9140e-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9140e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9140e-123">Requirements</span></span>



| <span data-ttu-id="9140e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9140e-124">Requirement</span></span> | <span data-ttu-id="9140e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9140e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9140e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9140e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9140e-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9140e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9140e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9140e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9140e-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9140e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9140e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="9140e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9140e-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9140e-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





