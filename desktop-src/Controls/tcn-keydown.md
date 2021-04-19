---
title: TCN_KEYDOWN le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet qu’une touche a été enfoncée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- Contrôles Windows de code de notification TCN_KEYDOWN
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510301"
---
# <a name="tcn_keydown-notification-code"></a><span data-ttu-id="9e887-105">Code de notification KeyOut TCN \_</span><span class="sxs-lookup"><span data-stu-id="9e887-105">TCN\_KEYDOWN notification code</span></span>

<span data-ttu-id="9e887-106">Avertit une fenêtre parente d’un contrôle onglet qu’une touche a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="9e887-106">Notifies a tab control's parent window that a key has been pressed.</span></span> <span data-ttu-id="9e887-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9e887-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9e887-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e887-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e887-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e887-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e887-110">Pointeur vers une structure [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) .</span><span class="sxs-lookup"><span data-stu-id="9e887-110">Pointer to an [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e887-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e887-111">Return value</span></span>

<span data-ttu-id="9e887-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9e887-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e887-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e887-113">Requirements</span></span>



| <span data-ttu-id="9e887-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e887-114">Requirement</span></span> | <span data-ttu-id="9e887-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e887-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e887-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e887-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e887-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e887-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e887-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e887-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e887-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e887-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e887-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e887-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e887-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e887-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





