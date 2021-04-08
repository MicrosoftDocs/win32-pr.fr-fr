---
title: NM_THEMECHANGED le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le thème a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- Contrôles Windows de code de notification NM_THEMECHANGED
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033052"
---
# <a name="nm_themechanged-notification-code"></a><span data-ttu-id="02ca0-105">\_Code de notification THEMECHANGED nm</span><span class="sxs-lookup"><span data-stu-id="02ca0-105">NM\_THEMECHANGED notification code</span></span>

<span data-ttu-id="02ca0-106">Avertit la fenêtre parente d’un contrôle que le thème a changé.</span><span class="sxs-lookup"><span data-stu-id="02ca0-106">Notifies a control's parent window that the theme has changed.</span></span> <span data-ttu-id="02ca0-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="02ca0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="02ca0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02ca0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ca0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02ca0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02ca0-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="02ca0-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ca0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02ca0-111">Return value</span></span>

<span data-ttu-id="02ca0-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="02ca0-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ca0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02ca0-113">Requirements</span></span>



| <span data-ttu-id="02ca0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02ca0-114">Requirement</span></span> | <span data-ttu-id="02ca0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="02ca0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02ca0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02ca0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02ca0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02ca0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02ca0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02ca0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02ca0-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02ca0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02ca0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="02ca0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02ca0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="02ca0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





