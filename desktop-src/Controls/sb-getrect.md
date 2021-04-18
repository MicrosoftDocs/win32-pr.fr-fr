---
title: Message SB_GETRECT (commctrl. h)
description: Récupère le rectangle englobant d’un composant dans une fenêtre d’État.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- SB_GETRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466231"
---
# <a name="sb_getrect-message"></a><span data-ttu-id="08dc0-104">\_Message SB GETRECT</span><span class="sxs-lookup"><span data-stu-id="08dc0-104">SB\_GETRECT message</span></span>

<span data-ttu-id="08dc0-105">Récupère le rectangle englobant d’un composant dans une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="08dc0-105">Retrieves the bounding rectangle of a part in a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="08dc0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08dc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08dc0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08dc0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc0-108">Index de base zéro du composant dont le rectangle englobant doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="08dc0-108">Zero-based index of the part whose bounding rectangle is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="08dc0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08dc0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08dc0-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="08dc0-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08dc0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08dc0-111">Return value</span></span>

<span data-ttu-id="08dc0-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="08dc0-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="08dc0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08dc0-113">Requirements</span></span>



| <span data-ttu-id="08dc0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08dc0-114">Requirement</span></span> | <span data-ttu-id="08dc0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="08dc0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08dc0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08dc0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08dc0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08dc0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08dc0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08dc0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08dc0-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08dc0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08dc0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="08dc0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08dc0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08dc0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

