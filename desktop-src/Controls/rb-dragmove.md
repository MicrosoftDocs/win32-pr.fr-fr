---
title: Message RB_DRAGMOVE (commctrl. h)
description: Met à jour la position de glissement dans le contrôle rebar après un \_ message RB BEGINDRAG précédent.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942463"
---
# <a name="rb_dragmove-message"></a><span data-ttu-id="0929c-104">\_Message DRAGMOVE RB</span><span class="sxs-lookup"><span data-stu-id="0929c-104">RB\_DRAGMOVE message</span></span>

<span data-ttu-id="0929c-105">Met à jour la position de glissement dans le contrôle rebar après un message [**RB \_ BEGINDRAG**](rb-begindrag.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="0929c-105">Updates the drag position in the rebar control after a previous [**RB\_BEGINDRAG**](rb-begindrag.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="0929c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0929c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0929c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0929c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0929c-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0929c-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0929c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0929c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0929c-110">Valeur **DWORD** qui contient les nouvelles coordonnées de la souris.</span><span class="sxs-lookup"><span data-stu-id="0929c-110">**DWORD** value that contains the new mouse coordinates.</span></span> <span data-ttu-id="0929c-111">La coordonnée horizontale est contenue dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et la coordonnée verticale est contenue dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0929c-111">The horizontal coordinate is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical coordinate is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="0929c-112">Si vous transmettez (DWORD)-1, le contrôle rebar utilise la position de la souris la dernière fois que le thread du contrôle a appelé [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span><span class="sxs-lookup"><span data-stu-id="0929c-112">If you pass (DWORD)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0929c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0929c-113">Return value</span></span>

<span data-ttu-id="0929c-114">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0929c-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0929c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0929c-115">Requirements</span></span>



| <span data-ttu-id="0929c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0929c-116">Requirement</span></span> | <span data-ttu-id="0929c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0929c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0929c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0929c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0929c-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0929c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0929c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0929c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0929c-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0929c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0929c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0929c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0929c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0929c-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0929c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0929c-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="0929c-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0929c-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0929c-126">**\_ENDDRAG RB**</span><span class="sxs-lookup"><span data-stu-id="0929c-126">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
</dt> </dl>

 

