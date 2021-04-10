---
title: Message UDM_SETBUDDY (commctrl. h)
description: Définit la fenêtre associée pour un contrôle up-up.
ms.assetid: 66e35acc-95f6-4bc5-b654-690abf2188ba
keywords:
- UDM_SETBUDDY les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e8bd57727d730c67fe09a52c0bedf121eac982
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104764"
---
# <a name="udm_setbuddy-message"></a><span data-ttu-id="c912a-104">\_Message SETBUDDY UDM</span><span class="sxs-lookup"><span data-stu-id="c912a-104">UDM\_SETBUDDY message</span></span>

<span data-ttu-id="c912a-105">Définit la fenêtre associée pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="c912a-105">Sets the buddy window for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c912a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c912a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c912a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c912a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c912a-108">Handle vers la nouvelle fenêtre associée.</span><span class="sxs-lookup"><span data-stu-id="c912a-108">Handle to the new buddy window.</span></span>

</dd> <dt>

<span data-ttu-id="c912a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c912a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c912a-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c912a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c912a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c912a-111">Return value</span></span>

<span data-ttu-id="c912a-112">La valeur de retour est le handle de la fenêtre associée précédente.</span><span class="sxs-lookup"><span data-stu-id="c912a-112">The return value is the handle to the previous buddy window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c912a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c912a-113">Requirements</span></span>



| <span data-ttu-id="c912a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c912a-114">Requirement</span></span> | <span data-ttu-id="c912a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c912a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c912a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c912a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c912a-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c912a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c912a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c912a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c912a-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c912a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c912a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c912a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c912a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c912a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





