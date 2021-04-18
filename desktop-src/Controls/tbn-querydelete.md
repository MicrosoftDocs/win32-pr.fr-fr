---
title: TBN_QUERYDELETE le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être supprimé d’une barre d’outils pendant que l’utilisateur personnalise la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- Contrôles Windows de code de notification TBN_QUERYDELETE
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508297"
---
# <a name="tbn_querydelete-notification-code"></a><span data-ttu-id="72b27-105">\_Code de notification TBN QUERYDELETE</span><span class="sxs-lookup"><span data-stu-id="72b27-105">TBN\_QUERYDELETE notification code</span></span>

<span data-ttu-id="72b27-106">Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être supprimé d’une barre d’outils pendant que l’utilisateur personnalise la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="72b27-106">Notifies the toolbar's parent window whether a button may be deleted from a toolbar while the user is customizing the toolbar.</span></span> <span data-ttu-id="72b27-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="72b27-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="72b27-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72b27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72b27-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72b27-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72b27-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="72b27-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="72b27-111">Le membre **iItem** contient l’index de base zéro du bouton à supprimer.</span><span class="sxs-lookup"><span data-stu-id="72b27-111">The **iItem** member contains the zero-based index of the button to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72b27-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72b27-112">Return value</span></span>

<span data-ttu-id="72b27-113">Retourne la **valeur true** pour autoriser la suppression du bouton ou **false** pour empêcher la suppression du bouton.</span><span class="sxs-lookup"><span data-stu-id="72b27-113">Returns **TRUE** to allow the button to be deleted, or **FALSE** to prevent the button from being deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b27-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72b27-114">Requirements</span></span>



| <span data-ttu-id="72b27-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72b27-115">Requirement</span></span> | <span data-ttu-id="72b27-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="72b27-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72b27-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72b27-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72b27-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72b27-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72b27-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72b27-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72b27-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72b27-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72b27-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="72b27-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b27-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b27-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





