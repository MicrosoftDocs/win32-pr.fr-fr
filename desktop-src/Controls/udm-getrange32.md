---
title: Message UDM_GETRANGE32 (commctrl. h)
description: Récupère la plage 32 bits d’un contrôle up-up.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465023"
---
# <a name="udm_getrange32-message"></a><span data-ttu-id="d2650-104">\_Message GETRANGE32 UDM</span><span class="sxs-lookup"><span data-stu-id="d2650-104">UDM\_GETRANGE32 message</span></span>

<span data-ttu-id="d2650-105">Récupère la plage 32 bits d’un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="d2650-105">Retrieves the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2650-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2650-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2650-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2650-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2650-108">Pointeur vers un entier signé qui reçoit la limite inférieure de la plage de contrôles Up-Up.</span><span class="sxs-lookup"><span data-stu-id="d2650-108">Pointer to a signed integer that receives the lower limit of the up-down control range.</span></span> <span data-ttu-id="d2650-109">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d2650-109">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2650-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2650-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2650-111">Pointeur vers un entier signé qui reçoit la limite supérieure de la plage de contrôles Up-Up.</span><span class="sxs-lookup"><span data-stu-id="d2650-111">Pointer to a signed integer that receives the upper limit of the up-down control range.</span></span> <span data-ttu-id="d2650-112">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d2650-112">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2650-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2650-113">Return value</span></span>

<span data-ttu-id="d2650-114">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2650-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2650-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2650-115">Requirements</span></span>



| <span data-ttu-id="d2650-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2650-116">Requirement</span></span> | <span data-ttu-id="d2650-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2650-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2650-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2650-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2650-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2650-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2650-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2650-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2650-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2650-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2650-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2650-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2650-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2650-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





