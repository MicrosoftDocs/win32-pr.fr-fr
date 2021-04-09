---
title: NM_TVSTATEIMAGECHANGING le code de notification (commctrl. h)
description: Envoyé par un contrôle Tree-View à sa fenêtre parente que l’image d’état change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- Contrôles Windows de code de notification NM_TVSTATEIMAGECHANGING
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103344"
---
# <a name="nm_tvstateimagechanging-notification-code"></a><span data-ttu-id="7fc91-105">\_Code de notification TVSTATEIMAGECHANGING nm</span><span class="sxs-lookup"><span data-stu-id="7fc91-105">NM\_TVSTATEIMAGECHANGING notification code</span></span>

<span data-ttu-id="7fc91-106">Envoyé par un contrôle Tree-View à sa fenêtre parente que l’image d’état change.</span><span class="sxs-lookup"><span data-stu-id="7fc91-106">Sent by a tree-view control to its parent window that the state image is changing.</span></span> <span data-ttu-id="7fc91-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc91-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7fc91-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fc91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc91-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fc91-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc91-110">Pointeur vers une structure [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="7fc91-110">A pointer to an [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc91-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fc91-111">Return value</span></span>

<span data-ttu-id="7fc91-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="7fc91-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc91-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fc91-113">Requirements</span></span>



| <span data-ttu-id="7fc91-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fc91-114">Requirement</span></span> | <span data-ttu-id="7fc91-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fc91-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc91-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fc91-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc91-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fc91-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fc91-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fc91-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc91-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fc91-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fc91-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fc91-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fc91-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc91-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





