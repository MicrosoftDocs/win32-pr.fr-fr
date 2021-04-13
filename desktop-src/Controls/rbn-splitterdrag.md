---
title: RBN_SPLITTERDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque l’utilisateur fait glisser un séparateur. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- Contrôles Windows de code de notification RBN_SPLITTERDRAG
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508902"
---
# <a name="rbn_splitterdrag-notification-code"></a><span data-ttu-id="2007d-105">\_Code de notification RBN SPLITTERDRAG</span><span class="sxs-lookup"><span data-stu-id="2007d-105">RBN\_SPLITTERDRAG notification code</span></span>

<span data-ttu-id="2007d-106">Envoyé par un contrôle rebar lorsque l’utilisateur fait glisser un séparateur.</span><span class="sxs-lookup"><span data-stu-id="2007d-106">Sent by a rebar control when the user drags a splitter.</span></span> <span data-ttu-id="2007d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2007d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2007d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2007d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2007d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2007d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2007d-110">Pointeur vers une structure [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="2007d-110">Pointer to an [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2007d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2007d-111">Return value</span></span>

<span data-ttu-id="2007d-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2007d-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2007d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2007d-113">Requirements</span></span>



| <span data-ttu-id="2007d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2007d-114">Requirement</span></span> | <span data-ttu-id="2007d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2007d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2007d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2007d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2007d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2007d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2007d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2007d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2007d-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2007d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2007d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2007d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2007d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2007d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





