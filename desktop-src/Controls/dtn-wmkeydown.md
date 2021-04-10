---
title: DTN_WMKEYDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur tape dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- Contrôles Windows de code de notification DTN_WMKEYDOWN
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103061"
---
# <a name="dtn_wmkeydown-notification-code"></a><span data-ttu-id="8264d-105">\_Code de notification DTN WMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="8264d-105">DTN\_WMKEYDOWN notification code</span></span>

<span data-ttu-id="8264d-106">Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur tape dans un champ de rappel.</span><span class="sxs-lookup"><span data-stu-id="8264d-106">Sent by a date and time picker (DTP) control when the user types in a callback field.</span></span> <span data-ttu-id="8264d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8264d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a><span data-ttu-id="8264d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8264d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8264d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8264d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8264d-110">Pointeur vers une structure [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) contenant des informations sur cette instance du code de notification.</span><span class="sxs-lookup"><span data-stu-id="8264d-110">A pointer to an [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) structure containing information about this instance of the notification code.</span></span> <span data-ttu-id="8264d-111">La structure comprend des informations sur la clé tapée par l’utilisateur, la sous-chaîne qui définit le champ de rappel et la date et l’heure système actuelles.</span><span class="sxs-lookup"><span data-stu-id="8264d-111">The structure includes information about the key that the user typed, the substring that defines the callback field, and the current system date and time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8264d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8264d-112">Return value</span></span>

<span data-ttu-id="8264d-113">Le propriétaire du contrôle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="8264d-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8264d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8264d-114">Remarks</span></span>

<span data-ttu-id="8264d-115">La gestion de ce code de notification permet au propriétaire du contrôle de fournir des réponses spécifiques aux séquences de touches dans les champs de rappel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8264d-115">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8264d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8264d-116">Requirements</span></span>



| <span data-ttu-id="8264d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8264d-117">Requirement</span></span> | <span data-ttu-id="8264d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8264d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8264d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8264d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8264d-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8264d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8264d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8264d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8264d-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8264d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8264d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8264d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8264d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8264d-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8264d-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="8264d-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8264d-126">**DTN \_ WMKEYDOWNW** (Unicode) et **DTN \_ WMKEYDOWNA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8264d-126">**DTN\_WMKEYDOWNW** (Unicode) and **DTN\_WMKEYDOWNA** (ANSI)</span></span><br/>               |



 

 





