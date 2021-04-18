---
title: NM_RDBLCLK (barre d’État) Code de notification (commctrl. h)
description: Avertit les fenêtres parentes d’un contrôle de barre d’État que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- NM_RDBLCLK (barre d’État) contrôles Windows de code de notification
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18092b03a599c75a88deb56bb256d96728b96328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467110"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a><span data-ttu-id="f9562-105">\_RDBLCLK nm (barre d’État) Code de notification</span><span class="sxs-lookup"><span data-stu-id="f9562-105">NM\_RDBLCLK (status bar) notification code</span></span>

<span data-ttu-id="f9562-106">Avertit les fenêtres parentes d’un contrôle de barre d’État que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f9562-106">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="f9562-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f9562-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f9562-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9562-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9562-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9562-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9562-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="f9562-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="f9562-111">Le membre **dwItemSpec** contient l’index de la section sur laquelle l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="f9562-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9562-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9562-112">Return value</span></span>

<span data-ttu-id="f9562-113">Retourne la **valeur true** pour indiquer que le clic de souris a été géré et supprimer le traitement par défaut par le système.</span><span class="sxs-lookup"><span data-stu-id="f9562-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="f9562-114">Retourne **false** pour autoriser le traitement par défaut du clic.</span><span class="sxs-lookup"><span data-stu-id="f9562-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9562-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9562-115">Requirements</span></span>



| <span data-ttu-id="f9562-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9562-116">Requirement</span></span> | <span data-ttu-id="f9562-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9562-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9562-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9562-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9562-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9562-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9562-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9562-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9562-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9562-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9562-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9562-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9562-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9562-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





