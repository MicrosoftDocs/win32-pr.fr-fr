---
title: HDN_ITEMKEYDOWN le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header qu’une touche a été enfoncée avec un élément sélectionné. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- Contrôles Windows de code de notification HDN_ITEMKEYDOWN
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033245"
---
# <a name="hdn_itemkeydown-notification-code"></a><span data-ttu-id="17b7e-105">\_Code de notification HDN ITEMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="17b7e-105">HDN\_ITEMKEYDOWN notification code</span></span>

<span data-ttu-id="17b7e-106">Avertit la fenêtre parente d’un contrôle header qu’une touche a été enfoncée avec un élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="17b7e-106">Notifies a header control's parent window that a key has been pressed with an item selected.</span></span> <span data-ttu-id="17b7e-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="17b7e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="17b7e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17b7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b7e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17b7e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17b7e-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations supplémentaires sur la touche qui est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="17b7e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b7e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17b7e-111">Return value</span></span>

<span data-ttu-id="17b7e-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="17b7e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b7e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17b7e-113">Requirements</span></span>



| <span data-ttu-id="17b7e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17b7e-114">Requirement</span></span> | <span data-ttu-id="17b7e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="17b7e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17b7e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17b7e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17b7e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17b7e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17b7e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17b7e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17b7e-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17b7e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17b7e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="17b7e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17b7e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b7e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





