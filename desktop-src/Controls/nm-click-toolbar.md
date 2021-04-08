---
title: Code de notification NM_CLICK (barre d’outils) (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Contrôles Windows de code de notification NM_CLICK (barre d’outils)
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
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844462"
---
# <a name="nm_click-toolbar-notification-code"></a><span data-ttu-id="e0147-105">\_Code de notification de clic (barre d’outils) sur nm</span><span class="sxs-lookup"><span data-stu-id="e0147-105">NM\_CLICK (toolbar) notification code</span></span>

<span data-ttu-id="e0147-106">Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="e0147-106">Sent by a toolbar control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="e0147-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e0147-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e0147-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0147-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0147-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0147-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0147-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="e0147-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="e0147-111">Le membre **dwItemSpec** contient l’index de la section sur laquelle l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="e0147-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0147-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0147-112">Return value</span></span>

<span data-ttu-id="e0147-113">Retourne la **valeur true** pour indiquer que le clic de souris a été géré et supprimer le traitement par défaut par le système.</span><span class="sxs-lookup"><span data-stu-id="e0147-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="e0147-114">Retourne **false** pour autoriser le traitement par défaut du clic.</span><span class="sxs-lookup"><span data-stu-id="e0147-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0147-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e0147-115">Remarks</span></span>

<span data-ttu-id="e0147-116">Si vous cliquez sur un élément avec le bouton gauche de la souris, la barre d’outils envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec le code de notification sur lequel l' [ \_ utilisateur a cliqué](bn-clicked.md) dans la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="e0147-116">Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window.</span></span> <span data-ttu-id="e0147-117">La \_ notification de clic sur nm est envoyée après le message de **\_ commande WM** .</span><span class="sxs-lookup"><span data-stu-id="e0147-117">The NM\_CLICK notification is sent after the **WM\_COMMAND** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0147-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0147-118">Requirements</span></span>



| <span data-ttu-id="e0147-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0147-119">Requirement</span></span> | <span data-ttu-id="e0147-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0147-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0147-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0147-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e0147-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0147-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0147-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0147-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e0147-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0147-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0147-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0147-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0147-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0147-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

