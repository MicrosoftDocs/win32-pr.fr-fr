---
title: Message TTM_ADJUSTRECT (commctrl. h)
description: Calcule le rectangle d’affichage du texte d’un contrôle ToolTip à partir du rectangle de la fenêtre, ou le rectangle de la fenêtre d’info-bulle nécessaire pour afficher un rectangle d’affichage de texte spécifié.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942152"
---
# <a name="ttm_adjustrect-message"></a><span data-ttu-id="b1c90-104">\_Message atténuation ADJUSTRECT</span><span class="sxs-lookup"><span data-stu-id="b1c90-104">TTM\_ADJUSTRECT message</span></span>

<span data-ttu-id="b1c90-105">Calcule le rectangle d’affichage du texte d’un contrôle ToolTip à partir du rectangle de la fenêtre, ou le rectangle de la fenêtre d’info-bulle nécessaire pour afficher un rectangle d’affichage de texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="b1c90-105">Calculates a tooltip control's text display rectangle from its window rectangle, or the tooltip window rectangle needed to display a specified text display rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1c90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1c90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1c90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1c90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1c90-108">Valeur qui spécifie l’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="b1c90-108">Value that specifies which operation to perform.</span></span> <span data-ttu-id="b1c90-109">Si la **valeur est true**, *lParam* est utilisé pour spécifier un rectangle d’affichage de texte et reçoit le rectangle de fenêtre correspondant.</span><span class="sxs-lookup"><span data-stu-id="b1c90-109">If **TRUE**, *lParam* is used to specify a text-display rectangle and it receives the corresponding window rectangle.</span></span> <span data-ttu-id="b1c90-110">Si la **valeur est false**, *lParam* est utilisé pour spécifier un rectangle de fenêtre et reçoit le rectangle d’affichage de texte correspondant.</span><span class="sxs-lookup"><span data-stu-id="b1c90-110">If **FALSE**, *lParam* is used to specify a window rectangle and it receives the corresponding text display rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b1c90-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1c90-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1c90-112">La structure **Rect** pour contenir un rectangle de fenêtre d’info-bulle ou un rectangle d’affichage de texte.</span><span class="sxs-lookup"><span data-stu-id="b1c90-112">**RECT** structure to hold either a tooltip window rectangle or a text display rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1c90-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1c90-113">Return value</span></span>

<span data-ttu-id="b1c90-114">Retourne une valeur différente de zéro si le rectangle est correctement ajusté et retourne zéro si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="b1c90-114">Returns a nonzero value if the rectangle is successfully adjusted, and returns zero if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1c90-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b1c90-115">Remarks</span></span>

<span data-ttu-id="b1c90-116">Ce message est particulièrement utile lorsque vous souhaitez utiliser un contrôle ToolTip pour afficher le texte intégral d’une chaîne habituellement tronquée.</span><span class="sxs-lookup"><span data-stu-id="b1c90-116">This message is particularly useful when you want to use a tooltip control to display the full text of a string that is usually truncated.</span></span> <span data-ttu-id="b1c90-117">Elle est couramment utilisée avec les contrôles ListView et TreeView.</span><span class="sxs-lookup"><span data-stu-id="b1c90-117">It is commonly used with listview and treeview controls.</span></span> <span data-ttu-id="b1c90-118">En général, vous envoyez ce message en réponse à un code de notification [ttn \_ Show](ttn-show.md) afin que vous puissiez positionner le contrôle ToolTip correctement.</span><span class="sxs-lookup"><span data-stu-id="b1c90-118">You typically send this message in response to a [TTN\_SHOW](ttn-show.md) notification code so that you can position the tooltip control properly.</span></span>

<span data-ttu-id="b1c90-119">Le rectangle de la fenêtre d’info-bulle est un peu plus grand que le rectangle d’affichage de texte qui délimite la chaîne d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="b1c90-119">The tooltip window rectangle is somewhat larger than the text display rectangle that bounds the tooltip string.</span></span> <span data-ttu-id="b1c90-120">L’origine de la fenêtre est également décalée vers le haut et vers la gauche à partir de l’origine du rectangle d’affichage de texte.</span><span class="sxs-lookup"><span data-stu-id="b1c90-120">The window origin is also offset up and to the left from the origin of the text display rectangle.</span></span> <span data-ttu-id="b1c90-121">Pour positionner le rectangle d’affichage du texte, vous devez calculer le rectangle de la fenêtre correspondante et utiliser ce rectangle pour positionner l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="b1c90-121">To position the text display rectangle, you must calculate the corresponding window rectangle and use that rectangle to position the tooltip.</span></span> <span data-ttu-id="b1c90-122">**Atténuation \_ ADJUSTRECT** gère ce calcul pour vous.</span><span class="sxs-lookup"><span data-stu-id="b1c90-122">**TTM\_ADJUSTRECT** handles this calculation for you.</span></span>

<span data-ttu-id="b1c90-123">Si vous affectez à *wParam* la **valeur true**, **atténuation \_ ADJUSTRECT** prend la taille et la position du rectangle d’info-bulle souhaité, et transmet la taille et la position de la fenêtre d’info-bulle nécessaire pour afficher le texte à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1c90-123">If you set *wParam* to **TRUE**, **TTM\_ADJUSTRECT** takes the size and position of the desired tooltip text display rectangle, and passes back the size and position of the tooltip window needed to display the text in the specified position.</span></span> <span data-ttu-id="b1c90-124">Si vous affectez à *wParam* la **valeur false**, vous pouvez spécifier un rectangle de fenêtre d’info-bulle et **atténuation \_ ADJUSTRECT** retourne la taille et la position de son rectangle de texte.</span><span class="sxs-lookup"><span data-stu-id="b1c90-124">If you set *wParam* to **FALSE**, you can specify a tooltip window rectangle and **TTM\_ADJUSTRECT** will return the size and position of its text rectangle.</span></span>

<span data-ttu-id="b1c90-125">Le fragment de code suivant illustre l’utilisation du message **atténuation \_ ADJUSTRECT** pour positionner un contrôle ToolTip afin d’afficher le texte complet de la chaîne d’un contrôle à la place d’une chaîne tronquée.</span><span class="sxs-lookup"><span data-stu-id="b1c90-125">The following code fragment illustrates the use of the **TTM\_ADJUSTRECT** message to position a tooltip control to display the full text of a control's string in place of a truncated string.</span></span> <span data-ttu-id="b1c90-126">La fonction **GetMyItemRect** définie par l’application retourne le rectangle de texte qui sera nécessaire pour afficher le texte info-bulle directement sur la chaîne tronquée.</span><span class="sxs-lookup"><span data-stu-id="b1c90-126">The application-defined **GetMyItemRect** function returns the text rectangle that will be needed to display the tooltip text directly over the truncated string.</span></span> <span data-ttu-id="b1c90-127">Les détails de l’implémentation de cette fonction dépendent du contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="b1c90-127">The details of how this function is implemented will depend on the particular control.</span></span> <span data-ttu-id="b1c90-128">**Atténuation \_ ADJUSTRECT** est utilisé pour envoyer ce rectangle de texte au contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b1c90-128">**TTM\_ADJUSTRECT** is used to send this text rectangle to the tooltip control.</span></span> <span data-ttu-id="b1c90-129">Elle retourne un rectangle de fenêtre de taille et de position approprié qui est ensuite utilisé pour positionner la fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="b1c90-129">It returns an appropriately sized and positioned window rectangle that is then used to position the tooltip window.</span></span>


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a><span data-ttu-id="b1c90-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1c90-130">Requirements</span></span>



| <span data-ttu-id="b1c90-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1c90-131">Requirement</span></span> | <span data-ttu-id="b1c90-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1c90-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c90-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1c90-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b1c90-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1c90-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1c90-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1c90-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b1c90-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1c90-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1c90-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1c90-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1c90-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1c90-138"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





