---
title: TBN_BEGINADJUST le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à personnaliser une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 689aeda3-5051-4422-9e66-64557b263943
keywords:
- Contrôles Windows de code de notification TBN_BEGINADJUST
topic_type:
- apiref
api_name:
- TBN_BEGINADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4708cd205461e3117432cec25e0e4256a6b0d87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843294"
---
# <a name="tbn_beginadjust-notification-code"></a><span data-ttu-id="5cc90-105">\_Code de notification TBN BEGINADJUST</span><span class="sxs-lookup"><span data-stu-id="5cc90-105">TBN\_BEGINADJUST notification code</span></span>

<span data-ttu-id="5cc90-106">Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à personnaliser une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="5cc90-106">Notifies a toolbar's parent window that the user has begun customizing a toolbar.</span></span> <span data-ttu-id="5cc90-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc90-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5cc90-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cc90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cc90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cc90-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cc90-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="5cc90-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cc90-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5cc90-111">Return value</span></span>

<span data-ttu-id="5cc90-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5cc90-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc90-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cc90-113">Requirements</span></span>



| <span data-ttu-id="5cc90-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cc90-114">Requirement</span></span> | <span data-ttu-id="5cc90-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cc90-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc90-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cc90-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc90-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cc90-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cc90-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cc90-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc90-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cc90-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cc90-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cc90-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cc90-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc90-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





