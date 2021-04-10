---
title: Message LB_GETTEXTLEN (winuser. h)
description: Obtient la longueur d’une chaîne dans une zone de liste.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- LB_GETTEXTLEN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103484"
---
# <a name="lb_gettextlen-message"></a><span data-ttu-id="b8751-104">\_Message GETTEXTLEN lb</span><span class="sxs-lookup"><span data-stu-id="b8751-104">LB\_GETTEXTLEN message</span></span>

<span data-ttu-id="b8751-105">Obtient la longueur d’une chaîne dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="b8751-105">Gets the length of a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8751-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8751-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8751-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8751-108">Index de base zéro de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b8751-108">The zero-based index of the string.</span></span>

<span data-ttu-id="b8751-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b8751-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="b8751-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="b8751-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="b8751-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="b8751-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="b8751-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8751-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8751-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b8751-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8751-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8751-114">Return value</span></span>

<span data-ttu-id="b8751-115">La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="b8751-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="b8751-116">Dans certaines conditions, cette valeur peut en fait être supérieure à la longueur du texte.</span><span class="sxs-lookup"><span data-stu-id="b8751-116">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="b8751-117">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="b8751-117">For more information, see the following Remarks section.</span></span>

<span data-ttu-id="b8751-118">Si le paramètre *wParam* ne spécifie pas d’index valide, la valeur de retour est lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="b8751-118">If the *wParam* parameter does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8751-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b8751-119">Remarks</span></span>

<span data-ttu-id="b8751-120">Dans certaines conditions, la valeur de retour est supérieure à la longueur réelle du texte.</span><span class="sxs-lookup"><span data-stu-id="b8751-120">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="b8751-121">Cela se produit avec certains mélanges d’ANSI et Unicode, et est dû au système d’exploitation qui autorise l’existence possible de caractères DBCS (Double-Byte Character Set) dans le texte.</span><span class="sxs-lookup"><span data-stu-id="b8751-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="b8751-122">Toutefois, la valeur de retour sera toujours au moins égale à la longueur réelle du texte. vous pouvez donc toujours l’utiliser pour guider l’allocation de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b8751-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="b8751-123">Ce comportement peut se produire lorsqu’une application utilise à la fois des fonctions ANSI et des boîtes de dialogue courantes, qui utilisent Unicode.</span><span class="sxs-lookup"><span data-stu-id="b8751-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="b8751-124">Pour obtenir la longueur exacte du texte, utilisez les messages [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) , ou la fonction [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="b8751-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="b8751-125">Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , la valeur de retour est toujours la taille, en octets, d’un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b8751-125">If the list box has an owner-drawn style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the return value is always the size, in bytes, of a **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8751-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8751-126">Requirements</span></span>



| <span data-ttu-id="b8751-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8751-127">Requirement</span></span> | <span data-ttu-id="b8751-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8751-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8751-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8751-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b8751-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8751-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8751-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8751-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b8751-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8751-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8751-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8751-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8751-134"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8751-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8751-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8751-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8751-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b8751-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b8751-137">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="b8751-137">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="b8751-138">**LB, \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="b8751-138">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="b8751-139">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="b8751-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b8751-140">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="b8751-140">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="b8751-141">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="b8751-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

