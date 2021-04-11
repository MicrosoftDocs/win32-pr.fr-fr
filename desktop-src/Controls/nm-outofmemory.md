---
title: NM_OUTOFMEMORY le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle n’a pas pu terminer une opération, car la mémoire disponible est insuffisante. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- Contrôles Windows de code de notification NM_OUTOFMEMORY
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032420"
---
# <a name="nm_outofmemory-notification-code"></a><span data-ttu-id="298f3-105">\_Code de notification OUTOFMEMORY nm</span><span class="sxs-lookup"><span data-stu-id="298f3-105">NM\_OUTOFMEMORY notification code</span></span>

<span data-ttu-id="298f3-106">Avertit la fenêtre parente d’un contrôle que le contrôle n’a pas pu terminer une opération, car la mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="298f3-106">Notifies a control's parent window that the control could not complete an operation because there was not enough memory available.</span></span> <span data-ttu-id="298f3-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="298f3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="298f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="298f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="298f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="298f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="298f3-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="298f3-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="298f3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="298f3-111">Return value</span></span>

<span data-ttu-id="298f3-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="298f3-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="298f3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="298f3-113">Requirements</span></span>



| <span data-ttu-id="298f3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="298f3-114">Requirement</span></span> | <span data-ttu-id="298f3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="298f3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="298f3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="298f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="298f3-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="298f3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="298f3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="298f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="298f3-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="298f3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="298f3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="298f3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="298f3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="298f3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





