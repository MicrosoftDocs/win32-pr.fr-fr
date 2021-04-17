---
title: Message MCM_GETMINREQRECT (commctrl. h)
description: Récupère la taille minimale requise pour afficher un mois complet dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464878"
---
# <a name="mcm_getminreqrect-message"></a><span data-ttu-id="5b261-105">\_Message GETMINREQRECT MCM</span><span class="sxs-lookup"><span data-stu-id="5b261-105">MCM\_GETMINREQRECT message</span></span>

<span data-ttu-id="5b261-106">Récupère la taille minimale requise pour afficher un mois complet dans un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="5b261-106">Retrieves the minimum size required to display a full month in a month calendar control.</span></span> <span data-ttu-id="5b261-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .</span><span class="sxs-lookup"><span data-stu-id="5b261-107">You can send this message explicitly or by using the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b261-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b261-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b261-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b261-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5b261-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5b261-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5b261-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b261-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b261-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="5b261-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive bounding rectangle information.</span></span> <span data-ttu-id="5b261-113">Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5b261-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b261-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b261-114">Return value</span></span>

<span data-ttu-id="5b261-115">Retourne une valeur différente de zéro et *lParam* reçoit les informations de limite applicables en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="5b261-115">Returns nonzero and *lParam* receives the applicable bounding information if successful.</span></span> <span data-ttu-id="5b261-116">Dans le cas contraire, le message retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="5b261-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b261-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5b261-117">Remarks</span></span>

<span data-ttu-id="5b261-118">La taille de fenêtre minimale requise pour un contrôle de calendrier mensuel dépend de la police actuellement sélectionnée, des styles de contrôle, des métriques système et des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="5b261-118">The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings.</span></span> <span data-ttu-id="5b261-119">Lorsqu’une application modifie tout ce qui affecte la taille de fenêtre minimale, ou traite un message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) , il doit envoyer des **\_ GETMINREQRECT MCM** pour déterminer la nouvelle taille minimale.</span><span class="sxs-lookup"><span data-stu-id="5b261-119">When an application changes anything that affects the minimum window size, or processes a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message, it should send **MCM\_GETMINREQRECT** to determine the new minimum size.</span></span>

> [!Note]  
> <span data-ttu-id="5b261-120">Le rectangle retourné par **MCM \_ GETMINREQRECT** n’inclut pas la largeur de la chaîne « Today », si elle est présente.</span><span class="sxs-lookup"><span data-stu-id="5b261-120">The rectangle returned by **MCM\_GETMINREQRECT** does not include the width of the "Today" string, if it is present.</span></span> <span data-ttu-id="5b261-121">Si le style [**MCS \_ notoday**](month-calendar-control-styles.md) n’est pas défini, votre application doit également récupérer le rectangle qui définit la largeur de chaîne « aujourd’hui » en envoyant un message [**\_ GETMAXTODAYWIDTH MCM**](mcm-getmaxtodaywidth.md) .</span><span class="sxs-lookup"><span data-stu-id="5b261-121">If the [**MCS\_NOTODAY**](month-calendar-control-styles.md) style is not set, your application should also retrieve the rectangle that defines the "Today" string width by sending a [**MCM\_GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) message.</span></span> <span data-ttu-id="5b261-122">Utilisez le plus grand des deux rectangles pour vous assurer que la chaîne « aujourd’hui » n’est pas découpée.</span><span class="sxs-lookup"><span data-stu-id="5b261-122">Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</span></span>

 

<span data-ttu-id="5b261-123">Les membres **supérieurs** et **gauches** de la structure vers laquelle pointe *lParam* seront toujours nuls.</span><span class="sxs-lookup"><span data-stu-id="5b261-123">The **top** and **left** members of the structure pointed to by *lParam* will always be zero.</span></span> <span data-ttu-id="5b261-124">Les membres **droits** et **inférieurs** représentent la valeur minimale pour *CX* et *CY* requis pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="5b261-124">The **right** and **bottom** members represent the minimum *cx* and *cy* required for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b261-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b261-125">Requirements</span></span>



| <span data-ttu-id="5b261-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b261-126">Requirement</span></span> | <span data-ttu-id="5b261-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b261-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b261-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b261-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5b261-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b261-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b261-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b261-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5b261-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b261-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b261-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b261-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b261-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b261-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

