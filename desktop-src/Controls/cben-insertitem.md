---
title: CBEN_INSERTITEM le code de notification (commctrl. h)
description: Envoyé lorsqu’un nouvel élément a été inséré dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- Contrôles Windows de code de notification CBEN_INSERTITEM
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743820"
---
# <a name="cben_insertitem-notification-code"></a><span data-ttu-id="0add7-105">\_Code de notification CBEN INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="0add7-105">CBEN\_INSERTITEM notification code</span></span>

<span data-ttu-id="0add7-106">Envoyé lorsqu’un nouvel élément a été inséré dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0add7-106">Sent when a new item has been inserted in the control.</span></span> <span data-ttu-id="0add7-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0add7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0add7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0add7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0add7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0add7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0add7-110">Pointeur vers une structure [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenant des informations sur le code de notification et l’élément inséré.</span><span class="sxs-lookup"><span data-stu-id="0add7-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure containing information about the notification code and the item that was inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0add7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0add7-111">Return value</span></span>

<span data-ttu-id="0add7-112">L’application traitant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="0add7-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0add7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0add7-113">Requirements</span></span>



| <span data-ttu-id="0add7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0add7-114">Requirement</span></span> | <span data-ttu-id="0add7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0add7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0add7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0add7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0add7-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0add7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0add7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0add7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0add7-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0add7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0add7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0add7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0add7-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0add7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





