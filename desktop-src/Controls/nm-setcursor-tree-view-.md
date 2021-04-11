---
title: Code de notification NM_SETCURSOR (arborescence) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que le contrôle définit le curseur en réponse à un \_ message WM SETCURSOR. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- Contrôles Windows de code de notification NM_SETCURSOR (arborescence)
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40b733e32c72abc9620e0fd18a6ef554aee9214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942550"
---
# <a name="nm_setcursor-tree-view-notification-code"></a><span data-ttu-id="de625-105">\_Code de notification SETCURSOR nm (arborescence)</span><span class="sxs-lookup"><span data-stu-id="de625-105">NM\_SETCURSOR (tree view) notification code</span></span>

<span data-ttu-id="de625-106">Avertit une fenêtre parente d’un contrôle Tree-View que le contrôle définit le curseur en réponse à un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="de625-106">Notifies a tree-view control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="de625-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="de625-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="de625-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de625-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de625-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de625-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de625-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="de625-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de625-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de625-111">Return value</span></span>

<span data-ttu-id="de625-112">Retournez zéro pour permettre au contrôle de définir le curseur ou une valeur différente de zéro pour empêcher le contrôle de définir le curseur.</span><span class="sxs-lookup"><span data-stu-id="de625-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="de625-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de625-113">Requirements</span></span>



| <span data-ttu-id="de625-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de625-114">Requirement</span></span> | <span data-ttu-id="de625-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="de625-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de625-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de625-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de625-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de625-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de625-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de625-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de625-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de625-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de625-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="de625-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de625-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de625-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

