---
title: Message PGM_FORWARDMOUSE (commctrl. h)
description: Active ou désactive le transfert de la souris pour le contrôle de pagineur. Lorsque le transfert de souris est activé, le contrôle de pagineur transfère les \_ messages de la souris WM à la fenêtre contenue. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ ForwardMouse.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542861"
---
# <a name="pgm_forwardmouse-message"></a><span data-ttu-id="f3dc4-106">\_Message FORWARDMOUSE PGM</span><span class="sxs-lookup"><span data-stu-id="f3dc4-106">PGM\_FORWARDMOUSE message</span></span>

<span data-ttu-id="f3dc4-107">Active ou désactive le transfert de la souris pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-107">Enables or disables mouse forwarding for the pager control.</span></span> <span data-ttu-id="f3dc4-108">Lorsque le transfert de souris est activé, le contrôle de pagineur transfère les messages de la souris [**WM \_**](/windows/desktop/inputdev/wm-mousemove) à la fenêtre contenue.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-108">When mouse forwarding is enabled, the pager control forwards [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to the contained window.</span></span> <span data-ttu-id="f3dc4-109">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .</span><span class="sxs-lookup"><span data-stu-id="f3dc4-109">You can send this message explicitly or use the [**Pager\_ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3dc4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3dc4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3dc4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3dc4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3dc4-112">Valeur **booléenne** qui détermine si le transfert de souris est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-112">**BOOL** value that determines if mouse forwarding is enabled or disabled.</span></span> <span data-ttu-id="f3dc4-113">Si cette valeur est différente de zéro, le transfert de souris est activé.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-113">If this value is nonzero, mouse forwarding is enabled.</span></span> <span data-ttu-id="f3dc4-114">Si cette valeur est égale à zéro, le transfert de la souris est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-114">If this value is zero, mouse forwarding is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f3dc4-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3dc4-115">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f3dc4-116">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-116">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3dc4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3dc4-117">Return value</span></span>

<span data-ttu-id="f3dc4-118">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-118">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3dc4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3dc4-119">Requirements</span></span>



| <span data-ttu-id="f3dc4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3dc4-120">Requirement</span></span> | <span data-ttu-id="f3dc4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3dc4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3dc4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3dc4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3dc4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3dc4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3dc4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3dc4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3dc4-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3dc4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3dc4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3dc4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3dc4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3dc4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

