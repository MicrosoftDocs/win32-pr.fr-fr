---
title: Message CB_FINDSTRINGEXACT (winuser. h)
description: Recherche la première chaîne de zone de liste dans une zone de liste déroulante qui correspond à la chaîne spécifiée dans le paramètre lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327174"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="1b016-104">\_Message FINDEXACTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="1b016-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="1b016-105">Recherche la première chaîne de zone de liste dans une zone de liste déroulante qui correspond à la chaîne spécifiée dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1b016-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b016-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b016-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b016-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b016-108">Index de base zéro de l’élément qui précède le premier élément dans lequel effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="1b016-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="1b016-109">Lorsque la recherche atteint le bas de la zone de liste, elle continue à partir du haut de la zone de liste jusqu’à l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1b016-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="1b016-110">Si *wParam* est-1, la zone de liste entière est recherchée à partir du début.</span><span class="sxs-lookup"><span data-stu-id="1b016-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="1b016-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b016-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b016-112">Pointeur vers la chaîne terminée par le caractère null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="1b016-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="1b016-113">La recherche ne respecte pas la casse, par conséquent, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.</span><span class="sxs-lookup"><span data-stu-id="1b016-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b016-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b016-114">Return value</span></span>

<span data-ttu-id="1b016-115">La valeur de retour est l’index de base zéro de l’élément correspondant.</span><span class="sxs-lookup"><span data-stu-id="1b016-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="1b016-116">Si la recherche échoue, il s’agit de l' \_ erreur CB.</span><span class="sxs-lookup"><span data-stu-id="1b016-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b016-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b016-117">Remarks</span></span>

<span data-ttu-id="1b016-118">Cette fonction est réussie uniquement si la chaîne spécifiée et un élément de zone de liste déroulante ont la même longueur (à l’exception du caractère null de fin) et les mêmes caractères.</span><span class="sxs-lookup"><span data-stu-id="1b016-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="1b016-119">Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , les fonctionnalités du message **CB \_ FindExactString** varient selon que votre application utilise ou non le style de [**\_ Tri CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1b016-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="1b016-120">Si vous utilisez le style de **\_ Tri CBS** , les messages [**WM \_ COMPAREITEM**](wm-compareitem.md) sont envoyés au propriétaire de la zone de liste déroulante pour déterminer quel élément correspond à la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1b016-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="1b016-121">Si vous n’utilisez pas le style de **\_ Tri CBS** , le message **CB \_ FindExactString** recherche un élément de liste qui correspond à la valeur du paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1b016-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b016-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b016-122">Requirements</span></span>



| <span data-ttu-id="1b016-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b016-123">Requirement</span></span> | <span data-ttu-id="1b016-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b016-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b016-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b016-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1b016-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b016-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1b016-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b016-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1b016-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b016-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b016-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b016-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b016-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b016-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b016-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b016-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b016-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1b016-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1b016-133">**\_FindString CB**</span><span class="sxs-lookup"><span data-stu-id="1b016-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="1b016-134">**\_SELECTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="1b016-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="1b016-135">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="1b016-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





