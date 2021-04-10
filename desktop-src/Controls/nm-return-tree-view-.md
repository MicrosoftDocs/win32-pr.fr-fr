---
title: Code de notification NM_RETURN (arborescence) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- Contrôles Windows de code de notification NM_RETURN (arborescence)
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942551"
---
# <a name="nm_return-tree-view-notification-code"></a><span data-ttu-id="c28fe-105">\_Code de notification de retour (arborescence) nm</span><span class="sxs-lookup"><span data-stu-id="c28fe-105">NM\_RETURN (tree view) notification code</span></span>

<span data-ttu-id="c28fe-106">Avertit une fenêtre parente d’un contrôle Tree-View que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche.</span><span class="sxs-lookup"><span data-stu-id="c28fe-106">Notifies a tree-view control's parent window that the control has the input focus and that the user has pressed the key.</span></span> <span data-ttu-id="c28fe-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c28fe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c28fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c28fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c28fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c28fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c28fe-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="c28fe-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c28fe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c28fe-111">Return value</span></span>

<span data-ttu-id="c28fe-112">Retourne une valeur différente de zéro pour empêcher le traitement par défaut, ou zéro pour autoriser le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="c28fe-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c28fe-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c28fe-113">Requirements</span></span>



| <span data-ttu-id="c28fe-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c28fe-114">Requirement</span></span> | <span data-ttu-id="c28fe-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c28fe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c28fe-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c28fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c28fe-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c28fe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c28fe-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c28fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c28fe-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c28fe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c28fe-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c28fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c28fe-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c28fe-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





