---
title: RBN_CHILDSIZE le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque la fenêtre enfant d’une bande est redimensionnée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- Contrôles Windows de code de notification RBN_CHILDSIZE
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843789"
---
# <a name="rbn_childsize-notification-code"></a><span data-ttu-id="c646d-105">\_Code de notification RBN CHILDSIZE</span><span class="sxs-lookup"><span data-stu-id="c646d-105">RBN\_CHILDSIZE notification code</span></span>

<span data-ttu-id="c646d-106">Envoyé par un contrôle rebar lorsque la fenêtre enfant d’une bande est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="c646d-106">Sent by a rebar control when a band's child window is resized.</span></span> <span data-ttu-id="c646d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c646d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c646d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c646d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c646d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c646d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c646d-110">Pointeur vers une structure [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="c646d-110">Pointer to an [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c646d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c646d-111">Return value</span></span>

<span data-ttu-id="c646d-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c646d-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c646d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c646d-113">Requirements</span></span>



| <span data-ttu-id="c646d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c646d-114">Requirement</span></span> | <span data-ttu-id="c646d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c646d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c646d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c646d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c646d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c646d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c646d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c646d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c646d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c646d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c646d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c646d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c646d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c646d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





