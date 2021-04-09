---
title: Message WM_DWMNCRENDERINGCHANGED (winuser. h)
description: Envoyé lorsque la stratégie de rendu de la zone non cliente a changé.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- Message de WM_DWMNCRENDERINGCHANGED Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942210"
---
# <a name="wm_dwmncrenderingchanged-message"></a><span data-ttu-id="42609-104">\_Message WM DWMNCRENDERINGCHANGED</span><span class="sxs-lookup"><span data-stu-id="42609-104">WM\_DWMNCRENDERINGCHANGED message</span></span>

<span data-ttu-id="42609-105">Envoyé lorsque la stratégie de rendu de la zone non cliente a changé.</span><span class="sxs-lookup"><span data-stu-id="42609-105">Sent when the non-client area rendering policy has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="42609-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42609-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42609-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42609-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42609-108">Spécifie si le rendu DWM est activé pour la zone non cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="42609-108">Specifies whether DWM rendering is enabled for the non-client area of the window.</span></span> <span data-ttu-id="42609-109">**True** si l’option est activée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="42609-109">**TRUE** if enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="42609-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42609-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42609-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="42609-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42609-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42609-112">Return value</span></span>

<span data-ttu-id="42609-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="42609-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="42609-114">Notes</span><span class="sxs-lookup"><span data-stu-id="42609-114">Remarks</span></span>

<span data-ttu-id="42609-115">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="42609-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="42609-116">Les fonctions [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) et [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) sont utilisées pour récupérer ou définir la stratégie de rendu non client.</span><span class="sxs-lookup"><span data-stu-id="42609-116">The [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions are used to get or set the non-client rendering policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="42609-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42609-117">Requirements</span></span>



| <span data-ttu-id="42609-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42609-118">Requirement</span></span> | <span data-ttu-id="42609-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="42609-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42609-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42609-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42609-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42609-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="42609-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42609-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42609-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42609-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42609-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="42609-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="42609-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="42609-125"><dt>Winuser.h</dt></span></span> </dl> |



 

