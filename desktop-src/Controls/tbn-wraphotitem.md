---
title: TBN_WRAPHOTITEM le code de notification (commctrl. h)
description: Avertit une application avec au moins deux barres d’outils que l’élément réactif est sur le point de changer. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- Contrôles Windows de code de notification TBN_WRAPHOTITEM
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465030"
---
# <a name="tbn_wraphotitem-notification-code"></a><span data-ttu-id="c9710-105">\_Code de notification TBN WRAPHOTITEM</span><span class="sxs-lookup"><span data-stu-id="c9710-105">TBN\_WRAPHOTITEM notification code</span></span>

<span data-ttu-id="c9710-106">Avertit une application avec au moins deux barres d’outils que l’élément réactif est sur le point de changer.</span><span class="sxs-lookup"><span data-stu-id="c9710-106">Notifies an application with two or more toolbars that the hot item is about to change.</span></span> <span data-ttu-id="c9710-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c9710-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c9710-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9710-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9710-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9710-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9710-110">Pointeur vers une structure qui contient l’ancien élément réactif (**iStart**) et si le nouvel élément réactif est avant (**iDir** =-1) ou après (**iDir** = 1), ainsi que la raison pour laquelle l’élément réactif change.</span><span class="sxs-lookup"><span data-stu-id="c9710-110">A pointer to a structure that contains the old hot item (**iStart**) and whether the new hot item is before it (**iDir** = -1) or after it (**iDir** = 1), as well as a reason why the hot item is changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9710-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9710-111">Return value</span></span>

<span data-ttu-id="c9710-112">**True** si l’application gère la modification de l’élément réactif lui-même ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="c9710-112">**TRUE** if the application is handling the hot item change itself; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9710-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c9710-113">Remarks</span></span>

<span data-ttu-id="c9710-114">La structure **NMTBWRAPHOTITEM** doit être définie par l’application comme suit :</span><span class="sxs-lookup"><span data-stu-id="c9710-114">The **NMTBWRAPHOTITEM** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a><span data-ttu-id="c9710-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9710-115">Requirements</span></span>



| <span data-ttu-id="c9710-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9710-116">Requirement</span></span> | <span data-ttu-id="c9710-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9710-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9710-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9710-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9710-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9710-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9710-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9710-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9710-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9710-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9710-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9710-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9710-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9710-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





