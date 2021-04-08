---
title: LVN_ODSTATECHANGED le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’état d’un élément ou d’une plage d’éléments a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- Contrôles Windows de code de notification LVN_ODSTATECHANGED
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742549"
---
# <a name="lvn_odstatechanged-notification-code"></a><span data-ttu-id="2f855-105">\_Code de notification LVN ODSTATECHANGED</span><span class="sxs-lookup"><span data-stu-id="2f855-105">LVN\_ODSTATECHANGED notification code</span></span>

<span data-ttu-id="2f855-106">Envoyé par un contrôle List-View lorsque l’état d’un élément ou d’une plage d’éléments a changé.</span><span class="sxs-lookup"><span data-stu-id="2f855-106">Sent by a list-view control when the state of an item or range of items has changed.</span></span> <span data-ttu-id="2f855-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2f855-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2f855-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f855-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f855-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f855-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f855-110">Pointeur vers une structure [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) qui contient des informations sur l’élément ou les éléments qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="2f855-110">Pointer to an [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) structure that contains information about the item or items that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f855-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f855-111">Return value</span></span>

<span data-ttu-id="2f855-112">L’application recevant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="2f855-112">The application receiving this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f855-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f855-113">Requirements</span></span>



| <span data-ttu-id="2f855-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f855-114">Requirement</span></span> | <span data-ttu-id="2f855-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f855-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f855-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f855-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f855-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f855-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f855-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f855-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f855-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f855-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f855-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f855-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f855-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f855-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





