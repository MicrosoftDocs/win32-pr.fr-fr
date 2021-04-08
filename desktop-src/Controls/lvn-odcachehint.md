---
title: LVN_ODCACHEHINT le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View virtuel lorsque le contenu de sa zone d’affichage a changé.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- Contrôles Windows de code de notification LVN_ODCACHEHINT
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942918"
---
# <a name="lvn_odcachehint-notification-code"></a><span data-ttu-id="cd57c-104">\_Code de notification LVN ODCACHEHINT</span><span class="sxs-lookup"><span data-stu-id="cd57c-104">LVN\_ODCACHEHINT notification code</span></span>

<span data-ttu-id="cd57c-105">Envoyé par un contrôle List-View virtuel lorsque le contenu de sa zone d’affichage a changé.</span><span class="sxs-lookup"><span data-stu-id="cd57c-105">Sent by a virtual list-view control when the contents of its display area have changed.</span></span> <span data-ttu-id="cd57c-106">Par exemple, un contrôle List-View envoie ce code de notification lorsque l’utilisateur fait défiler l’affichage du contrôle.</span><span class="sxs-lookup"><span data-stu-id="cd57c-106">For example, a list-view control sends this notification code when the user scrolls the control's display.</span></span> <span data-ttu-id="cd57c-107">Le \_ Code de notification LVN ODCACHEHINT est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cd57c-107">The LVN\_ODCACHEHINT notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cd57c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd57c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd57c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd57c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd57c-110">Pointeur vers une structure [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) contenant des informations sur la plage d’éléments à mettre en cache.</span><span class="sxs-lookup"><span data-stu-id="cd57c-110">Pointer to an [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) structure containing information about the range of items to be cached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd57c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd57c-111">Return value</span></span>

<span data-ttu-id="cd57c-112">L’application recevant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="cd57c-112">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd57c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cd57c-113">Remarks</span></span>

<span data-ttu-id="cd57c-114">La gestion de ce message permet à l’application de mettre à jour les informations d’élément conservées dans le cache afin qu’elles soient facilement disponibles lorsqu’un code de notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) est envoyé.</span><span class="sxs-lookup"><span data-stu-id="cd57c-114">Handling this message allows the application to update the item information held in cache so that it is readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification code is sent.</span></span>

<span data-ttu-id="cd57c-115">Notez que ce code de notification n’est pas toujours une représentation exacte des éléments qui seront demandés par [LVN \_ GETDISPINFO](lvn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="cd57c-115">Note that this notification code is not always an exact representation of the items that will be requested by [LVN\_GETDISPINFO](lvn-getdispinfo.md).</span></span> <span data-ttu-id="cd57c-116">Par conséquent, si l’élément demandé n’est pas mis en cache pendant la gestion de LVN \_ GETDISPINFO, l’application doit être préparée à fournir les informations demandées à partir d’une source située à l’extérieur du cache.</span><span class="sxs-lookup"><span data-stu-id="cd57c-116">Therefore, if the requested item is not cached while handling LVN\_GETDISPINFO, the application must be prepared to supply the requested information from a source outside the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd57c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd57c-117">Requirements</span></span>



| <span data-ttu-id="cd57c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd57c-118">Requirement</span></span> | <span data-ttu-id="cd57c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd57c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd57c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd57c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd57c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd57c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd57c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd57c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd57c-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd57c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd57c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd57c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd57c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd57c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





