---
title: Message ICM_SET_STATUS_PROC (VFW. h)
description: Le \_ \_ \_ message de procédure de traitement d’État ICM fournit une fonction de rappel d’État avec l’état d’une opération de longue durée.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- Message ICM_SET_STATUS_PROC Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467090"
---
# <a name="icm_set_status_proc-message"></a><span data-ttu-id="7fea2-104">\_Message de \_ procédure d’état de l’ensemble ICM \_</span><span class="sxs-lookup"><span data-stu-id="7fea2-104">ICM\_SET\_STATUS\_PROC message</span></span>

<span data-ttu-id="7fea2-105">Le message de **\_ procédure de \_ \_ traitement d’État ICM** fournit une fonction de rappel d’État avec l’état d’une opération de longue durée.</span><span class="sxs-lookup"><span data-stu-id="7fea2-105">The **ICM\_SET\_STATUS\_PROC** message provides a status callback function with the status of a lengthy operation.</span></span>


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a><span data-ttu-id="7fea2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fea2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fea2-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span><span class="sxs-lookup"><span data-stu-id="7fea2-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span></span>
</dt> <dd>

<span data-ttu-id="7fea2-108">Pointeur vers une structure [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .</span><span class="sxs-lookup"><span data-stu-id="7fea2-108">Pointer to an [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7fea2-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fea2-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7fea2-110">Taille, en octets, de **ICSETSTATUSPROC**.</span><span class="sxs-lookup"><span data-stu-id="7fea2-110">Size, in bytes, of **ICSETSTATUSPROC**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fea2-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7fea2-111">Return Value</span></span>

<span data-ttu-id="7fea2-112">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7fea2-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fea2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7fea2-113">Remarks</span></span>

<span data-ttu-id="7fea2-114">La prise en charge de ce message est facultative, mais fortement recommandée si la compression ou la décompression prend plus d’un dixième de seconde environ.</span><span class="sxs-lookup"><span data-stu-id="7fea2-114">Support of this message is optional but strongly recommended if compression or decompression takes longer than approximately one-tenth of a second.</span></span>

<span data-ttu-id="7fea2-115">Une application peut envoyer ce message périodiquement à une fonction de rappel d’État pendant des opérations de longue durée.</span><span class="sxs-lookup"><span data-stu-id="7fea2-115">An application can send this message periodically to a status callback function during lengthy operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fea2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fea2-116">Requirements</span></span>



| <span data-ttu-id="7fea2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fea2-117">Requirement</span></span> | <span data-ttu-id="7fea2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fea2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fea2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fea2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7fea2-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fea2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7fea2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fea2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7fea2-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fea2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7fea2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fea2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fea2-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fea2-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fea2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fea2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fea2-126">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="7fea2-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7fea2-127">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="7fea2-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





