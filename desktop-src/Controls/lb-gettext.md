---
title: Message LB_GETTEXT (winuser. h)
description: Obtient une chaîne à partir d’une zone de liste.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466335"
---
# <a name="lb_gettext-message"></a><span data-ttu-id="ecec2-104">LB, \_ message GETTEXT</span><span class="sxs-lookup"><span data-stu-id="ecec2-104">LB\_GETTEXT message</span></span>

<span data-ttu-id="ecec2-105">Obtient une chaîne à partir d’une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="ecec2-105">Gets a string from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecec2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecec2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecec2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecec2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecec2-108">Index de base zéro de la chaîne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ecec2-108">The zero-based index of the string to retrieve.</span></span>

<span data-ttu-id="ecec2-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ecec2-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="ecec2-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="ecec2-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="ecec2-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="ecec2-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="ecec2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecec2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecec2-113">Pointeur vers la mémoire tampon qui recevra la chaîne ; Il s’agit du type **LPTStr** qui est ensuite casté en **lParam**.</span><span class="sxs-lookup"><span data-stu-id="ecec2-113">A pointer to the buffer that will receive the string; it is type **LPTSTR** which is subsequently cast to an **LPARAM**.</span></span> <span data-ttu-id="ecec2-114">La mémoire tampon doit avoir suffisamment d’espace pour la chaîne et un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="ecec2-114">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="ecec2-115">Un [**message \_ GETTEXTLEN**](lb-gettextlen.md) peut être envoyé avant le message d’attente **\_ GETTEXT** pour récupérer la longueur, dans **TCHAR** s, de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="ecec2-115">An [**LB\_GETTEXTLEN**](lb-gettextlen.md) message can be sent before the **LB\_GETTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecec2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ecec2-116">Return value</span></span>

<span data-ttu-id="ecec2-117">La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="ecec2-117">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="ecec2-118">Si *wParam* ne spécifie pas d’index valide, la valeur de retour est lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ecec2-118">If *wParam* does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecec2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ecec2-119">Remarks</span></span>

<span data-ttu-id="ecec2-120">Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , la mémoire tampon vers laquelle pointe le paramètre *lParam* reçoit la valeur associée à l’élément (les données de l’élément).</span><span class="sxs-lookup"><span data-stu-id="ecec2-120">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the buffer pointed to by the *lParam* parameter receives the value associated with the item (the item data).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecec2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecec2-121">Requirements</span></span>



| <span data-ttu-id="ecec2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecec2-122">Requirement</span></span> | <span data-ttu-id="ecec2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecec2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecec2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecec2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ecec2-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecec2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ecec2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecec2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ecec2-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecec2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ecec2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecec2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecec2-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecec2-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecec2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecec2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecec2-131">**\_GETTEXTLEN lb**</span><span class="sxs-lookup"><span data-stu-id="ecec2-131">**LB\_GETTEXTLEN**</span></span>](lb-gettextlen.md)
</dt> </dl>

 

 





