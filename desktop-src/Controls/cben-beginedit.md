---
title: CBEN_BEGINEDIT le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur active la liste déroulante ou clique dans la zone d’édition du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- Contrôles Windows de code de notification CBEN_BEGINEDIT
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d4cc80d12b01b9374173f413f0aee3701e5040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510168"
---
# <a name="cben_beginedit-notification-code"></a><span data-ttu-id="08cf6-105">\_Code de notification CBEN BEGINEDIT</span><span class="sxs-lookup"><span data-stu-id="08cf6-105">CBEN\_BEGINEDIT notification code</span></span>

<span data-ttu-id="08cf6-106">Envoyé lorsque l’utilisateur active la liste déroulante ou clique dans la zone d’édition du contrôle.</span><span class="sxs-lookup"><span data-stu-id="08cf6-106">Sent when the user activates the drop-down list or clicks in the control's edit box.</span></span> <span data-ttu-id="08cf6-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="08cf6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="08cf6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08cf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08cf6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08cf6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08cf6-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="08cf6-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08cf6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08cf6-111">Return value</span></span>

<span data-ttu-id="08cf6-112">L’application traitant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="08cf6-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="08cf6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08cf6-113">Requirements</span></span>



| <span data-ttu-id="08cf6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08cf6-114">Requirement</span></span> | <span data-ttu-id="08cf6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="08cf6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08cf6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08cf6-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08cf6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08cf6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08cf6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08cf6-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08cf6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08cf6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="08cf6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08cf6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08cf6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





