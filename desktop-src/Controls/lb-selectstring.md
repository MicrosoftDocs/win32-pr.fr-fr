---
title: Message LB_SELECTSTRING (winuser. h)
description: Recherche un élément qui commence par les caractères d’une chaîne spécifiée dans une zone de liste. Si un élément correspondant est trouvé, l’élément est sélectionné.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466530"
---
# <a name="lb_selectstring-message"></a><span data-ttu-id="7259a-105">\_Message SELECTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="7259a-105">LB\_SELECTSTRING message</span></span>

<span data-ttu-id="7259a-106">Recherche un élément qui commence par les caractères d’une chaîne spécifiée dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="7259a-106">Searches a list box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="7259a-107">Si un élément correspondant est trouvé, l’élément est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7259a-107">If a matching item is found, the item is selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="7259a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7259a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7259a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7259a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7259a-110">Index de base zéro de l'élément précédant le premier élément sur lequel la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="7259a-110">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="7259a-111">Lorsque la recherche atteint le bas de la zone de liste, elle continue à partir du haut de la zone de liste jusqu’à l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="7259a-111">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="7259a-112">Si *wParam* est-1, la zone de liste entière est recherchée à partir du début.</span><span class="sxs-lookup"><span data-stu-id="7259a-112">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="7259a-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7259a-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="7259a-114">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="7259a-114">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="7259a-115">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="7259a-115">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="7259a-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7259a-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7259a-117">Pointeur vers la chaîne terminée par le caractère null qui contient le préfixe à rechercher.</span><span class="sxs-lookup"><span data-stu-id="7259a-117">A pointer to the null-terminated string that contains the prefix for which to search.</span></span> <span data-ttu-id="7259a-118">La recherche étant indépendante de la casse, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.</span><span class="sxs-lookup"><span data-stu-id="7259a-118">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7259a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7259a-119">Return value</span></span>

<span data-ttu-id="7259a-120">Si la recherche réussit, la valeur de retour est l’index de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7259a-120">If the search is successful, the return value is the index of the selected item.</span></span> <span data-ttu-id="7259a-121">Si la recherche échoue, la valeur de retour est LB \_ Err et la sélection actuelle n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="7259a-121">If the search is unsuccessful, the return value is LB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7259a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="7259a-122">Remarks</span></span>

<span data-ttu-id="7259a-123">La zone de liste défile, si nécessaire, pour afficher l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7259a-123">The list box is scrolled, if necessary, to bring the selected item into view.</span></span>

<span data-ttu-id="7259a-124">N’utilisez pas ce message avec une zone de liste avec les [**styles \_ MULTIPLESEL**](list-box-styles.md) ou [**lbs \_ EXTENDEDSEL**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7259a-124">Do not use this message with a list box that has the [**LBS\_MULTIPLESEL**](list-box-styles.md) or the [**LBS\_EXTENDEDSEL**](list-box-styles.md) styles.</span></span>

<span data-ttu-id="7259a-125">Un élément est sélectionné uniquement si ses caractères initiaux à partir du point de départ correspondent aux caractères de la chaîne spécifiée par le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="7259a-125">An item is selected only if its initial characters from the starting point match the characters in the string specified by the *lParam* parameter.</span></span>

<span data-ttu-id="7259a-126">Si la zone de liste a le style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , l’action entreprise par **lb \_ SELECTSTRING** varie selon que le style de [**\_ Tri lbs**](list-box-styles.md) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="7259a-126">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_SELECTSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="7259a-127">Si **le \_ tri de lbs** est utilisé, le système envoie des messages [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste pour déterminer l’élément qui correspond à la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7259a-127">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="7259a-128">Dans le cas contraire, **lb \_ SELECTSTRING** tente de trouver un élément ayant une valeur long (fourni comme paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) ) qui correspond au paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="7259a-128">Otherwise, **LB\_SELECTSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7259a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7259a-129">Requirements</span></span>



| <span data-ttu-id="7259a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7259a-130">Requirement</span></span> | <span data-ttu-id="7259a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7259a-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7259a-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7259a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7259a-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7259a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7259a-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7259a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7259a-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7259a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7259a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="7259a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7259a-137"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7259a-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7259a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7259a-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="7259a-139">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7259a-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7259a-140">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="7259a-140">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="7259a-141">**\_FindString lb**</span><span class="sxs-lookup"><span data-stu-id="7259a-141">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> <dt>

[<span data-ttu-id="7259a-142">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="7259a-142">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





