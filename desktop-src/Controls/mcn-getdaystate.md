---
title: MCN_GETDAYSTATE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar pour demander des informations sur le mode d’affichage des jours individuels. Ce code de notification n’est envoyé que par les contrôles de calendrier mensuel qui utilisent le \_ style MCS DAYSTATE et il est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- Contrôles Windows de code de notification MCN_GETDAYSTATE
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741692"
---
# <a name="mcn_getdaystate-notification-code"></a><span data-ttu-id="95683-105">\_Code de notification MCN GETDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="95683-105">MCN\_GETDAYSTATE notification code</span></span>

<span data-ttu-id="95683-106">Envoyé par un contrôle Month Calendar pour demander des informations sur le mode d’affichage des jours individuels.</span><span class="sxs-lookup"><span data-stu-id="95683-106">Sent by a month calendar control to request information about how individual days should be displayed.</span></span> <span data-ttu-id="95683-107">Ce code de notification n’est envoyé que par les contrôles de calendrier mensuel qui utilisent le style [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) et il est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="95683-107">This notification code is sent only by month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style, and it is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="95683-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95683-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95683-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95683-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95683-110">Pointeur vers une structure [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) .</span><span class="sxs-lookup"><span data-stu-id="95683-110">Pointer to an [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure.</span></span> <span data-ttu-id="95683-111">La structure contient des informations sur le laps de temps pour lequel le contrôle a besoin d’informations et reçoit l’adresse d’un tableau qui fournit ces données.</span><span class="sxs-lookup"><span data-stu-id="95683-111">The structure contains information about the time frame for which the control needs information, and it receives the address of an array that provides this data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95683-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95683-112">Return value</span></span>

<span data-ttu-id="95683-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="95683-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95683-114">Notes</span><span class="sxs-lookup"><span data-stu-id="95683-114">Remarks</span></span>

<span data-ttu-id="95683-115">La gestion de ce code de notification permet à votre application de personnaliser son affichage en spécifiant que certains jours s’affichent en gras.</span><span class="sxs-lookup"><span data-stu-id="95683-115">Handling this notification code allows your application to customize its display by specifying that certain days be displayed in bold.</span></span>

## <a name="requirements"></a><span data-ttu-id="95683-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95683-116">Requirements</span></span>



| <span data-ttu-id="95683-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95683-117">Requirement</span></span> | <span data-ttu-id="95683-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="95683-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95683-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95683-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95683-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95683-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95683-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95683-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95683-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95683-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95683-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="95683-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95683-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95683-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





