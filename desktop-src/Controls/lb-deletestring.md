---
title: Message LB_DELETESTRING (winuser. h)
description: Supprime une chaîne dans une zone de liste.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844037"
---
# <a name="lb_deletestring-message"></a><span data-ttu-id="5a501-104">\_Message DELETESTRING lb</span><span class="sxs-lookup"><span data-stu-id="5a501-104">LB\_DELETESTRING message</span></span>

<span data-ttu-id="5a501-105">Supprime une chaîne dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="5a501-105">Deletes a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a501-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a501-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a501-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a501-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a501-108">Index de base zéro de la chaîne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="5a501-108">The zero-based index of the string to be deleted.</span></span>

<span data-ttu-id="5a501-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5a501-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5a501-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="5a501-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5a501-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="5a501-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5a501-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a501-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a501-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5a501-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a501-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a501-114">Return value</span></span>

<span data-ttu-id="5a501-115">La valeur de retour est le nombre de chaînes restantes dans la liste.</span><span class="sxs-lookup"><span data-stu-id="5a501-115">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="5a501-116">La valeur de retour est LB \_ Err si le paramètre *wParam* spécifie un index supérieur au nombre d’éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="5a501-116">The return value is LB\_ERR if the *wParam* parameter specifies an index greater than the number of items in the list.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a501-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5a501-117">Remarks</span></span>

<span data-ttu-id="5a501-118">Si une application crée la zone de liste avec un style owner-drawn, mais sans le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le système envoie un message [**WM \_ DELETEITEM**](wm-deleteitem.md) au propriétaire de la zone de liste afin que l’application puisse libérer toutes les données supplémentaires associées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="5a501-118">If an application creates the list box with an owner-drawn style but without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the list box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a501-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a501-119">Requirements</span></span>



| <span data-ttu-id="5a501-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a501-120">Requirement</span></span> | <span data-ttu-id="5a501-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a501-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a501-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a501-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5a501-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a501-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a501-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a501-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5a501-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a501-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a501-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a501-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a501-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a501-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a501-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a501-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a501-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5a501-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5a501-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="5a501-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5a501-131">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="5a501-131">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="5a501-132">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="5a501-132">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





