---
title: Code de notification NM_DBLCLK (barre d’outils) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle ToolBar que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- Contrôles Windows de code de notification NM_DBLCLK (barre d’outils)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5441f86fa47f25a98dad82f9bfde05a84b5f498
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464266"
---
# <a name="nm_dblclk-toolbar-notification-code"></a><span data-ttu-id="bf941-105">\_Code de notification DBLCLK nm (barre d’outils)</span><span class="sxs-lookup"><span data-stu-id="bf941-105">NM\_DBLCLK (toolbar) notification code</span></span>

<span data-ttu-id="bf941-106">Avertit la fenêtre parente d’un contrôle ToolBar que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="bf941-106">Notifies the parent window of a toolbar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="bf941-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bf941-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bf941-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf941-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf941-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf941-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf941-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="bf941-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="bf941-111">Si l’utilisateur a cliqué sur un élément de la barre d’outils, le membre **dwItemSpec** contient l’identificateur de l’élément et le membre **dwItemData** contient les données de l’élément.</span><span class="sxs-lookup"><span data-stu-id="bf941-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="bf941-112">Si vous avez cliqué sur un séparateur ou un espace blanc dans la barre d’outils, le membre **dwItemSpec** contient-1.</span><span class="sxs-lookup"><span data-stu-id="bf941-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf941-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf941-113">Return value</span></span>

<span data-ttu-id="bf941-114">Retourne **false** pour permettre au contrôle de barre d’outils d’effectuer le traitement par défaut de l’événement, ou **true** pour empêcher le contrôle de traiter l’événement.</span><span class="sxs-lookup"><span data-stu-id="bf941-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf941-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf941-115">Requirements</span></span>



| <span data-ttu-id="bf941-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf941-116">Requirement</span></span> | <span data-ttu-id="bf941-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf941-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf941-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf941-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf941-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf941-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf941-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf941-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf941-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf941-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf941-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf941-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf941-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf941-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





