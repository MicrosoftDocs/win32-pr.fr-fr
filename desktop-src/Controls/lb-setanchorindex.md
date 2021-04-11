---
title: Message LB_SETANCHORINDEX (winuser. h)
description: Définit l’élément d’ancrage \ 8212 ; autrement dit, l’élément à partir duquel une sélection multiple démarre. Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- LB_SETANCHORINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105538"
---
# <a name="lb_setanchorindex-message"></a><span data-ttu-id="93a0b-105">\_Message SETANCHORINDEX lb</span><span class="sxs-lookup"><span data-stu-id="93a0b-105">LB\_SETANCHORINDEX message</span></span>

<span data-ttu-id="93a0b-106">Définit l’élément d’ancrage qui est l’élément à partir duquel commence une sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="93a0b-106">Sets the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="93a0b-107">Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="93a0b-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="93a0b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93a0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a0b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93a0b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93a0b-110">Spécifie l’index du nouvel élément d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="93a0b-110">Specifies the index of the new anchor item.</span></span>

<span data-ttu-id="93a0b-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="93a0b-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="93a0b-112">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="93a0b-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="93a0b-113">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="93a0b-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="93a0b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93a0b-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93a0b-115">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="93a0b-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a0b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93a0b-116">Return value</span></span>

<span data-ttu-id="93a0b-117">Si le message est correctement exécuté, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="93a0b-117">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="93a0b-118">Si le message échoue, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="93a0b-118">If the message fails, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a0b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93a0b-119">Requirements</span></span>



| <span data-ttu-id="93a0b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93a0b-120">Requirement</span></span> | <span data-ttu-id="93a0b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="93a0b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a0b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93a0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="93a0b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93a0b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93a0b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93a0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="93a0b-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93a0b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93a0b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="93a0b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a0b-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93a0b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a0b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93a0b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a0b-129">**\_GETANCHORINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="93a0b-129">**LB\_GETANCHORINDEX**</span></span>](lb-getanchorindex.md)
</dt> </dl>

 

 





