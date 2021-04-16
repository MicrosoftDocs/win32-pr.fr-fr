---
title: CBEN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé pour récupérer des informations d’affichage sur un élément de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- Contrôles Windows de code de notification CBEN_GETDISPINFO
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508313"
---
# <a name="cben_getdispinfo-notification-code"></a><span data-ttu-id="43f7b-105">\_Code de notification CBEN GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="43f7b-105">CBEN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="43f7b-106">Envoyé pour récupérer des informations d’affichage sur un élément de rappel.</span><span class="sxs-lookup"><span data-stu-id="43f7b-106">Sent to retrieve display information about a callback item.</span></span> <span data-ttu-id="43f7b-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="43f7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="43f7b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43f7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43f7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43f7b-110">Pointeur vers une structure [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="43f7b-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f7b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43f7b-111">Return value</span></span>

<span data-ttu-id="43f7b-112">L’application traitant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="43f7b-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="43f7b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="43f7b-113">Remarks</span></span>

<span data-ttu-id="43f7b-114">La structure [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contient une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="43f7b-114">The [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure contains a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="43f7b-115">Le membre de **masque** spécifie les informations demandées par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="43f7b-115">The **mask** member specifies the information being requested by the control.</span></span>

<span data-ttu-id="43f7b-116">Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle.</span><span class="sxs-lookup"><span data-stu-id="43f7b-116">Fill the appropriate members of the structure to return the requested information to the control.</span></span> <span data-ttu-id="43f7b-117">Si votre gestionnaire de messages définit le membre **Mask** de la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) sur CBEIF \_ di \_ SETITEM, le contrôle stocke les informations et ne les redemande pas.</span><span class="sxs-lookup"><span data-stu-id="43f7b-117">If your message handler sets the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f7b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43f7b-118">Requirements</span></span>



| <span data-ttu-id="43f7b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43f7b-119">Requirement</span></span> | <span data-ttu-id="43f7b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="43f7b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43f7b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43f7b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43f7b-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43f7b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43f7b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43f7b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43f7b-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43f7b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43f7b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="43f7b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f7b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f7b-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="43f7b-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="43f7b-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="43f7b-128">**CBEN \_ GETDISPINFOW** (Unicode) et **CBEN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="43f7b-128">**CBEN\_GETDISPINFOW** (Unicode) and **CBEN\_GETDISPINFOA** (ANSI)</span></span><br/>         |



 

 





