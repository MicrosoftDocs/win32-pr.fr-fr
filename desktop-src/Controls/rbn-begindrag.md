---
title: RBN_BEGINDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque l’utilisateur commence à faire glisser une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- Contrôles Windows de code de notification RBN_BEGINDRAG
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464390"
---
# <a name="rbn_begindrag-notification-code"></a><span data-ttu-id="1c989-105">\_Code de notification RBN BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="1c989-105">RBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="1c989-106">Envoyé par un contrôle rebar lorsque l’utilisateur commence à faire glisser une bande.</span><span class="sxs-lookup"><span data-stu-id="1c989-106">Sent by a rebar control when the user begins dragging a band.</span></span> <span data-ttu-id="1c989-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1c989-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1c989-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c989-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c989-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c989-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c989-110">Pointeur vers une structure [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="1c989-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c989-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c989-111">Return value</span></span>

<span data-ttu-id="1c989-112">Retourne zéro pour permettre au Rebar de continuer l’opération glisser, ou une valeur différente de zéro pour abandonner l’opération glisser.</span><span class="sxs-lookup"><span data-stu-id="1c989-112">Return zero to allow the rebar to continue the drag operation, or nonzero to abort the drag operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c989-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c989-113">Requirements</span></span>



| <span data-ttu-id="1c989-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c989-114">Requirement</span></span> | <span data-ttu-id="1c989-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c989-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c989-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c989-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c989-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c989-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c989-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c989-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c989-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c989-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c989-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c989-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c989-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c989-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





