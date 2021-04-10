---
title: Code de notification NM_RCLICK (arborescence) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle Tree-View sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5816d8b8-7f3d-477d-9116-1b3670d99240
keywords:
- Contrôles Windows de code de notification NM_RCLICK (arborescence)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d72ee220bf33189e8954a2e1ef454b22886553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106618"
---
# <a name="nm_rclick-tree-view-notification-code"></a><span data-ttu-id="ceada-105">\_Code de notification RCLICK nm (arborescence)</span><span class="sxs-lookup"><span data-stu-id="ceada-105">NM\_RCLICK (tree view) notification code</span></span>

<span data-ttu-id="ceada-106">Notifie la fenêtre parente d’un contrôle Tree-View sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ceada-106">Notifies the parent window of a tree-view control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="ceada-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ceada-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ceada-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ceada-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceada-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ceada-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ceada-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="ceada-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceada-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ceada-111">Return value</span></span>

<span data-ttu-id="ceada-112">Retourne une valeur différente de zéro pour empêcher le traitement par défaut, ou zéro pour autoriser le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="ceada-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceada-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ceada-113">Requirements</span></span>



| <span data-ttu-id="ceada-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ceada-114">Requirement</span></span> | <span data-ttu-id="ceada-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ceada-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ceada-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ceada-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ceada-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ceada-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ceada-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ceada-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ceada-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ceada-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ceada-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ceada-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceada-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceada-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





