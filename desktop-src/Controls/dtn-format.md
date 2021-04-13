---
title: DTN_FORMAT le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) pour demander du texte à afficher dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- Contrôles Windows de code de notification DTN_FORMAT
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465919"
---
# <a name="dtn_format-notification-code"></a><span data-ttu-id="fcf8d-105">\_Code de notification au format DTN</span><span class="sxs-lookup"><span data-stu-id="fcf8d-105">DTN\_FORMAT notification code</span></span>

<span data-ttu-id="fcf8d-106">Envoyé par un contrôle de sélecteur de date et heure (PAO) pour demander du texte à afficher dans un champ de rappel.</span><span class="sxs-lookup"><span data-stu-id="fcf8d-106">Sent by a date and time picker (DTP) control to request text to be displayed in a callback field.</span></span> <span data-ttu-id="fcf8d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fcf8d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fcf8d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcf8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf8d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcf8d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcf8d-110">Pointeur vers une structure [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) contenant des informations relatives à cette instance du code de notification.</span><span class="sxs-lookup"><span data-stu-id="fcf8d-110">A pointer to an [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) structure containing information regarding this instance of the notification code.</span></span> <span data-ttu-id="fcf8d-111">La structure contient la sous-chaîne qui définit le champ de rappel et reçoit la chaîne mise en forme qui sera affichée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="fcf8d-111">The structure contains the substring that defines the callback field and receives the formatted string that the control will display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf8d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcf8d-112">Return value</span></span>

<span data-ttu-id="fcf8d-113">Le propriétaire du contrôle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="fcf8d-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcf8d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fcf8d-114">Remarks</span></span>

<span data-ttu-id="fcf8d-115">La gestion de ce code de notification permet au propriétaire du contrôle de fournir une chaîne personnalisée que le contrôle affichera.</span><span class="sxs-lookup"><span data-stu-id="fcf8d-115">Handling this notification code allows the owner of the control to provide a custom string that the control will display.</span></span> <span data-ttu-id="fcf8d-116">(Pour plus d’informations sur les champs de rappel, consultez [champs de rappel](date-and-time-picker-controls.md).)</span><span class="sxs-lookup"><span data-stu-id="fcf8d-116">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf8d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcf8d-117">Requirements</span></span>



| <span data-ttu-id="fcf8d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcf8d-118">Requirement</span></span> | <span data-ttu-id="fcf8d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcf8d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf8d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcf8d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf8d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcf8d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcf8d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcf8d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf8d-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcf8d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcf8d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcf8d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf8d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf8d-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fcf8d-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fcf8d-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fcf8d-127">**DTN \_ FORMATW** (Unicode) et **DTN \_ Formata** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fcf8d-127">**DTN\_FORMATW** (Unicode) and **DTN\_FORMATA** (ANSI)</span></span><br/>                     |



 

 





