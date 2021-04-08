---
title: Message TCM_GETIMAGELIST (commctrl. h)
description: Récupère la liste d’images associée à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetImageList.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- TCM_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844182"
---
# <a name="tcm_getimagelist-message"></a><span data-ttu-id="9ad0b-105">\_Message GETIMAGELIST TCM</span><span class="sxs-lookup"><span data-stu-id="9ad0b-105">TCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="9ad0b-106">Récupère la liste d’images associée à un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="9ad0b-106">Retrieves the image list associated with a tab control.</span></span> <span data-ttu-id="9ad0b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="9ad0b-107">You can send this message explicitly or by using the [**TabCtrl\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ad0b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ad0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ad0b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ad0b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ad0b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9ad0b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9ad0b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ad0b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9ad0b-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9ad0b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ad0b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ad0b-113">Return value</span></span>

<span data-ttu-id="9ad0b-114">Retourne le handle de la liste d’images en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9ad0b-114">Returns the handle to the image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad0b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ad0b-115">Requirements</span></span>



| <span data-ttu-id="9ad0b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ad0b-116">Requirement</span></span> | <span data-ttu-id="9ad0b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ad0b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad0b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ad0b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad0b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ad0b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ad0b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ad0b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad0b-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ad0b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ad0b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ad0b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ad0b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ad0b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





