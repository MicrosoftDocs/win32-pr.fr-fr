---
title: Message SB_ISSIMPLE (commctrl. h)
description: Vérifie un contrôle de barre d’État pour déterminer s’il est en mode simple.
ms.assetid: f4362bc3-1852-4569-af9b-96d2da4f0606
keywords:
- SB_ISSIMPLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_ISSIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a5c523bef45065b103051962d7f147816c505d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105076"
---
# <a name="sb_issimple-message"></a><span data-ttu-id="3621e-104">\_Message SB ISSIMPLE</span><span class="sxs-lookup"><span data-stu-id="3621e-104">SB\_ISSIMPLE message</span></span>

<span data-ttu-id="3621e-105">Vérifie un contrôle de barre d’État pour déterminer s’il est en mode simple.</span><span class="sxs-lookup"><span data-stu-id="3621e-105">Checks a status bar control to determine if it is in simple mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="3621e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3621e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3621e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3621e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3621e-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3621e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3621e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3621e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3621e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3621e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3621e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3621e-111">Return value</span></span>

<span data-ttu-id="3621e-112">Retourne une valeur différente de zéro si le contrôle de barre d’État est en mode simple, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3621e-112">Returns nonzero if the status bar control is in simple mode, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3621e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3621e-113">Requirements</span></span>



| <span data-ttu-id="3621e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3621e-114">Requirement</span></span> | <span data-ttu-id="3621e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3621e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3621e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3621e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3621e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3621e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3621e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3621e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3621e-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3621e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3621e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3621e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3621e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3621e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





