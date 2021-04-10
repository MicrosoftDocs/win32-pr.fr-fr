---
title: Message LB_GETHORIZONTALEXTENT (winuser. h)
description: Obtient la largeur, en pixels, qu’une zone de liste peut faire défiler horizontalement (la largeur avec défilement) si la zone de liste a une barre de défilement horizontale.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942766"
---
# <a name="lb_gethorizontalextent-message"></a><span data-ttu-id="8318f-104">\_Message GETHORIZONTALEXTENT lb</span><span class="sxs-lookup"><span data-stu-id="8318f-104">LB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="8318f-105">Obtient la largeur, en pixels, qu’une zone de liste peut faire défiler horizontalement (la largeur avec défilement) si la zone de liste a une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="8318f-105">Gets the width, in pixels, that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8318f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8318f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8318f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8318f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8318f-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8318f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8318f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8318f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8318f-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8318f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8318f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8318f-111">Return value</span></span>

<span data-ttu-id="8318f-112">La valeur de retour est la largeur de défilement, en pixels, de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="8318f-112">The return value is the scrollable width, in pixels, of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="8318f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8318f-113">Remarks</span></span>

<span data-ttu-id="8318f-114">Pour répondre au message **lb \_ GETHORIZONTALEXTENT** , la zone de liste doit avoir été définie avec le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="8318f-114">To respond to the **LB\_GETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="8318f-115">Si l’application ne définit pas l’étendue horizontale de la zone de liste (à l’aide de [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), l’étendue horizontale par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="8318f-115">If the application does not set the horizontal extent of the list box (using [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), the default horizontal extent is zero.</span></span> <span data-ttu-id="8318f-116">Notez que la zone de liste ne met pas à jour son étendue horizontale de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="8318f-116">Note that the list box does not update its horizontal extent dynamically.</span></span>

## <a name="requirements"></a><span data-ttu-id="8318f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8318f-117">Requirements</span></span>



| <span data-ttu-id="8318f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8318f-118">Requirement</span></span> | <span data-ttu-id="8318f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8318f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8318f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8318f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8318f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8318f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8318f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8318f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8318f-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8318f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8318f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8318f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8318f-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8318f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8318f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8318f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8318f-127">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="8318f-127">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

