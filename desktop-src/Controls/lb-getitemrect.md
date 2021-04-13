---
title: Message LB_GETITEMRECT (winuser. h)
description: Obtient les dimensions du rectangle qui délimite un élément de zone de liste tel qu’il est actuellement affiché dans la zone de liste.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- LB_GETITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465039"
---
# <a name="lb_getitemrect-message"></a><span data-ttu-id="ebc6e-104">\_Message GETITEMRECT lb</span><span class="sxs-lookup"><span data-stu-id="ebc6e-104">LB\_GETITEMRECT message</span></span>

<span data-ttu-id="ebc6e-105">Obtient les dimensions du rectangle qui délimite un élément de zone de liste tel qu’il est actuellement affiché dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="ebc6e-105">Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebc6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc6e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebc6e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc6e-108">Index de base zéro de l'élément.</span><span class="sxs-lookup"><span data-stu-id="ebc6e-108">The zero-based index of the item.</span></span>

<span data-ttu-id="ebc6e-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ebc6e-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="ebc6e-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="ebc6e-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="ebc6e-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="ebc6e-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="ebc6e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebc6e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc6e-113">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les coordonnées clientes de l’élément dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="ebc6e-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the client coordinates for the item in the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebc6e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebc6e-114">Return value</span></span>

<span data-ttu-id="ebc6e-115">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ebc6e-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc6e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebc6e-116">Requirements</span></span>



| <span data-ttu-id="ebc6e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebc6e-117">Requirement</span></span> | <span data-ttu-id="ebc6e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebc6e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc6e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebc6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc6e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebc6e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ebc6e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebc6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc6e-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebc6e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebc6e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebc6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebc6e-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebc6e-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc6e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc6e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebc6e-126">[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebc6e-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

