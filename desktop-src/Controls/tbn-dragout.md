---
title: TBN_DRAGOUT le code de notification (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton, puis déplace le curseur en dehors du bouton. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- Contrôles Windows de code de notification TBN_DRAGOUT
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032607"
---
# <a name="tbn_dragout-notification-code"></a><span data-ttu-id="c7c38-105">\_Code de notification TBN DRAGOUT</span><span class="sxs-lookup"><span data-stu-id="c7c38-105">TBN\_DRAGOUT notification code</span></span>

<span data-ttu-id="c7c38-106">Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton, puis déplace le curseur en dehors du bouton.</span><span class="sxs-lookup"><span data-stu-id="c7c38-106">Sent by a toolbar control when the user clicks a button and then moves the cursor off the button.</span></span> <span data-ttu-id="c7c38-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c7c38-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c7c38-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7c38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c38-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7c38-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c38-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="c7c38-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="c7c38-111">Pour ce code de notification, seuls les membres **HDR** et **iItem** de cette structure sont valides.</span><span class="sxs-lookup"><span data-stu-id="c7c38-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="c7c38-112">Le membre **iItem** de cette structure contient l’identificateur de commande du bouton qui est glissé.</span><span class="sxs-lookup"><span data-stu-id="c7c38-112">The **iItem** member of this structure contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c38-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7c38-113">Return value</span></span>

<span data-ttu-id="c7c38-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c7c38-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c38-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c7c38-115">Remarks</span></span>

<span data-ttu-id="c7c38-116">Ce code de notification permet à une application d’implémenter la fonctionnalité glisser-déplacer pour les boutons de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="c7c38-116">This notification code allows an application to implement drag-and-drop functionality for toolbar buttons.</span></span> <span data-ttu-id="c7c38-117">Lors du traitement de ce code de notification, l’application commence l’opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="c7c38-117">When processing this notification code, the application will begin the drag-and-drop operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c38-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7c38-118">Requirements</span></span>



| <span data-ttu-id="c7c38-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7c38-119">Requirement</span></span> | <span data-ttu-id="c7c38-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7c38-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c38-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7c38-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c38-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7c38-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7c38-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7c38-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c38-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7c38-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7c38-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7c38-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c38-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c38-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





