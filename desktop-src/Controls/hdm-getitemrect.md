---
title: Message HDM_GETITEMRECT (commctrl. h)
description: Obtient le rectangle englobant pour un élément donné dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetItemRect.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- HDM_GETITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465886"
---
# <a name="hdm_getitemrect-message"></a><span data-ttu-id="5195d-105">\_Message HDM GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="5195d-105">HDM\_GETITEMRECT message</span></span>

<span data-ttu-id="5195d-106">Obtient le rectangle englobant pour un élément donné dans un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="5195d-106">Gets the bounding rectangle for a given item in a header control.</span></span> <span data-ttu-id="5195d-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="5195d-107">You can send this message explicitly or use the [**Header\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5195d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5195d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5195d-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5195d-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5195d-110">Index de base zéro de l’élément de contrôle d’en-tête pour lequel récupérer le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="5195d-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="5195d-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5195d-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5195d-112">Pointeur vers une structure [**Rect**](/windows/win32/api/windef/ns-windef-rect) qui reçoit les informations de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="5195d-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="5195d-113">L’expéditeur du message est chargé d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="5195d-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="5195d-114">Les coordonnées retournées dans la structure RECT sont exprimées par rapport au parent du contrôle header.</span><span class="sxs-lookup"><span data-stu-id="5195d-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5195d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5195d-115">Return value</span></span>

<span data-ttu-id="5195d-116">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5195d-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5195d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5195d-117">Requirements</span></span>



| <span data-ttu-id="5195d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5195d-118">Requirement</span></span> | <span data-ttu-id="5195d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5195d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5195d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5195d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5195d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5195d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5195d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5195d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5195d-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5195d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5195d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5195d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5195d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5195d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





