---
title: HDN_DROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur la flèche déroulante du contrôle d’en-tête. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- Contrôles Windows de code de notification HDN_DROPDOWN
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844489"
---
# <a name="hdn_dropdown-notification-code"></a><span data-ttu-id="7204d-105">\_Code de notification de liste déroulante HDN</span><span class="sxs-lookup"><span data-stu-id="7204d-105">HDN\_DROPDOWN notification code</span></span>

<span data-ttu-id="7204d-106">Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur la flèche déroulante du contrôle d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7204d-106">Sent by a header control to its parent when the drop-down arrow on the header control is clicked.</span></span> <span data-ttu-id="7204d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7204d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7204d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7204d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7204d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7204d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7204d-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header.</span><span class="sxs-lookup"><span data-stu-id="7204d-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information on the header control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7204d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7204d-111">Return value</span></span>

<span data-ttu-id="7204d-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="7204d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7204d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7204d-113">Remarks</span></span>

<span data-ttu-id="7204d-114">L’exemple de la section syntaxe montre comment le récepteur de notification convertit **lParam** pour récupérer la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="7204d-114">The example in the Syntax section shows how the notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="7204d-115">**WParam** contient l’ID du contrôle qui envoie ce message.</span><span class="sxs-lookup"><span data-stu-id="7204d-115">**WPARAM** contains the ID of the control that sends this message.</span></span>

<span data-ttu-id="7204d-116">Ce message est envoyé uniquement si le style HDF \_ SPLITBUTTON est défini sur l’élément d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7204d-116">This message is sent only if style HDF\_SPLITBUTTON is set on the header item.</span></span>

## <a name="requirements"></a><span data-ttu-id="7204d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7204d-117">Requirements</span></span>



| <span data-ttu-id="7204d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7204d-118">Requirement</span></span> | <span data-ttu-id="7204d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7204d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7204d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7204d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7204d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7204d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7204d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7204d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7204d-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7204d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7204d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7204d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7204d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7204d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





