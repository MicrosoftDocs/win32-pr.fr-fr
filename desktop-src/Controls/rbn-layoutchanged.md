---
title: RBN_LAYOUTCHANGED le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque l’utilisateur modifie la disposition des bandes du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- Contrôles Windows de code de notification RBN_LAYOUTCHANGED
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104770"
---
# <a name="rbn_layoutchanged-notification-code"></a><span data-ttu-id="ec0d5-105">\_Code de notification RBN LAYOUTCHANGED</span><span class="sxs-lookup"><span data-stu-id="ec0d5-105">RBN\_LAYOUTCHANGED notification code</span></span>

<span data-ttu-id="ec0d5-106">Envoyé par un contrôle rebar lorsque l’utilisateur modifie la disposition des bandes du contrôle.</span><span class="sxs-lookup"><span data-stu-id="ec0d5-106">Sent by a rebar control when the user changes the layout of the control's bands.</span></span> <span data-ttu-id="ec0d5-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ec0d5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ec0d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec0d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec0d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec0d5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec0d5-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="ec0d5-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec0d5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec0d5-111">Return value</span></span>

<span data-ttu-id="ec0d5-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ec0d5-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec0d5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec0d5-113">Requirements</span></span>



| <span data-ttu-id="ec0d5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec0d5-114">Requirement</span></span> | <span data-ttu-id="ec0d5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec0d5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0d5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec0d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0d5-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec0d5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec0d5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec0d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0d5-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec0d5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec0d5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec0d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec0d5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec0d5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





