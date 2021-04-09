---
title: TVN_BEGINRDRAG le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View à propos de l’initiation d’une opération de glisser-déplacer impliquant le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- Contrôles Windows de code de notification TVN_BEGINRDRAG
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942752"
---
# <a name="tvn_beginrdrag-notification-code"></a><span data-ttu-id="7b1be-105">\_Code de notification TVN BEGINRDRAG</span><span class="sxs-lookup"><span data-stu-id="7b1be-105">TVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="7b1be-106">Avertit une fenêtre parente d’un contrôle Tree-View à propos de l’initiation d’une opération de glisser-déplacer impliquant le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="7b1be-106">Notifies a tree-view control's parent window about the initiation of a drag-and-drop operation involving the right mouse button.</span></span> <span data-ttu-id="7b1be-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7b1be-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="7b1be-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b1be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b1be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b1be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b1be-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="7b1be-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="7b1be-111">Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides dans les membres **hitem**, **State** et **lParam** sur l’élément à faire glisser.</span><span class="sxs-lookup"><span data-stu-id="7b1be-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information in the **hItem**, **state**, and **lParam** members about the item to be dragged.</span></span> <span data-ttu-id="7b1be-112">Le membre **ptDrag** spécifie les coordonnées d’écran actuelles de la souris.</span><span class="sxs-lookup"><span data-stu-id="7b1be-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b1be-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b1be-113">Return value</span></span>

<span data-ttu-id="7b1be-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="7b1be-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b1be-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b1be-115">Requirements</span></span>



| <span data-ttu-id="7b1be-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b1be-116">Requirement</span></span> | <span data-ttu-id="7b1be-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b1be-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1be-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b1be-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b1be-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b1be-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b1be-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b1be-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b1be-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b1be-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b1be-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b1be-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b1be-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b1be-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7b1be-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7b1be-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7b1be-125">**TVN \_ BEGINRDRAGW** (Unicode) et **TVN \_ BEGINRDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7b1be-125">**TVN\_BEGINRDRAGW** (Unicode) and **TVN\_BEGINRDRAGA** (ANSI)</span></span><br/>             |



 

 





