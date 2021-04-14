---
title: Message WM_POINTERROUTEDTO
description: Envoyé lors de l’entrée de pointeur en cours, pour un ID de pointeur existant, passe d’un processus à un autre dans le contenu configuré pour le chaînage inter-processus (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384411"
---
# <a name="wm_pointerroutedto-message"></a><span data-ttu-id="8f4d6-104">Message WM_POINTERROUTEDTO</span><span class="sxs-lookup"><span data-stu-id="8f4d6-104">WM_POINTERROUTEDTO message</span></span>

<span data-ttu-id="8f4d6-105">Envoyé lors de l’entrée de pointeur en cours, pour un ID de pointeur existant, passe d’un processus à un autre dans le contenu configuré pour le chaînage inter-processus ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="8f4d6-105">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="8f4d6-106">Ce message est envoyé au processus qui ne reçoit pas actuellement l’entrée de pointeur.</span><span class="sxs-lookup"><span data-stu-id="8f4d6-106">This message is sent to the process not currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a><span data-ttu-id="8f4d6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f4d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f4d6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f4d6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4d6-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="8f4d6-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8f4d6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f4d6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4d6-111">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="8f4d6-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f4d6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f4d6-112">Return value</span></span>

<span data-ttu-id="8f4d6-113">NULL</span><span class="sxs-lookup"><span data-stu-id="8f4d6-113">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="8f4d6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8f4d6-114">Remarks</span></span>

<span data-ttu-id="8f4d6-115">Ce message n’est pas envoyé lorsqu’un message de [**WM_POINTERDOWN**](wm-pointerdown.md) est publié pour un nouvel ID de pointeur sur un processus différent.</span><span class="sxs-lookup"><span data-stu-id="8f4d6-115">This message is not sent when a [**WM_POINTERDOWN**](wm-pointerdown.md) message is posted for a new pointer ID on a different process.</span></span>

<span data-ttu-id="8f4d6-116">Un message de [**WM_POINTERDOWN**](wm-pointerdown.md) n’est pas envoyé si un message **WM_POINTERROUTEDTO** est publié en premier.</span><span class="sxs-lookup"><span data-stu-id="8f4d6-116">A [**WM_POINTERDOWN**](wm-pointerdown.md) message is not sent if a **WM_POINTERROUTEDTO** message is posted first.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f4d6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f4d6-117">Requirements</span></span>



| <span data-ttu-id="8f4d6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f4d6-118">Requirement</span></span> | <span data-ttu-id="8f4d6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f4d6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f4d6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f4d6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8f4d6-121">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f4d6-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8f4d6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f4d6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8f4d6-123">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f4d6-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f4d6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f4d6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f4d6-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f4d6-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f4d6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f4d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f4d6-127">Messages</span><span class="sxs-lookup"><span data-stu-id="8f4d6-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="8f4d6-128">**WM_POINTERROUTEDAWAY**</span><span class="sxs-lookup"><span data-stu-id="8f4d6-128">**WM_POINTERROUTEDAWAY**</span></span>](wm-pointerroutedaway.md)
</dt> </dl>

 

