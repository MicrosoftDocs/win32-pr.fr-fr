---
title: RBN_GETOBJECT le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar créé avec le \_ style RBS REGISTERDROP lorsqu’un objet est glissé sur une bande dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- Contrôles Windows de code de notification RBN_GETOBJECT
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104776"
---
# <a name="rbn_getobject-notification-code"></a><span data-ttu-id="13553-105">\_Code de notification RBN GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="13553-105">RBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="13553-106">Envoyé par un contrôle rebar créé avec le style [**RBS \_ REGISTERDROP**](rebar-control-styles.md) lorsqu’un objet est glissé sur une bande dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="13553-106">Sent by a rebar control created with the [**RBS\_REGISTERDROP**](rebar-control-styles.md) style when an object is dragged over a band in the control.</span></span> <span data-ttu-id="13553-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="13553-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="13553-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13553-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13553-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13553-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13553-110">Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui contient des informations sur la bande sur laquelle l’objet est glissé et reçoit également les données fournies par l’application réceptrice en réponse à ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="13553-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the band that the object is dragged over and also receives the data provided by the receiving application in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13553-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13553-111">Return value</span></span>

<span data-ttu-id="13553-112">La valeur de retour pour ce code de notification doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="13553-112">The return value for this notification code must be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13553-113">Notes</span><span class="sxs-lookup"><span data-stu-id="13553-113">Remarks</span></span>

<span data-ttu-id="13553-114">Pour recevoir le \_ Code de notification RBN GETOBJECT, initialisez OLE avec un appel à [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ou à [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="13553-114">To receive the RBN\_GETOBJECT notification code, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span>

## <a name="requirements"></a><span data-ttu-id="13553-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13553-115">Requirements</span></span>



| <span data-ttu-id="13553-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13553-116">Requirement</span></span> | <span data-ttu-id="13553-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="13553-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13553-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13553-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13553-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13553-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13553-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13553-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13553-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13553-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13553-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="13553-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="13553-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13553-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

