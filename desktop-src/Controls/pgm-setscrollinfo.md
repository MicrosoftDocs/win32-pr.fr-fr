---
title: Message PGM_SETSCROLLINFO (commctrl. h)
description: Définit les paramètres de défilement du contrôle de pagineur, y compris la valeur du délai d’attente, les lignes par délai d’attente et les pixels par ligne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de radiomessagerie \_ SetScrollInfo.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- PGM_SETSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843426"
---
# <a name="pgm_setscrollinfo-message"></a><span data-ttu-id="4b640-105">\_Message SETSCROLLINFO PGM</span><span class="sxs-lookup"><span data-stu-id="4b640-105">PGM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="4b640-106">\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</span><span class="sxs-lookup"><span data-stu-id="4b640-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="4b640-107">Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b640-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="4b640-108">Définit les paramètres de défilement du contrôle de pagineur, y compris la valeur du délai d’attente, les lignes par délai d’attente et les pixels par ligne.</span><span class="sxs-lookup"><span data-stu-id="4b640-108">Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line.</span></span> <span data-ttu-id="4b640-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de [**radiomessagerie \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="4b640-109">You can send this message explicitly or by using the [**Pager\_SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b640-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b640-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b640-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b640-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b640-112">**Uint** qui spécifie la valeur de délai d’attente pour le défilement, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4b640-112">A **UINT** that specifies the timeout value for the scroll, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="4b640-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b640-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b640-114">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **uint** qui spécifie le nombre de lignes à faire défiler par délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="4b640-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **UINT** that specifies the number of lines to scroll per timeout.</span></span> <span data-ttu-id="4b640-115">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **uint** qui spécifie le nombre de pixels par ligne.</span><span class="sxs-lookup"><span data-stu-id="4b640-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **UINT** that specifies the number of pixels per line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b640-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b640-116">Return value</span></span>

<span data-ttu-id="4b640-117">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4b640-117">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="4b640-118">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="4b640-118">Security Considerations</span></span>

<span data-ttu-id="4b640-119">L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="4b640-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b640-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4b640-120">Remarks</span></span>

<span data-ttu-id="4b640-121">La valeur *wParam* Timeout contrôle la vitesse à laquelle le contrôle de pagineur génère des événements de défilement lorsque le contrôle a capturé l’entrée de la souris et que le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="4b640-121">The *wParam* timeout value controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed.</span></span> <span data-ttu-id="4b640-122">Des valeurs plus petites entraînent un défilement plus rapide ; des valeurs plus élevées entraînent un défilement plus lent.</span><span class="sxs-lookup"><span data-stu-id="4b640-122">Smaller values result in faster scrolling; larger values result in slower scrolling.</span></span> <span data-ttu-id="4b640-123">La valeur par défaut est un huitième de la durée du double-clic.</span><span class="sxs-lookup"><span data-stu-id="4b640-123">The default value is one-eighth of the double-click time.</span></span> <span data-ttu-id="4b640-124">Pour plus d’informations, consultez [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span><span class="sxs-lookup"><span data-stu-id="4b640-124">For more information, see [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span></span>

<span data-ttu-id="4b640-125">Par défaut, à chaque événement de défilement, le contrôle de pagineur fait défiler un montant égal à la largeur ou à la hauteur entière du contrôle, selon que le contrôle de pagineur a une orientation horizontale ou verticale.</span><span class="sxs-lookup"><span data-stu-id="4b640-125">By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation.</span></span> <span data-ttu-id="4b640-126">Les valeurs de *lParam* sont utilisées pour remplacer la valeur de défilement par défaut.</span><span class="sxs-lookup"><span data-stu-id="4b640-126">The values in *lParam* are used to override the default scrolling amount.</span></span> <span data-ttu-id="4b640-127">Si les valeurs autres que zéro sont fournies, la valeur de défilement est le produit des deux valeurs (LOWORD (*lParam*) \* HIWORD (*lParam*)).</span><span class="sxs-lookup"><span data-stu-id="4b640-127">If nonzero values are provided, the scrolling amount is the product of the two values (LOWORD(*lParam*) \* HIWORD(*lParam*)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b640-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b640-128">Requirements</span></span>



| <span data-ttu-id="4b640-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b640-129">Requirement</span></span> | <span data-ttu-id="4b640-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b640-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b640-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b640-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4b640-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b640-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b640-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b640-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4b640-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b640-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b640-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b640-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b640-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b640-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b640-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b640-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b640-138">**Radiomessagerie \_ SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="4b640-138">**Pager\_SetScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

