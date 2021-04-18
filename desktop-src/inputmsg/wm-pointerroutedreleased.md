---
title: Message WM_POINTERROUTEDRELEASED
description: Envoyé à tous les processus (configurés pour le chaînage inter-processus via AddContentWithCrossProcessChaining et ne gérant pas actuellement l’entrée de pointeur) jamais associés à un ID de pointeur spécifique, lors de la réception d’un message de WM_POINTERUP sur le processus actuel.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384684"
---
# <a name="wm_pointerroutedreleased-message"></a><span data-ttu-id="7f64f-104">Message WM_POINTERROUTEDRELEASED</span><span class="sxs-lookup"><span data-stu-id="7f64f-104">WM_POINTERROUTEDRELEASED message</span></span>

<span data-ttu-id="7f64f-105">Envoyé à tous les processus (configurés pour le chaînage inter-processus via [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) et ne gérant pas actuellement l’entrée de pointeur) jamais associés à un ID de pointeur spécifique, lors de la réception d’un message de [**WM_POINTERUP**](wm-pointerup.md) sur le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="7f64f-105">Sent to all processes (configured for cross-process chaining through [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [**WM_POINTERUP**](wm-pointerup.md) message is received on the current process.</span></span>


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a><span data-ttu-id="7f64f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f64f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f64f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f64f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f64f-108">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7f64f-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="7f64f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f64f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f64f-110">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7f64f-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f64f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f64f-111">Return value</span></span>

<span data-ttu-id="7f64f-112">NULL</span><span class="sxs-lookup"><span data-stu-id="7f64f-112">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="7f64f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f64f-113">Requirements</span></span>



| <span data-ttu-id="7f64f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f64f-114">Requirement</span></span> | <span data-ttu-id="7f64f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f64f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f64f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f64f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f64f-117">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7f64f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f64f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f64f-119">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f64f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f64f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f64f-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f64f-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f64f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f64f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f64f-123">Messages</span><span class="sxs-lookup"><span data-stu-id="7f64f-123">Messages</span></span>](messages.md)
</dt> </dl>

 

