---
title: DTN_USERSTRING le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsqu’un utilisateur termine la modification d’une chaîne dans le contrôle.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- Contrôles Windows de code de notification DTN_USERSTRING
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843209"
---
# <a name="dtn_userstring-notification-code"></a><span data-ttu-id="1494c-104">\_Code de notification DTN USERSTRING</span><span class="sxs-lookup"><span data-stu-id="1494c-104">DTN\_USERSTRING notification code</span></span>

<span data-ttu-id="1494c-105">Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsqu’un utilisateur termine la modification d’une chaîne dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="1494c-105">Sent by a date and time picker (DTP) control when a user finishes editing a string in the control.</span></span> <span data-ttu-id="1494c-106">Ce code de notification est uniquement envoyé par les contrôles de PAO définis sur le style [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1494c-106">This notification code is only sent by DTP controls that are set to the [**DTS\_APPCANPARSE**](date-and-time-picker-control-styles.md) style.</span></span> <span data-ttu-id="1494c-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1494c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1494c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1494c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1494c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1494c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1494c-110">Pointeur vers une structure [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) qui contient des informations sur l’instance du code de notification.</span><span class="sxs-lookup"><span data-stu-id="1494c-110">A pointer to an [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) structure that contains information about the instance of the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1494c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1494c-111">Return value</span></span>

<span data-ttu-id="1494c-112">Le propriétaire du contrôle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="1494c-112">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1494c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1494c-113">Remarks</span></span>

<span data-ttu-id="1494c-114">La gestion de ce code de notification permet au propriétaire de fournir des réponses personnalisées aux chaînes entrées dans le contrôle par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1494c-114">Handling this notification code allows the owner to provide custom responses to strings entered into the control by the user.</span></span> <span data-ttu-id="1494c-115">Le propriétaire doit être prêt à analyser la chaîne d’entrée et à agir si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1494c-115">The owner must be prepared to parse the input string and take action if necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="1494c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1494c-116">Requirements</span></span>



| <span data-ttu-id="1494c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1494c-117">Requirement</span></span> | <span data-ttu-id="1494c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1494c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1494c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1494c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1494c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1494c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1494c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1494c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1494c-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1494c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1494c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1494c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1494c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1494c-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1494c-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1494c-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1494c-126">**DTN \_ USERSTRINGW** (Unicode) et **DTN \_ USERSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1494c-126">**DTN\_USERSTRINGW** (Unicode) and **DTN\_USERSTRINGA** (ANSI)</span></span><br/>             |



 

 





