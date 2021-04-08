---
title: Message LB_ITEMFROMPOINT (winuser. h)
description: Obtient l’index de base zéro de l’élément le plus proche du point spécifié dans une zone de liste.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743021"
---
# <a name="lb_itemfrompoint-message"></a><span data-ttu-id="85558-104">\_Message ITEMFROMPOINT lb</span><span class="sxs-lookup"><span data-stu-id="85558-104">LB\_ITEMFROMPOINT message</span></span>

<span data-ttu-id="85558-105">Obtient l’index de base zéro de l’élément le plus proche du point spécifié dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="85558-105">Gets the zero-based index of the item nearest the specified point in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="85558-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85558-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85558-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85558-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="85558-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85558-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85558-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85558-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la coordonnée x d’un point, par rapport à l’angle supérieur gauche de la zone cliente de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="85558-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

<span data-ttu-id="85558-111">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la coordonnée y d’un point, par rapport à l’angle supérieur gauche de la zone cliente de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="85558-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85558-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85558-112">Return value</span></span>

<span data-ttu-id="85558-113">La valeur de retour contient l’index de l’élément le plus proche dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85558-113">The return value contains the index of the nearest item in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span> <span data-ttu-id="85558-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est égal à zéro si le point spécifié se trouve dans la zone cliente de la zone de liste, ou un point s’il est en dehors de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="85558-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is zero if the specified point is in the client area of the list box, or one if it is outside the client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="85558-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85558-115">Requirements</span></span>



| <span data-ttu-id="85558-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85558-116">Requirement</span></span> | <span data-ttu-id="85558-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="85558-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85558-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85558-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85558-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85558-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="85558-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85558-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85558-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85558-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85558-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="85558-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="85558-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85558-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85558-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85558-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85558-125">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="85558-125">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

