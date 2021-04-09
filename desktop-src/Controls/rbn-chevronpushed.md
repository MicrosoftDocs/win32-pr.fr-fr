---
title: RBN_CHEVRONPUSHED le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsqu’un chevron fait l’objet d’un push. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- Contrôles Windows de code de notification RBN_CHEVRONPUSHED
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032840"
---
# <a name="rbn_chevronpushed-notification-code"></a><span data-ttu-id="b4e2e-105">\_Code de notification RBN CHEVRONPUSHED</span><span class="sxs-lookup"><span data-stu-id="b4e2e-105">RBN\_CHEVRONPUSHED notification code</span></span>

<span data-ttu-id="b4e2e-106">Envoyé par un contrôle rebar lorsqu’un chevron fait l’objet d’un push.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-106">Sent by a rebar control when a chevron is pushed.</span></span> <span data-ttu-id="b4e2e-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e2e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b4e2e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4e2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4e2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4e2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4e2e-110">Pointeur vers la structure [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) de la bande.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-110">Pointer to the band's [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4e2e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4e2e-111">Return value</span></span>

<span data-ttu-id="b4e2e-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4e2e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b4e2e-113">Remarks</span></span>

<span data-ttu-id="b4e2e-114">Lorsqu’une application reçoit ce code de notification, il est chargé d’afficher un menu contextuel contenant des éléments pour chaque outil masqué.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-114">When an application receives this notification code, it is responsible for displaying a popup menu with items for each hidden tool.</span></span> <span data-ttu-id="b4e2e-115">Utilisez le membre **RC** de la structure [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) pour rechercher la position correcte du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-115">Use the **rc** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure to find the correct position for the popup menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e2e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4e2e-116">Requirements</span></span>



| <span data-ttu-id="b4e2e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4e2e-117">Requirement</span></span> | <span data-ttu-id="b4e2e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4e2e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e2e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4e2e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e2e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4e2e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4e2e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4e2e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e2e-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4e2e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4e2e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4e2e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4e2e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4e2e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





