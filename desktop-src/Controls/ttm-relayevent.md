---
title: Message TTM_RELAYEVENT (commctrl. h)
description: Transmet un message de souris à un contrôle ToolTip pour traitement.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322277"
---
# <a name="ttm_relayevent-message"></a><span data-ttu-id="911cd-104">\_Message atténuation RELAYEVENT</span><span class="sxs-lookup"><span data-stu-id="911cd-104">TTM\_RELAYEVENT message</span></span>

<span data-ttu-id="911cd-105">Transmet un message de souris à un contrôle ToolTip pour traitement.</span><span class="sxs-lookup"><span data-stu-id="911cd-105">Passes a mouse message to a tooltip control for processing.</span></span>

## <a name="parameters"></a><span data-ttu-id="911cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="911cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="911cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="911cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="911cd-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="911cd-108">Must be zero.</span></span> <span data-ttu-id="911cd-109">**Windows 7 et versions ultérieures :** Si la position de l’info-bulle est décalée par rapport à la position du curseur (dans le cas contraire, un doigt ou un dispositif de pointage n’est pas obstrué), ce paramètre peut contenir des informations supplémentaires extraites du message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="911cd-109">**Windows 7 and later:** If the position of the tooltip is offset from the cursor position (in order not be obstructed by a finger or pointing device), this parameter can contain extra information taken from the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="911cd-110">Récupérez ces informations supplémentaires avec [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span><span class="sxs-lookup"><span data-stu-id="911cd-110">Retrieve this extra information with [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span></span>

</dd> <dt>

<span data-ttu-id="911cd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="911cd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="911cd-112">Pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) qui contient le message à relayer.</span><span class="sxs-lookup"><span data-stu-id="911cd-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to relay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="911cd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="911cd-113">Return value</span></span>

<span data-ttu-id="911cd-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="911cd-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="911cd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="911cd-115">Remarks</span></span>

<span data-ttu-id="911cd-116">Un contrôle ToolTip traite uniquement les messages suivants qui lui sont passés par le message **atténuation \_ RELAYEVENT** :</span><span class="sxs-lookup"><span data-stu-id="911cd-116">A tooltip control processes only the following messages passed to it by the **TTM\_RELAYEVENT** message:</span></span>

-   <span data-ttu-id="911cd-117">\_LBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="911cd-117">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="911cd-118">\_LBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="911cd-118">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="911cd-119">\_MBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="911cd-119">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="911cd-120">\_MBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="911cd-120">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="911cd-121">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="911cd-121">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="911cd-122">\_NCMOUSEMOVE WM</span><span class="sxs-lookup"><span data-stu-id="911cd-122">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="911cd-123">\_RBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="911cd-123">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="911cd-124">\_RBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="911cd-124">WM\_RBUTTONUP</span></span>

<span data-ttu-id="911cd-125">Tous les autres messages sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="911cd-125">All other messages are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="911cd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="911cd-126">Requirements</span></span>



| <span data-ttu-id="911cd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="911cd-127">Requirement</span></span> | <span data-ttu-id="911cd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="911cd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="911cd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="911cd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="911cd-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="911cd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="911cd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="911cd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="911cd-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="911cd-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="911cd-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="911cd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="911cd-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="911cd-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

