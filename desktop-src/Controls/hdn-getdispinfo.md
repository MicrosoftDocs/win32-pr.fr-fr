---
title: HDN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé au propriétaire d’un contrôle header lorsque le contrôle a besoin d’informations sur un élément d’en-tête de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- Contrôles Windows de code de notification HDN_GETDISPINFO
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032433"
---
# <a name="hdn_getdispinfo-notification-code"></a><span data-ttu-id="28a19-105">\_Code de notification HDN GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="28a19-105">HDN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="28a19-106">Envoyé au propriétaire d’un contrôle header lorsque le contrôle a besoin d’informations sur un élément d’en-tête de rappel.</span><span class="sxs-lookup"><span data-stu-id="28a19-106">Sent to the owner of a header control when the control needs information about a callback header item.</span></span> <span data-ttu-id="28a19-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="28a19-107">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="28a19-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28a19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28a19-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28a19-110">Pointeur vers une structure [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="28a19-110">A pointer to an [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure.</span></span> <span data-ttu-id="28a19-111">En entrée, les champs de la structure spécifient les informations requises et l’élément concerné.</span><span class="sxs-lookup"><span data-stu-id="28a19-111">On input, the fields of the structure specify what information is required and the item of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28a19-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28a19-112">Return value</span></span>

<span data-ttu-id="28a19-113">Retourne un LRESULT.</span><span class="sxs-lookup"><span data-stu-id="28a19-113">Returns an LRESULT.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a19-114">Notes</span><span class="sxs-lookup"><span data-stu-id="28a19-114">Remarks</span></span>

<span data-ttu-id="28a19-115">Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle header.</span><span class="sxs-lookup"><span data-stu-id="28a19-115">Fill the appropriate members of the structure to return the requested information to the header control.</span></span> <span data-ttu-id="28a19-116">Si votre gestionnaire de messages définit le membre **Mask** de la structure [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) sur HDI \_ di \_ SETITEM, le contrôle header stocke les informations et ne les redemande pas.</span><span class="sxs-lookup"><span data-stu-id="28a19-116">If your message handler sets the **mask** member of the [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure to HDI\_DI\_SETITEM, the header control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="28a19-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28a19-117">Requirements</span></span>



| <span data-ttu-id="28a19-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28a19-118">Requirement</span></span> | <span data-ttu-id="28a19-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="28a19-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28a19-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28a19-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28a19-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28a19-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28a19-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28a19-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28a19-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28a19-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28a19-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="28a19-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="28a19-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28a19-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="28a19-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="28a19-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="28a19-127">**HDN \_ GETDISPINFOW** (Unicode) et **HDN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="28a19-127">**HDN\_GETDISPINFOW** (Unicode) and **HDN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





