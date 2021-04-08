---
title: Message HDM_GETIMAGELIST (commctrl. h)
description: Obtient le handle vers la liste d’images qui a été définie pour un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetImageList ou d’en-tête \_ GetStateImageList.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742277"
---
# <a name="hdm_getimagelist-message"></a><span data-ttu-id="5c2b8-105">\_Message HDM GETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="5c2b8-105">HDM\_GETIMAGELIST message</span></span>

<span data-ttu-id="5c2b8-106">Obtient le handle vers la liste d’images qui a été définie pour un contrôle d’en-tête existant.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-106">Gets the handle to the image list that has been set for an existing header control.</span></span> <span data-ttu-id="5c2b8-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en [**-tête \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) ou d' [**en-tête \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) .</span><span class="sxs-lookup"><span data-stu-id="5c2b8-107">You can send this message explicitly or use the [**Header\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) or [**Header\_GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c2b8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c2b8-108">Parameters</span></span>

<dl> <span data-ttu-id="5c2b8-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="5c2b8-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="5c2b8-110">Une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c2b8-110">One of the following values:</span></span>

| <span data-ttu-id="5c2b8-111">Value</span><span class="sxs-lookup"><span data-stu-id="5c2b8-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="5c2b8-112">Signification</span><span class="sxs-lookup"><span data-stu-id="5c2b8-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="5c2b8-113"><dt>**HDSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2b8-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="5c2b8-114">Indique qu’il s’agit d’une liste d’images normale.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="5c2b8-115"><dt>**État de HDSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2b8-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="5c2b8-116">Indique qu’il s’agit d’une liste d’images d’État.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="5c2b8-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c2b8-117">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5c2b8-118">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-118">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2b8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c2b8-119">Return value</span></span>

<span data-ttu-id="5c2b8-120">Retourne un handle vers le jeu de listes d’images pour le contrôle d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-120">Returns a handle to the image list set for the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2b8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c2b8-121">Requirements</span></span>



| <span data-ttu-id="5c2b8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c2b8-122">Requirement</span></span> | <span data-ttu-id="5c2b8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c2b8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2b8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c2b8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2b8-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c2b8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c2b8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c2b8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2b8-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c2b8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c2b8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c2b8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2b8-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2b8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





