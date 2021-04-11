---
title: Message CB_SELECTSTRING (winuser. h)
description: Recherche dans la liste d’une zone de liste déroulante un élément qui commence par les caractères d’une chaîne spécifiée. Si un élément correspondant est trouvé, il est sélectionné et copié dans le contrôle d’édition.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032845"
---
# <a name="cb_selectstring-message"></a><span data-ttu-id="3ec75-105">\_Message SELECTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="3ec75-105">CB\_SELECTSTRING message</span></span>

<span data-ttu-id="3ec75-106">Recherche dans la liste d’une zone de liste déroulante un élément qui commence par les caractères d’une chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ec75-106">Searches the list of a combo box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="3ec75-107">Si un élément correspondant est trouvé, il est sélectionné et copié dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="3ec75-107">If a matching item is found, it is selected and copied to the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ec75-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ec75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec75-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ec75-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ec75-110">Index de base zéro de l’élément qui précède le premier élément dans lequel effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="3ec75-110">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="3ec75-111">Lorsque la recherche atteint le bas de la liste, elle continue à partir du haut de la liste jusqu’à l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="3ec75-111">When the search reaches the bottom of the list, it continues from the top of the list back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="3ec75-112">Si *wParam* est-1, la liste entière est recherchée à partir du début.</span><span class="sxs-lookup"><span data-stu-id="3ec75-112">If *wParam* is -1, the entire list is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="3ec75-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ec75-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ec75-114">Pointeur vers la chaîne terminée par le caractère null qui contient les caractères à rechercher.</span><span class="sxs-lookup"><span data-stu-id="3ec75-114">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="3ec75-115">La recherche ne respecte pas la casse, par conséquent, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.</span><span class="sxs-lookup"><span data-stu-id="3ec75-115">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec75-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ec75-116">Return value</span></span>

<span data-ttu-id="3ec75-117">Si la chaîne est trouvée, la valeur de retour est l’index de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3ec75-117">If the string is found, the return value is the index of the selected item.</span></span> <span data-ttu-id="3ec75-118">Si la recherche échoue, la valeur de retour est CB \_ Err et la sélection actuelle n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="3ec75-118">If the search is unsuccessful, the return value is CB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ec75-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3ec75-119">Remarks</span></span>

<span data-ttu-id="3ec75-120">Une chaîne est sélectionnée uniquement si les caractères à partir du point de départ correspondent aux caractères de la chaîne de préfixe.</span><span class="sxs-lookup"><span data-stu-id="3ec75-120">A string is selected only if the characters from the starting point match the characters in the prefix string.</span></span>

<span data-ttu-id="3ec75-121">Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , ce que fait le message **\_ SELECTSTRING CB** varie selon que vous utilisez le style de [**\_ Tri CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec75-121">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_SELECTSTRING** message does depends on whether you use the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="3ec75-122">Si le style de **\_ Tri CBS** est utilisé, le système envoie des messages [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste déroulante pour déterminer l’élément qui correspond à la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ec75-122">If the **CBS\_SORT** style is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="3ec75-123">Si vous n’utilisez pas le style de **\_ Tri CBS** , **CB \_ SELECTSTRING** tente de faire correspondre la valeur **DWORD** à la valeur du paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3ec75-123">If you do not use the **CBS\_SORT** style, **CB\_SELECTSTRING** attempts to match the **DWORD** value against the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec75-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ec75-124">Requirements</span></span>



| <span data-ttu-id="3ec75-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ec75-125">Requirement</span></span> | <span data-ttu-id="3ec75-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec75-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec75-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec75-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec75-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ec75-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ec75-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec75-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec75-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ec75-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ec75-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ec75-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec75-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ec75-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec75-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ec75-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ec75-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3ec75-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3ec75-135">**\_FindString CB**</span><span class="sxs-lookup"><span data-stu-id="3ec75-135">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="3ec75-136">**\_FINDEXACTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="3ec75-136">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="3ec75-137">**\_SETCURSEL CB**</span><span class="sxs-lookup"><span data-stu-id="3ec75-137">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="3ec75-138">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="3ec75-138">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





