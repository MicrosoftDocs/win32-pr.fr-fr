---
title: DL_CANCELDRAG le code de notification (commctrl. h)
description: Signale que l’utilisateur a annulé une opération glisser en cliquant sur le bouton droit de la souris ou en appuyant sur la touche ÉCHAP.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- Contrôles Windows de code de notification DL_CANCELDRAG
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106690"
---
# <a name="dl_canceldrag-notification-code"></a><span data-ttu-id="9c02d-104">\_Code de notification DL CANCELDRAG</span><span class="sxs-lookup"><span data-stu-id="9c02d-104">DL\_CANCELDRAG notification code</span></span>

<span data-ttu-id="9c02d-105">Signale que l’utilisateur a annulé une opération glisser en cliquant sur le bouton droit de la souris ou en appuyant sur la touche ÉCHAP.</span><span class="sxs-lookup"><span data-stu-id="9c02d-105">Signals that the user has canceled a drag operation by clicking the right mouse button or pressing the ESC key.</span></span> <span data-ttu-id="9c02d-106">Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement.</span><span class="sxs-lookup"><span data-stu-id="9c02d-106">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="9c02d-107">Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="9c02d-107">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9c02d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c02d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c02d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c02d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c02d-110">Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient le code de \_ notification DL CANCELDRAG, le handle de la zone de liste de glissement et la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="9c02d-110">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_CANCELDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c02d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c02d-111">Return value</span></span>

<span data-ttu-id="9c02d-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9c02d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c02d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9c02d-113">Remarks</span></span>

<span data-ttu-id="9c02d-114">En traitant le \_ Code de notification DL CANCELDRAG, une application peut réinitialiser son état interne pour indiquer que le glissement n’est pas appliqué.</span><span class="sxs-lookup"><span data-stu-id="9c02d-114">By processing the DL\_CANCELDRAG notification code, an application can reset its internal state to indicate that dragging is not in effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c02d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c02d-115">Requirements</span></span>



| <span data-ttu-id="9c02d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c02d-116">Requirement</span></span> | <span data-ttu-id="9c02d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c02d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c02d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c02d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9c02d-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c02d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c02d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c02d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9c02d-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c02d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c02d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c02d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c02d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c02d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





