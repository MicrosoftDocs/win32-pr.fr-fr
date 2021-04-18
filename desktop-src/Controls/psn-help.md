---
title: PSN_HELP le code de notification (Prsht. h)
description: Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton aide. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- Contrôles Windows de code de notification PSN_HELP
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512588"
---
# <a name="psn_help-notification-code"></a><span data-ttu-id="3c672-105">\_Code de notification d’aide PSN</span><span class="sxs-lookup"><span data-stu-id="3c672-105">PSN\_HELP notification code</span></span>

<span data-ttu-id="3c672-106">Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton aide.</span><span class="sxs-lookup"><span data-stu-id="3c672-106">Notifies a page that the user has clicked the Help button.</span></span> <span data-ttu-id="3c672-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3c672-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3c672-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c672-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c672-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c672-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c672-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="3c672-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="3c672-111">Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c672-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="3c672-112">Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.</span><span class="sxs-lookup"><span data-stu-id="3c672-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c672-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c672-113">Return value</span></span>

<span data-ttu-id="3c672-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="3c672-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c672-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3c672-115">Remarks</span></span>

<span data-ttu-id="3c672-116">Une application doit afficher des informations d’aide pour la page.</span><span class="sxs-lookup"><span data-stu-id="3c672-116">An application should display Help information for the page.</span></span>

> [!Note]  
> <span data-ttu-id="3c672-117">Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="3c672-117">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c672-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c672-118">Requirements</span></span>



| <span data-ttu-id="3c672-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c672-119">Requirement</span></span> | <span data-ttu-id="3c672-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c672-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c672-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c672-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3c672-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c672-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3c672-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c672-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3c672-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c672-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3c672-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c672-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c672-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c672-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





