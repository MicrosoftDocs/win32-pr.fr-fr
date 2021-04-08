---
title: Code de notification NM_CLICK (arborescence) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle Tree-View sur lequel l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- Contrôles Windows de code de notification NM_CLICK (arborescence)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45809a683d06871398e79419ec08729b1edcd2c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743988"
---
# <a name="nm_click-tree-view-notification-code"></a><span data-ttu-id="d1958-105">\_$ $ $, Cliquez (arborescence) Code de notification</span><span class="sxs-lookup"><span data-stu-id="d1958-105">NM\_CLICK (tree view) notification code</span></span>

<span data-ttu-id="d1958-106">Notifie la fenêtre parente d’un contrôle Tree-View sur lequel l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d1958-106">Notifies the parent window of a tree-view control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="d1958-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d1958-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d1958-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1958-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1958-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1958-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="d1958-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1958-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1958-111">Return value</span></span>

<span data-ttu-id="d1958-112">Retourne une valeur différente de zéro pour empêcher le traitement par défaut, ou zéro pour autoriser le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1958-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1958-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1958-113">Requirements</span></span>



| <span data-ttu-id="d1958-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1958-114">Requirement</span></span> | <span data-ttu-id="d1958-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1958-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1958-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1958-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1958-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1958-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1958-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1958-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1958-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1958-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1958-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1958-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1958-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1958-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





