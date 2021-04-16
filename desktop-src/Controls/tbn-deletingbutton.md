---
title: Message TBN_DELETINGBUTTON (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsqu’un bouton va être supprimé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- TBN_DELETINGBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508397"
---
# <a name="tbn_deletingbutton-message"></a><span data-ttu-id="c5a5e-105">\_Message TBN DELETINGBUTTON</span><span class="sxs-lookup"><span data-stu-id="c5a5e-105">TBN\_DELETINGBUTTON message</span></span>

<span data-ttu-id="c5a5e-106">Envoyé par un contrôle de barre d’outils lorsqu’un bouton va être supprimé.</span><span class="sxs-lookup"><span data-stu-id="c5a5e-106">Sent by a toolbar control when a button is about to be deleted.</span></span> <span data-ttu-id="c5a5e-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a5e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c5a5e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5a5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a5e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5a5e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a5e-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) qui contient des informations sur le bouton en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="c5a5e-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about the button being deleted.</span></span> <span data-ttu-id="c5a5e-111">Pour ce code de notification, seuls les membres **HDR** et **iItem** de cette structure sont valides.</span><span class="sxs-lookup"><span data-stu-id="c5a5e-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="c5a5e-112">Le membre **iItem** de cette structure contient l’identificateur de commande du bouton en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="c5a5e-112">The **iItem** member of this structure contains the command identifier of the button being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a5e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5a5e-113">Return value</span></span>

<span data-ttu-id="c5a5e-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c5a5e-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a5e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5a5e-115">Requirements</span></span>



| <span data-ttu-id="c5a5e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5a5e-116">Requirement</span></span> | <span data-ttu-id="c5a5e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5a5e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a5e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5a5e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a5e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5a5e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5a5e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5a5e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a5e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5a5e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5a5e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5a5e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5a5e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a5e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





