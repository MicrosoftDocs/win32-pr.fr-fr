---
title: Message LB_SETTOPINDEX (winuser. h)
description: Garantit que l’élément spécifié dans une zone de liste est visible.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- LB_SETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b415c2369ccc7963a5139ab001159bdba7d6326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105523"
---
# <a name="lb_settopindex-message"></a><span data-ttu-id="cfc76-104">\_Message SETTOPINDEX lb</span><span class="sxs-lookup"><span data-stu-id="cfc76-104">LB\_SETTOPINDEX message</span></span>

<span data-ttu-id="cfc76-105">Garantit que l’élément spécifié dans une zone de liste est visible.</span><span class="sxs-lookup"><span data-stu-id="cfc76-105">Ensures that the specified item in a list box is visible.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfc76-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfc76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc76-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfc76-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfc76-108">Index de base zéro de l’élément dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="cfc76-108">The zero-based index of the item in the list box.</span></span>

<span data-ttu-id="cfc76-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cfc76-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="cfc76-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="cfc76-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="cfc76-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="cfc76-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="cfc76-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfc76-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfc76-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cfc76-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc76-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfc76-114">Return value</span></span>

<span data-ttu-id="cfc76-115">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="cfc76-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc76-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cfc76-116">Remarks</span></span>

<span data-ttu-id="cfc76-117">Le système fait défiler le contenu de la zone de liste afin que l’élément spécifié apparaisse en haut de la zone de liste ou que la plage de défilement maximale ait été atteinte.</span><span class="sxs-lookup"><span data-stu-id="cfc76-117">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc76-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfc76-118">Requirements</span></span>



| <span data-ttu-id="cfc76-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfc76-119">Requirement</span></span> | <span data-ttu-id="cfc76-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfc76-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc76-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfc76-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc76-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfc76-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cfc76-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfc76-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc76-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfc76-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfc76-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfc76-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc76-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfc76-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc76-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc76-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc76-128">**\_GETTOPINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="cfc76-128">**LB\_GETTOPINDEX**</span></span>](lb-gettopindex.md)
</dt> </dl>

 

 





