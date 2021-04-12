---
title: Message TTM_NEWTOOLRECT (commctrl. h)
description: Définit un nouveau rectangle englobant pour un outil.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465350"
---
# <a name="ttm_newtoolrect-message"></a><span data-ttu-id="153fc-104">\_Message atténuation NEWTOOLRECT</span><span class="sxs-lookup"><span data-stu-id="153fc-104">TTM\_NEWTOOLRECT message</span></span>

<span data-ttu-id="153fc-105">Définit un nouveau rectangle englobant pour un outil.</span><span class="sxs-lookup"><span data-stu-id="153fc-105">Sets a new bounding rectangle for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="153fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="153fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153fc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="153fc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="153fc-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="153fc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="153fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="153fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="153fc-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="153fc-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="153fc-111">Les membres **HWND** et **UID** identifient un outil, tandis que le membre **Rect** spécifie le nouveau rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="153fc-111">The **hwnd** and **uId** members identify a tool, and the **rect** member specifies the new bounding rectangle.</span></span> <span data-ttu-id="153fc-112">Le membre **cbSize** de cette structure doit être rempli avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="153fc-112">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153fc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="153fc-113">Return value</span></span>

<span data-ttu-id="153fc-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="153fc-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="153fc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="153fc-115">Requirements</span></span>



| <span data-ttu-id="153fc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="153fc-116">Requirement</span></span> | <span data-ttu-id="153fc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="153fc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="153fc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="153fc-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="153fc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="153fc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="153fc-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="153fc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="153fc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="153fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="153fc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="153fc-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="153fc-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="153fc-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="153fc-125">**Atténuation \_ NEWTOOLRECTW** (Unicode) et **atténuation \_ NEWTOOLRECTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="153fc-125">**TTM\_NEWTOOLRECTW** (Unicode) and **TTM\_NEWTOOLRECTA** (ANSI)</span></span><br/>           |



 

 





