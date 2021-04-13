---
title: Message RB_GETDROPTARGET (commctrl. h)
description: Récupère le pointeur d’interface IDropTarget d’un contrôle rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466078"
---
# <a name="rb_getdroptarget-message"></a><span data-ttu-id="92fd5-104">\_Message GETDROPTARGET RB</span><span class="sxs-lookup"><span data-stu-id="92fd5-104">RB\_GETDROPTARGET message</span></span>

<span data-ttu-id="92fd5-105">Récupère le pointeur d’interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="92fd5-105">Retrieves a rebar control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span>

## <a name="parameters"></a><span data-ttu-id="92fd5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92fd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92fd5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92fd5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92fd5-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="92fd5-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="92fd5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92fd5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92fd5-110">Pointeur vers un pointeur [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) qui reçoit le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="92fd5-110">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="92fd5-111">Il incombe à l’appelant d’appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur ce pointeur lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="92fd5-111">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92fd5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92fd5-112">Return value</span></span>

<span data-ttu-id="92fd5-113">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="92fd5-113">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="92fd5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92fd5-114">Requirements</span></span>



| <span data-ttu-id="92fd5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92fd5-115">Requirement</span></span> | <span data-ttu-id="92fd5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="92fd5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92fd5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92fd5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="92fd5-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92fd5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92fd5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92fd5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="92fd5-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92fd5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92fd5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="92fd5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="92fd5-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92fd5-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

