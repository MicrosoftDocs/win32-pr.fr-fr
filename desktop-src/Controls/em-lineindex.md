---
title: Message EM_LINEINDEX (winuser. h)
description: Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_LINEINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941961"
---
# <a name="em_lineindex-message-winuserh"></a><span data-ttu-id="28cf0-104">Message EM_LINEINDEX (winuser. h)</span><span class="sxs-lookup"><span data-stu-id="28cf0-104">EM_LINEINDEX message (Winuser.h)</span></span>

<span data-ttu-id="28cf0-105">Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="28cf0-105">Gets the character index of the first character of a specified line in a multiline edit control.</span></span> <span data-ttu-id="28cf0-106">Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="28cf0-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="28cf0-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="28cf0-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="28cf0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28cf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28cf0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28cf0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28cf0-110">Numéro de ligne de base zéro.</span><span class="sxs-lookup"><span data-stu-id="28cf0-110">The zero-based line number.</span></span> <span data-ttu-id="28cf0-111">La valeur-1 spécifie le numéro de la ligne active (la ligne qui contient le signe insertion).</span><span class="sxs-lookup"><span data-stu-id="28cf0-111">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="28cf0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28cf0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28cf0-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="28cf0-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28cf0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28cf0-114">Return value</span></span>

<span data-ttu-id="28cf0-115">La valeur de retour est l’index de caractère de la ligne spécifiée dans le paramètre *wParam* , ou a la valeur-1 si le numéro de ligne spécifié est supérieur au nombre de lignes dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="28cf0-115">The return value is the character index of the line specified in the *wParam* parameter, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="28cf0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="28cf0-116">Remarks</span></span>

<span data-ttu-id="28cf0-117">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="28cf0-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="28cf0-118">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="28cf0-118">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28cf0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28cf0-119">Requirements</span></span>



| <span data-ttu-id="28cf0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28cf0-120">Requirement</span></span> | <span data-ttu-id="28cf0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="28cf0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28cf0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28cf0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="28cf0-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28cf0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="28cf0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28cf0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="28cf0-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28cf0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28cf0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="28cf0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="28cf0-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28cf0-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28cf0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28cf0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28cf0-129">**\_LINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="28cf0-129">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
</dt> </dl>

 

 





