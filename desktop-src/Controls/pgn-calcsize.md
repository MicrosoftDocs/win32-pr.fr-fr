---
title: PGN_CALCSIZE le code de notification (commctrl. h)
description: Envoyé par un contrôle pager pour obtenir les dimensions déroulantes de la fenêtre contenue.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- Contrôles Windows de code de notification PGN_CALCSIZE
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741220"
---
# <a name="pgn_calcsize-notification-code"></a><span data-ttu-id="c029f-104">\_Code de notification PGN CALCSIZE</span><span class="sxs-lookup"><span data-stu-id="c029f-104">PGN\_CALCSIZE notification code</span></span>

<span data-ttu-id="c029f-105">Envoyé par un contrôle pager pour obtenir les dimensions déroulantes de la fenêtre contenue.</span><span class="sxs-lookup"><span data-stu-id="c029f-105">Sent by a pager control to obtain the scrollable dimensions of the contained window.</span></span> <span data-ttu-id="c029f-106">Ces dimensions sont utilisées par le contrôle de pagineur pour déterminer la taille de défilement de la fenêtre contenue.</span><span class="sxs-lookup"><span data-stu-id="c029f-106">These dimensions are used by the pager control to determine the scrollable size of the contained window.</span></span> <span data-ttu-id="c029f-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c029f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c029f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c029f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c029f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c029f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c029f-110">Pointeur vers une structure [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) qui contient et reçoit des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="c029f-110">Pointer to an [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="c029f-111">Le membre **dwFlag** de cette structure indique quelle dimension est calculée.</span><span class="sxs-lookup"><span data-stu-id="c029f-111">The **dwFlag** member of this structure indicates which dimension is being calculated.</span></span> <span data-ttu-id="c029f-112">Selon la valeur de **dwFlag**, vous devez placer la dimension souhaitée dans le membre **iWidth** ou **iHeight** de cette structure.</span><span class="sxs-lookup"><span data-stu-id="c029f-112">Depending on the value of **dwFlag**, you should place the desired dimension in the **iWidth** or **iHeight** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c029f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c029f-113">Return value</span></span>

<span data-ttu-id="c029f-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c029f-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c029f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c029f-115">Requirements</span></span>



| <span data-ttu-id="c029f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c029f-116">Requirement</span></span> | <span data-ttu-id="c029f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c029f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c029f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c029f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c029f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c029f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c029f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c029f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c029f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c029f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c029f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c029f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c029f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c029f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





