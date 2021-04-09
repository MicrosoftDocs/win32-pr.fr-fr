---
title: Message WM_POINTERROUTEDAWAY
description: Se produit sur le processus qui reçoit l’entrée lorsque l’entrée du pointeur est routée vers un autre processus. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- WM_POINTERROUTEDAWAY les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033027"
---
# <a name="wm_pointerroutedaway-message"></a><span data-ttu-id="1d43a-104">Message WM_POINTERROUTEDAWAY</span><span class="sxs-lookup"><span data-stu-id="1d43a-104">WM_POINTERROUTEDAWAY message</span></span>

<span data-ttu-id="1d43a-105">Se produit sur le processus qui reçoit l’entrée lorsque l’entrée du pointeur est routée vers un autre processus.</span><span class="sxs-lookup"><span data-stu-id="1d43a-105">Occurs on the process receiving input when the pointer input is routed to another process.</span></span>

<span data-ttu-id="1d43a-106">Envoyé lorsque l’entrée de pointeur passe d’un processus à un autre dans le contenu configuré pour le chaînage inter-processus ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="1d43a-106">Sent when pointer input transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="1d43a-107">Ce message est envoyé au processus qui reçoit actuellement l’entrée de pointeur.</span><span class="sxs-lookup"><span data-stu-id="1d43a-107">This message is sent to the process currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a><span data-ttu-id="1d43a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d43a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d43a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d43a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d43a-110">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="1d43a-110">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="1d43a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d43a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d43a-112">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="1d43a-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d43a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d43a-113">Return value</span></span>

<span data-ttu-id="1d43a-114">NULL</span><span class="sxs-lookup"><span data-stu-id="1d43a-114">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="1d43a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1d43a-115">Remarks</span></span>

<span data-ttu-id="1d43a-116">Ce message n’est pas envoyé avec un message [**WM_POINTERUP**](wm-pointerup.md) ou un message [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="1d43a-116">This message is not sent with either a [**WM_POINTERUP**](wm-pointerup.md) message or a [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d43a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d43a-117">Requirements</span></span>



| <span data-ttu-id="1d43a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d43a-118">Requirement</span></span> | <span data-ttu-id="1d43a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d43a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d43a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d43a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d43a-121">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d43a-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1d43a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d43a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d43a-123">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d43a-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d43a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d43a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d43a-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d43a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d43a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d43a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d43a-127">Messages</span><span class="sxs-lookup"><span data-stu-id="1d43a-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="1d43a-128">**WM_POINTERROUTEDTO**</span><span class="sxs-lookup"><span data-stu-id="1d43a-128">**WM_POINTERROUTEDTO**</span></span>](wm-pointerroutedto.md)
</dt> </dl>

 

