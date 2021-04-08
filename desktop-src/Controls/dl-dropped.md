---
title: DL_DROPPED le code de notification (commctrl. h)
description: Signale que l’utilisateur a terminé une opération glisser-déplacer en relâchant le bouton gauche de la souris. Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez faire glisser des messages de zone de liste.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- Contrôles Windows de code de notification DL_DROPPED
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844497"
---
# <a name="dl_dropped-notification-code"></a><span data-ttu-id="56400-106">Code de notification de DL \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="56400-106">DL\_DROPPED notification code</span></span>

<span data-ttu-id="56400-107">Signale que l’utilisateur a terminé une opération glisser-déplacer en relâchant le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="56400-107">Signals that the user has completed a drag operation by releasing the left mouse button.</span></span> <span data-ttu-id="56400-108">Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement.</span><span class="sxs-lookup"><span data-stu-id="56400-108">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="56400-109">Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="56400-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="56400-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56400-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56400-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56400-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56400-112">Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient le code de \_ notification supprimé DL, le handle de la zone de liste de glissement et la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="56400-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DROPPED notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56400-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56400-113">Return value</span></span>

<span data-ttu-id="56400-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="56400-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56400-115">Notes</span><span class="sxs-lookup"><span data-stu-id="56400-115">Remarks</span></span>

<span data-ttu-id="56400-116">Ce code de notification est normalement traité en insérant l’élément déplacé dans la liste devant l’élément sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="56400-116">This notification code is normally processed by inserting the item being dragged into the list in front of the item under the cursor.</span></span> <span data-ttu-id="56400-117">Pour récupérer l’index de l’élément à la position du curseur, utilisez la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="56400-117">To retrieve the index of the item at the cursor position, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="56400-118">Notez que le code de notification de la liste de distribution \_ supprimée est envoyé même si le curseur ne se trouve pas sur un élément de liste.</span><span class="sxs-lookup"><span data-stu-id="56400-118">Note that the DL\_DROPPED notification code is sent even if the cursor is not on a list item.</span></span> <span data-ttu-id="56400-119">Dans ce cas, **LBItemFromPt** retourne-1.</span><span class="sxs-lookup"><span data-stu-id="56400-119">In that case, **LBItemFromPt** returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="56400-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56400-120">Requirements</span></span>



| <span data-ttu-id="56400-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56400-121">Requirement</span></span> | <span data-ttu-id="56400-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="56400-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56400-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56400-123">Minimum supported client</span></span><br/> | <span data-ttu-id="56400-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56400-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56400-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56400-125">Minimum supported server</span></span><br/> | <span data-ttu-id="56400-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56400-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56400-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="56400-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="56400-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56400-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





