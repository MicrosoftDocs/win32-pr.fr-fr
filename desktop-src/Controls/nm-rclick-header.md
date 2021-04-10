---
title: Code de notification NM_RCLICK (en-tête) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b453db51-9c41-4a85-8bc0-72bec10f8646
keywords:
- Contrôles Windows de code de notification NM_RCLICK (en-tête)
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
ms.openlocfilehash: bab91d3e35f4da74657faa2fce0e9a9881577087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942557"
---
# <a name="nm_rclick-header-notification-code"></a><span data-ttu-id="caa2d-105">\_Code de notification RCLICK nm (en-tête)</span><span class="sxs-lookup"><span data-stu-id="caa2d-105">NM\_RCLICK (header) notification code</span></span>

<span data-ttu-id="caa2d-106">Avertit une fenêtre parente d’un contrôle Tree-View que l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="caa2d-106">Notifies a tree-view control's parent window that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="caa2d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="caa2d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="caa2d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caa2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caa2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="caa2d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caa2d-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="caa2d-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caa2d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="caa2d-111">Return value</span></span>

<span data-ttu-id="caa2d-112">Retourne une valeur différente de zéro pour ne pas autoriser le traitement par défaut, ou zéro pour autoriser le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="caa2d-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="caa2d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caa2d-113">Requirements</span></span>



| <span data-ttu-id="caa2d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caa2d-114">Requirement</span></span> | <span data-ttu-id="caa2d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="caa2d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="caa2d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caa2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="caa2d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caa2d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="caa2d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caa2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="caa2d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caa2d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="caa2d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="caa2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa2d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="caa2d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





