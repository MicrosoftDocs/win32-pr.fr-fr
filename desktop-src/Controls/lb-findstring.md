---
title: Message LB_FINDSTRING (winuser. h)
description: Recherche la première chaîne dans une zone de liste qui commence par la chaîne spécifiée.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466807"
---
# <a name="lb_findstring-message"></a><span data-ttu-id="05161-104">\_Message FindString lb</span><span class="sxs-lookup"><span data-stu-id="05161-104">LB\_FINDSTRING message</span></span>

<span data-ttu-id="05161-105">Recherche la première chaîne dans une zone de liste qui commence par la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="05161-105">Finds the first string in a list box that begins with the specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="05161-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05161-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05161-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05161-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05161-108">Index de base zéro de l'élément précédant le premier élément sur lequel la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="05161-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="05161-109">Lorsque la recherche atteint le bas de la zone de liste, elle continue à effectuer une recherche à partir du haut de la zone de liste jusqu’à l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="05161-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="05161-110">Si *wParam* est-1, la zone de liste entière est recherchée à partir du début.</span><span class="sxs-lookup"><span data-stu-id="05161-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="05161-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="05161-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="05161-112">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="05161-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="05161-113">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="05161-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="05161-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05161-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05161-115">Pointeur vers la chaîne terminée par le caractère null qui contient la chaîne à rechercher.</span><span class="sxs-lookup"><span data-stu-id="05161-115">A pointer to the null-terminated string that contains the string for which to search.</span></span> <span data-ttu-id="05161-116">La recherche étant indépendante de la casse, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.</span><span class="sxs-lookup"><span data-stu-id="05161-116">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05161-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05161-117">Return value</span></span>

<span data-ttu-id="05161-118">La valeur de retour est l’index de l’élément correspondant, ou LB \_ Err si la recherche a échoué.</span><span class="sxs-lookup"><span data-stu-id="05161-118">The return value is the index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="05161-119">Notes</span><span class="sxs-lookup"><span data-stu-id="05161-119">Remarks</span></span>

<span data-ttu-id="05161-120">Si la zone de liste a le style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , l’action entreprise par **lb \_ FindString** varie selon que le style de [**\_ Tri lbs**](list-box-styles.md) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="05161-120">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="05161-121">Si **le \_ tri de lbs** est utilisé, le système envoie des messages [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste pour déterminer l’élément qui correspond à la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="05161-121">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="05161-122">Dans le cas contraire, **lb \_ FindString** tente de trouver un élément ayant une valeur long (fourni comme paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) ) qui correspond au paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="05161-122">Otherwise, **LB\_FINDSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="05161-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05161-123">Requirements</span></span>



| <span data-ttu-id="05161-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05161-124">Requirement</span></span> | <span data-ttu-id="05161-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="05161-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05161-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05161-126">Minimum supported client</span></span><br/> | <span data-ttu-id="05161-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05161-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="05161-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05161-128">Minimum supported server</span></span><br/> | <span data-ttu-id="05161-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05161-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05161-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="05161-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="05161-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05161-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05161-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05161-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05161-133">**\_FINDEXACTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="05161-133">**LB\_FINDSTRINGEXACT**</span></span>](lb-findstringexact.md)
</dt> </dl>

 

 





