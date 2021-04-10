---
title: Code de notification NM_CLICK (Syslink) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que l’utilisateur a cliqué sur un lien hypertexte avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- Contrôles Windows de code de notification NM_CLICK (Syslink)
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
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106642"
---
# <a name="nm_click-syslink-notification-code"></a><span data-ttu-id="cc023-105">\_Code de notification de clic (Syslink) nm</span><span class="sxs-lookup"><span data-stu-id="cc023-105">NM\_CLICK (syslink) notification code</span></span>

<span data-ttu-id="cc023-106">Avertit la fenêtre parente d’un contrôle que l’utilisateur a cliqué sur un lien hypertexte avec le bouton gauche de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc023-106">Notifies a control's parent window that the user has clicked a hyperlink with the left mouse button within the control.</span></span> <span data-ttu-id="cc023-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cc023-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cc023-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc023-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc023-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc023-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc023-110">Pointeur vers une structure [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="cc023-110">Pointer to an [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc023-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc023-111">Return value</span></span>

<span data-ttu-id="cc023-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc023-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc023-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cc023-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc023-114">Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="cc023-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cc023-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cc023-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc023-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc023-116">Requirements</span></span>



| <span data-ttu-id="cc023-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc023-117">Requirement</span></span> | <span data-ttu-id="cc023-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc023-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc023-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc023-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc023-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc023-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc023-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc023-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc023-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc023-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc023-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc023-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc023-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc023-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc023-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc023-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc023-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cc023-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cc023-127">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="cc023-127">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[<span data-ttu-id="cc023-128">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="cc023-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





