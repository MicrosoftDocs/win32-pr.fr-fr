---
title: RBN_ENDDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque l’utilisateur arrête de faire glisser une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- Contrôles Windows de code de notification RBN_ENDDRAG
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033043"
---
# <a name="rbn_enddrag-notification-code"></a><span data-ttu-id="0c1a6-105">\_Code de notification RBN ENDDRAG</span><span class="sxs-lookup"><span data-stu-id="0c1a6-105">RBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="0c1a6-106">Envoyé par un contrôle rebar lorsque l’utilisateur arrête de faire glisser une bande.</span><span class="sxs-lookup"><span data-stu-id="0c1a6-106">Sent by a rebar control when the user stops dragging a band.</span></span> <span data-ttu-id="0c1a6-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0c1a6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0c1a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c1a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c1a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c1a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c1a6-110">Pointeur vers une structure [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="0c1a6-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c1a6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c1a6-111">Return value</span></span>

<span data-ttu-id="0c1a6-112">La valeur de retour pour ce code de notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0c1a6-112">The return value for this notification code is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1a6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c1a6-113">Requirements</span></span>



| <span data-ttu-id="0c1a6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c1a6-114">Requirement</span></span> | <span data-ttu-id="0c1a6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c1a6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1a6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c1a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c1a6-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c1a6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c1a6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c1a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c1a6-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c1a6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c1a6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c1a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c1a6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c1a6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





