---
title: BCN_HOTITEMCHANGE le code de notification (commctrl. h)
description: Notifie le propriétaire du contrôle de bouton que la souris entre dans la zone cliente du contrôle bouton. Le contrôle Button envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- Contrôles Windows de code de notification BCN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032700"
---
# <a name="bcn_hotitemchange-notification-code"></a><span data-ttu-id="153b7-105">\_Code de notification BCN HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="153b7-105">BCN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="153b7-106">Notifie le propriétaire du contrôle de bouton que la souris entre dans la zone cliente du contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="153b7-106">Notifies the button control owner that the mouse is entering or leaving the client area of the button control.</span></span> <span data-ttu-id="153b7-107">Le contrôle Button envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="153b7-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="153b7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="153b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="153b7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="153b7-110">Pointeur vers une structure [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .</span><span class="sxs-lookup"><span data-stu-id="153b7-110">A pointer to a [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153b7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="153b7-111">Return value</span></span>

<span data-ttu-id="153b7-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="153b7-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="153b7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="153b7-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="153b7-114">Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="153b7-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="153b7-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="153b7-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="153b7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="153b7-116">Requirements</span></span>



| <span data-ttu-id="153b7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="153b7-117">Requirement</span></span> | <span data-ttu-id="153b7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="153b7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="153b7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153b7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="153b7-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="153b7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="153b7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153b7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="153b7-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="153b7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="153b7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="153b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="153b7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="153b7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





