---
title: TBN_DRAGOVER le code de notification (commctrl. h)
description: Vérifie si un \_ message MARKBUTTON to doit être envoyé pour un bouton qui est glissé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- Contrôles Windows de code de notification TBN_DRAGOVER
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464766"
---
# <a name="tbn_dragover-notification-code"></a><span data-ttu-id="76b6d-105">\_Code de notification TBN DRAGOVER</span><span class="sxs-lookup"><span data-stu-id="76b6d-105">TBN\_DRAGOVER notification code</span></span>

<span data-ttu-id="76b6d-106">Vérifie si un message [**\_ MARKBUTTON to**](tb-markbutton.md) doit être envoyé pour un bouton qui est glissé.</span><span class="sxs-lookup"><span data-stu-id="76b6d-106">Ascertains whether a [**TB\_MARKBUTTON**](tb-markbutton.md) message should be sent for a button that is being dragged over.</span></span> <span data-ttu-id="76b6d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="76b6d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="76b6d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76b6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76b6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76b6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76b6d-110">Pointeur vers une structure [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) qui spécifie l’élément sur lequel l’élément est glissé.</span><span class="sxs-lookup"><span data-stu-id="76b6d-110">A pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that specifies which item is being dragged over.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76b6d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76b6d-111">Return value</span></span>

<span data-ttu-id="76b6d-112">**False** si la barre d’outils doit envoyer un \_ message MARKBUTTON to ; sinon, **true**.</span><span class="sxs-lookup"><span data-stu-id="76b6d-112">**FALSE** if the toolbar should send a TB\_MARKBUTTON message; otherwise **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="76b6d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76b6d-113">Requirements</span></span>



| <span data-ttu-id="76b6d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76b6d-114">Requirement</span></span> | <span data-ttu-id="76b6d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="76b6d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76b6d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76b6d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="76b6d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76b6d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76b6d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76b6d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="76b6d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76b6d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76b6d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="76b6d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="76b6d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76b6d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





