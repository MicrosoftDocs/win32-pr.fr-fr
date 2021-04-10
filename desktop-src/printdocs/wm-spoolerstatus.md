---
description: Le \_ message WM SPOOLERSTATUS est envoyé à partir du gestionnaire d’impression chaque fois qu’un travail est ajouté ou supprimé de la file d’attente du gestionnaire d’impression.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Message WM_SPOOLERSTATUS (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115686"
---
# <a name="wm_spoolerstatus-message"></a><span data-ttu-id="7be07-103">\_Message WM SPOOLERSTATUS</span><span class="sxs-lookup"><span data-stu-id="7be07-103">WM\_SPOOLERSTATUS message</span></span>

<span data-ttu-id="7be07-104">Le message **WM \_ SPOOLERSTATUS** est envoyé à partir du gestionnaire d’impression chaque fois qu’un travail est ajouté ou supprimé de la file d’attente du gestionnaire d’impression.</span><span class="sxs-lookup"><span data-stu-id="7be07-104">The **WM\_SPOOLERSTATUS** message is sent from Print Manager whenever a job is added to or removed from the Print Manager queue.</span></span>

<span data-ttu-id="7be07-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7be07-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="7be07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7be07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7be07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7be07-108">Indicateur PR \_ JOBSTATUS.</span><span class="sxs-lookup"><span data-stu-id="7be07-108">The PR\_JOBSTATUS flag.</span></span>

</dd> <dt>

<span data-ttu-id="7be07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7be07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7be07-110">Le mot de poids faible spécifie le nombre de travaux restant dans la file d’attente du gestionnaire d’impression.</span><span class="sxs-lookup"><span data-stu-id="7be07-110">The low-order word specifies the number of jobs remaining in the Print Manager queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be07-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7be07-111">Return value</span></span>

<span data-ttu-id="7be07-112">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="7be07-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7be07-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7be07-113">Remarks</span></span>

<span data-ttu-id="7be07-114">Ce message est fourni à titre d’information uniquement.</span><span class="sxs-lookup"><span data-stu-id="7be07-114">This message is for informational purposes only.</span></span> <span data-ttu-id="7be07-115">Ce message est un avis et n’a pas de sémantique de remise garantie.</span><span class="sxs-lookup"><span data-stu-id="7be07-115">This message is advisory and does not have guaranteed delivery semantics.</span></span> <span data-ttu-id="7be07-116">Les applications ne doivent pas supposer qu’elles recevront un \_ message WM SPOOLERSTATUS pour chaque modification de l’état du spouleur.</span><span class="sxs-lookup"><span data-stu-id="7be07-116">Applications should not assume that they will receive a WM\_SPOOLERSTATUS message for every change in spooler status.</span></span>

<span data-ttu-id="7be07-117">Le \_ message WM SPOOLERSTATUS n’est pas pris en charge après Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7be07-117">The WM\_SPOOLERSTATUS message is not supported after Windows XP.</span></span> <span data-ttu-id="7be07-118">Pour être averti des modifications apportées à l’état de la file d’attente à l’impression, vous pouvez utiliser [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) et [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="7be07-118">To be notified of changes to the print queue status, you can use [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) and [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7be07-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7be07-119">Requirements</span></span>



| <span data-ttu-id="7be07-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7be07-120">Requirement</span></span> | <span data-ttu-id="7be07-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7be07-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be07-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7be07-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7be07-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7be07-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7be07-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7be07-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7be07-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7be07-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7be07-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7be07-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be07-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7be07-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be07-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7be07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be07-129">Impression</span><span class="sxs-lookup"><span data-stu-id="7be07-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7be07-130">Messages d’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="7be07-130">Print Spooler API Messages</span></span>](printing-and-print-spooler-messages.md)
</dt> <dt>

[<span data-ttu-id="7be07-131">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="7be07-131">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="7be07-132">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="7be07-132">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

