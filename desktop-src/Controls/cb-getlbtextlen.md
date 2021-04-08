---
title: Message CB_GETLBTEXTLEN (winuser. h)
description: Obtient la longueur, en caractères, d’une chaîne dans la liste d’une zone de liste déroulante.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942113"
---
# <a name="cb_getlbtextlen-message"></a><span data-ttu-id="d76b7-104">\_Message GETLBTEXTLEN CB</span><span class="sxs-lookup"><span data-stu-id="d76b7-104">CB\_GETLBTEXTLEN message</span></span>

<span data-ttu-id="d76b7-105">Obtient la longueur, en caractères, d’une chaîne dans la liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d76b7-105">Gets the length, in characters, of a string in the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d76b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d76b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76b7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d76b7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d76b7-108">Index de base zéro de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d76b7-108">The zero-based index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="d76b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d76b7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d76b7-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d76b7-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76b7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d76b7-111">Return value</span></span>

<span data-ttu-id="d76b7-112">La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="d76b7-112">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="d76b7-113">Si une chaîne ANSI correspond au nombre d’octets, et s’il s’agit d’une chaîne Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="d76b7-113">If an ANSI string this is the number of bytes, and if it is a Unicode string this is the number of characters.</span></span> <span data-ttu-id="d76b7-114">Dans certaines conditions, cette valeur peut en fait être supérieure à la longueur du texte.</span><span class="sxs-lookup"><span data-stu-id="d76b7-114">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="d76b7-115">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d76b7-115">For more information, see the Remarks section.</span></span>

<span data-ttu-id="d76b7-116">Si le paramètre *wParam* ne spécifie pas d’index valide, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d76b7-116">If the *wParam* parameter does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d76b7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d76b7-117">Remarks</span></span>

<span data-ttu-id="d76b7-118">Dans certaines conditions, la valeur de retour est supérieure à la longueur réelle du texte.</span><span class="sxs-lookup"><span data-stu-id="d76b7-118">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="d76b7-119">Cela se produit avec certains mélanges d’ANSI et Unicode, et est dû au système d’exploitation qui autorise l’existence possible de caractères DBCS (Double-Byte Character Set) dans le texte.</span><span class="sxs-lookup"><span data-stu-id="d76b7-119">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="d76b7-120">Toutefois, la valeur de retour sera toujours au moins égale à la longueur réelle du texte. vous pouvez donc toujours l’utiliser pour guider l’allocation de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d76b7-120">The return value, however, will always be at least as large as the actual length of the text; so you can always use it to guide buffer allocation.</span></span> <span data-ttu-id="d76b7-121">Ce comportement peut se produire lorsqu’une application utilise à la fois des fonctions ANSI et des boîtes de dialogue courantes, qui utilisent Unicode.</span><span class="sxs-lookup"><span data-stu-id="d76b7-121">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="d76b7-122">Pour obtenir la longueur exacte du texte, utilisez les messages [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) , ou la fonction [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="d76b7-122">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d76b7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d76b7-123">Requirements</span></span>



| <span data-ttu-id="d76b7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d76b7-124">Requirement</span></span> | <span data-ttu-id="d76b7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d76b7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76b7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d76b7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d76b7-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d76b7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d76b7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d76b7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d76b7-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d76b7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d76b7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d76b7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d76b7-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d76b7-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d76b7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d76b7-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="d76b7-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d76b7-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d76b7-134">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="d76b7-134">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="d76b7-135">**LB, \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d76b7-135">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="d76b7-136">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d76b7-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d76b7-137">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="d76b7-137">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="d76b7-138">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d76b7-138">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

