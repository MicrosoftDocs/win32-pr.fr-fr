---
title: Message EM_LINEFROMCHAR (winuser. h)
description: Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_LINEFROMCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103373"
---
# <a name="em_linefromchar-message"></a><span data-ttu-id="a01d6-104">\_Message LINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="a01d6-104">EM\_LINEFROMCHAR message</span></span>

<span data-ttu-id="a01d6-105">Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="a01d6-105">Gets the index of the line that contains the specified character index in a multiline edit control.</span></span> <span data-ttu-id="a01d6-106">Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="a01d6-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="a01d6-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="a01d6-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a01d6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a01d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01d6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a01d6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a01d6-110">Index de caractère du caractère contenu dans la ligne dont le nombre doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="a01d6-110">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="a01d6-111">Si ce paramètre a la valeur-1, **em \_ LINEFROMCHAR** récupère le numéro de ligne de la ligne active (la ligne qui contient le signe insertion) ou, s’il y a une sélection, le numéro de ligne de la ligne contenant le début de la sélection.</span><span class="sxs-lookup"><span data-stu-id="a01d6-111">If this parameter is -1, **EM\_LINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="a01d6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a01d6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a01d6-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a01d6-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01d6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a01d6-114">Return value</span></span>

<span data-ttu-id="a01d6-115">La valeur de retour est le numéro de ligne de base zéro de la ligne contenant l’index de caractère spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a01d6-115">The return value is the zero-based line number of the line containing the character index specified by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01d6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a01d6-116">Remarks</span></span>

<span data-ttu-id="a01d6-117">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a01d6-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a01d6-118">Si l’index de caractère est supérieur à 64 000, utilisez le message [**em \_ EXLINEFROMCHAR**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="a01d6-118">If the character index is greater than 64,000, use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span> <span data-ttu-id="a01d6-119">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="a01d6-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a01d6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a01d6-120">Requirements</span></span>



| <span data-ttu-id="a01d6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a01d6-121">Requirement</span></span> | <span data-ttu-id="a01d6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a01d6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01d6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a01d6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a01d6-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a01d6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a01d6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a01d6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a01d6-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a01d6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a01d6-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a01d6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a01d6-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a01d6-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01d6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a01d6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a01d6-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a01d6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a01d6-131">**\_EXLINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="a01d6-131">**EM\_EXLINEFROMCHAR**</span></span>](em-exlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="a01d6-132">**\_LINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="a01d6-132">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





