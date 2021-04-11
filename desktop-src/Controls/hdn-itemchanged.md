---
title: HDN_ITEMCHANGED le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête ont changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- Contrôles Windows de code de notification HDN_ITEMCHANGED
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032432"
---
# <a name="hdn_itemchanged-notification-code"></a><span data-ttu-id="7a941-105">\_Code de notification HDN ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="7a941-105">HDN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="7a941-106">Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête ont changé.</span><span class="sxs-lookup"><span data-stu-id="7a941-106">Notifies a header control's parent window that the attributes of a header item have changed.</span></span> <span data-ttu-id="7a941-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7a941-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7a941-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a941-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a941-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a941-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a941-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header, y compris les attributs qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="7a941-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control, including the attributes that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a941-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a941-111">Return value</span></span>

<span data-ttu-id="7a941-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="7a941-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a941-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a941-113">Requirements</span></span>



| <span data-ttu-id="7a941-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a941-114">Requirement</span></span> | <span data-ttu-id="7a941-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a941-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a941-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a941-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7a941-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a941-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a941-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a941-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7a941-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a941-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a941-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a941-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a941-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a941-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7a941-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7a941-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7a941-123">**HDN \_ ITEMCHANGEDW** (Unicode) et **HDN \_ ITEMCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7a941-123">**HDN\_ITEMCHANGEDW** (Unicode) and **HDN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



 

 





