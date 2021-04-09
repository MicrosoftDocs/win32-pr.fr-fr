---
title: Message LB_FINDSTRINGEXACT (winuser. h)
description: Recherche la première chaîne de zone de liste qui correspond exactement à la chaîne spécifiée, sauf que la recherche ne respecte pas la casse.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- LB_FINDSTRINGEXACT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033208"
---
# <a name="lb_findstringexact-message"></a><span data-ttu-id="010fe-104">\_Message FINDEXACTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="010fe-104">LB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="010fe-105">Recherche la première chaîne de zone de liste qui correspond exactement à la chaîne spécifiée, sauf que la recherche ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="010fe-105">Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive.</span></span>

## <a name="parameters"></a><span data-ttu-id="010fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="010fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="010fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="010fe-108">Index de base zéro de l'élément précédant le premier élément sur lequel la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="010fe-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="010fe-109">Lorsque la recherche atteint le bas de la zone de liste, elle continue à effectuer une recherche à partir du haut de la zone de liste jusqu’à l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="010fe-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="010fe-110">Si *wParam* est-1, la zone de liste entière est recherchée à partir du début.</span><span class="sxs-lookup"><span data-stu-id="010fe-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="010fe-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="010fe-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="010fe-112">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="010fe-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="010fe-113">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="010fe-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="010fe-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="010fe-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="010fe-115">Pointeur vers la chaîne terminée par le caractère null à rechercher.</span><span class="sxs-lookup"><span data-stu-id="010fe-115">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="010fe-116">La recherche ne respecte pas la casse, par conséquent, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.</span><span class="sxs-lookup"><span data-stu-id="010fe-116">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010fe-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="010fe-117">Return value</span></span>

<span data-ttu-id="010fe-118">La valeur de retour est l’index de base zéro de l’élément correspondant, ou LB \_ Err si la recherche a échoué.</span><span class="sxs-lookup"><span data-stu-id="010fe-118">The return value is the zero-based index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="010fe-119">Notes</span><span class="sxs-lookup"><span data-stu-id="010fe-119">Remarks</span></span>

<span data-ttu-id="010fe-120">Cette fonction est réussie uniquement si la chaîne spécifiée et un élément de zone de liste ont la même longueur (à l’exception de la valeur null à la fin de la chaîne spécifiée) et ont exactement les mêmes caractères.</span><span class="sxs-lookup"><span data-stu-id="010fe-120">This function is only successful if the specified string and a list box item have the same length (except for the null at the end of the specified string) and have exactly the same characters.</span></span>

<span data-ttu-id="010fe-121">Si la zone de liste a le style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , l’action entreprise par **lb \_ FindExactString** varie selon que le style de [**\_ Tri lbs**](list-box-styles.md) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="010fe-121">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRINGEXACT** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="010fe-122">Si **le \_ tri de lbs** est utilisé, le système envoie des messages [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste pour déterminer l’élément qui correspond à la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="010fe-122">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="010fe-123">Dans le cas contraire, **lb \_ FindExactString** tente de trouver un élément ayant une valeur long (fourni comme paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) ) qui correspond au paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="010fe-123">Otherwise, **LB\_FINDSTRINGEXACT** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="010fe-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="010fe-124">Requirements</span></span>



| <span data-ttu-id="010fe-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="010fe-125">Requirement</span></span> | <span data-ttu-id="010fe-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="010fe-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010fe-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="010fe-127">Minimum supported client</span></span><br/> | <span data-ttu-id="010fe-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="010fe-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="010fe-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="010fe-129">Minimum supported server</span></span><br/> | <span data-ttu-id="010fe-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="010fe-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="010fe-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="010fe-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="010fe-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="010fe-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010fe-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="010fe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010fe-134">**\_FindString lb**</span><span class="sxs-lookup"><span data-stu-id="010fe-134">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> </dl>

 

 





