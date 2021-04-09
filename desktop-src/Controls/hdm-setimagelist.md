---
title: Message HDM_SETIMAGELIST (commctrl. h)
description: Affecte une liste d’images à un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetImageList ou d’en-tête \_ SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942069"
---
# <a name="hdm_setimagelist-message"></a><span data-ttu-id="2dde2-105">\_Message HDM SETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="2dde2-105">HDM\_SETIMAGELIST message</span></span>

<span data-ttu-id="2dde2-106">Affecte une liste d’images à un contrôle d’en-tête existant.</span><span class="sxs-lookup"><span data-stu-id="2dde2-106">Assigns an image list to an existing header control.</span></span> <span data-ttu-id="2dde2-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en [**-tête \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) ou d' [**en-tête \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) .</span><span class="sxs-lookup"><span data-stu-id="2dde2-107">You can send this message explicitly or use the [**Header\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) or [**Header\_SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2dde2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2dde2-108">Parameters</span></span>

<dl> <span data-ttu-id="2dde2-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="2dde2-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="2dde2-110">Une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2dde2-110">One of the following values:</span></span>

| <span data-ttu-id="2dde2-111">Value</span><span class="sxs-lookup"><span data-stu-id="2dde2-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="2dde2-112">Signification</span><span class="sxs-lookup"><span data-stu-id="2dde2-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="2dde2-113"><dt>**HDSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="2dde2-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="2dde2-114">Indique qu’il s’agit d’une liste d’images normale.</span><span class="sxs-lookup"><span data-stu-id="2dde2-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="2dde2-115"><dt>**État de HDSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dde2-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="2dde2-116">Indique qu’il s’agit d’une liste d’images d’État.</span><span class="sxs-lookup"><span data-stu-id="2dde2-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="2dde2-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2dde2-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dde2-118">Handle d’une liste d’images.</span><span class="sxs-lookup"><span data-stu-id="2dde2-118">A handle to an image list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dde2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2dde2-119">Return value</span></span>

<span data-ttu-id="2dde2-120">Retourne le handle de la liste d’images précédemment associée au contrôle.</span><span class="sxs-lookup"><span data-stu-id="2dde2-120">Returns the handle to the image list previously associated with the control.</span></span> <span data-ttu-id="2dde2-121">Retourne la **valeur null** en cas d’échec ou si aucune liste d’images n’a été définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="2dde2-121">Returns **NULL** upon failure or if no image list was set previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dde2-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dde2-122">Requirements</span></span>



| <span data-ttu-id="2dde2-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2dde2-123">Requirement</span></span> | <span data-ttu-id="2dde2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dde2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2dde2-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dde2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2dde2-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2dde2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2dde2-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dde2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2dde2-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2dde2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2dde2-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2dde2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dde2-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dde2-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





