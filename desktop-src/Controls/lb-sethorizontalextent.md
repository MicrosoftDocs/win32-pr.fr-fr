---
title: Message LB_SETHORIZONTALEXTENT (winuser. h)
description: Définit la largeur, en pixels, à laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844110"
---
# <a name="lb_sethorizontalextent-message"></a><span data-ttu-id="e6dbd-104">\_Message SETHORIZONTALEXTENT lb</span><span class="sxs-lookup"><span data-stu-id="e6dbd-104">LB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="e6dbd-105">Définit la largeur, en pixels, à laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement).</span><span class="sxs-lookup"><span data-stu-id="e6dbd-105">Sets the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="e6dbd-106">Si la largeur de la zone de liste est inférieure à cette valeur, la barre de défilement horizontale fait défiler horizontalement les éléments de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="e6dbd-107">Si la largeur de la zone de liste est supérieure ou égale à cette valeur, la barre de défilement horizontale est masquée.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6dbd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6dbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6dbd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6dbd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6dbd-110">Spécifie le nombre de pixels utilisés pour faire défiler la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-110">Specifies the number of pixels by which the list box can be scrolled.</span></span>

<span data-ttu-id="e6dbd-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span>

</dd> <dt>

<span data-ttu-id="e6dbd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6dbd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6dbd-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6dbd-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6dbd-114">Return value</span></span>

<span data-ttu-id="e6dbd-115">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6dbd-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e6dbd-116">Remarks</span></span>

<span data-ttu-id="e6dbd-117">Pour répondre au message **lb \_ SETHORIZONTALEXTENT** , la zone de liste doit avoir été définie avec le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="e6dbd-117">To respond to the **LB\_SETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="e6dbd-118">Notez qu’une zone de liste ne met pas à jour son étendue horizontale de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-118">Note that a list box does not update its horizontal extent dynamically.</span></span>

<span data-ttu-id="e6dbd-119">Ce message n’a aucun effet sur une zone de liste à plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="e6dbd-119">This message has no effect on a multiple-column list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6dbd-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6dbd-120">Requirements</span></span>



| <span data-ttu-id="e6dbd-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6dbd-121">Requirement</span></span> | <span data-ttu-id="e6dbd-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6dbd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6dbd-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6dbd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6dbd-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6dbd-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6dbd-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6dbd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6dbd-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6dbd-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6dbd-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6dbd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6dbd-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6dbd-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6dbd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6dbd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6dbd-130">**\_GETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="e6dbd-130">**LB\_GETHORIZONTALEXTENT**</span></span>](lb-gethorizontalextent.md)
</dt> </dl>

 

