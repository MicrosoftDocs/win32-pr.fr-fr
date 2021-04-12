---
title: Message UDM_GETRANGE (commctrl. h)
description: Récupère les positions minimale et maximale (plage) pour un contrôle up-up.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200588"
---
# <a name="udm_getrange-message"></a><span data-ttu-id="6f7e3-104">\_Message GETRANGE UDM</span><span class="sxs-lookup"><span data-stu-id="6f7e3-104">UDM\_GETRANGE message</span></span>

<span data-ttu-id="6f7e3-105">Récupère les positions minimale et maximale (plage) pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-105">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f7e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f7e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f7e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f7e3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f7e3-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f7e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f7e3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6f7e3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f7e3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f7e3-111">Return value</span></span>

<span data-ttu-id="6f7e3-112">La valeur de retour est une valeur 32 bits qui contient les positions minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-112">The return value is a 32-bit value that contains the minimum and maximum positions.</span></span> <span data-ttu-id="6f7e3-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est la position maximale du contrôle et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est la position minimale.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum position for the control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f7e3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f7e3-114">Requirements</span></span>



| <span data-ttu-id="6f7e3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f7e3-115">Requirement</span></span> | <span data-ttu-id="6f7e3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f7e3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7e3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7e3-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f7e3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f7e3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7e3-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f7e3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f7e3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f7e3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f7e3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f7e3-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

