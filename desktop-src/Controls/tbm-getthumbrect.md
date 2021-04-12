---
title: Message TBM_GETTHUMBRECT (commctrl. h)
description: Récupère la taille et la position du rectangle englobant pour le curseur dans un TrackBar.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032883"
---
# <a name="tbm_getthumbrect-message"></a><span data-ttu-id="78712-104">\_Message TBM GETTHUMBRECT</span><span class="sxs-lookup"><span data-stu-id="78712-104">TBM\_GETTHUMBRECT message</span></span>

<span data-ttu-id="78712-105">Récupère la taille et la position du rectangle englobant pour le curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="78712-105">Retrieves the size and position of the bounding rectangle for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="78712-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78712-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78712-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="78712-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="78712-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="78712-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78712-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78712-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="78712-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="78712-111">Le message remplit cette structure à l’aide du rectangle englobant du curseur de la barre de défilement dans les coordonnées clientes de la fenêtre du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="78712-111">The message fills this structure with the bounding rectangle of the trackbar's slider in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78712-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78712-112">Return value</span></span>

<span data-ttu-id="78712-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="78712-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="78712-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78712-114">Requirements</span></span>



| <span data-ttu-id="78712-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78712-115">Requirement</span></span> | <span data-ttu-id="78712-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="78712-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78712-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78712-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78712-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78712-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78712-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78712-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78712-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78712-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78712-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="78712-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="78712-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78712-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

