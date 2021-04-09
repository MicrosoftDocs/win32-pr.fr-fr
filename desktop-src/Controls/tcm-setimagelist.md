---
title: Message TCM_SETIMAGELIST (commctrl. h)
description: Assigne une liste d’images à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetImageList.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- TCM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032338"
---
# <a name="tcm_setimagelist-message"></a><span data-ttu-id="36824-105">\_Message SETIMAGELIST TCM</span><span class="sxs-lookup"><span data-stu-id="36824-105">TCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="36824-106">Assigne une liste d’images à un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="36824-106">Assigns an image list to a tab control.</span></span> <span data-ttu-id="36824-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="36824-107">You can send this message explicitly or by using the [**TabCtrl\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36824-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36824-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36824-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36824-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="36824-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="36824-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="36824-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36824-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36824-112">Handle de la liste d’images à assigner au contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="36824-112">Handle to the image list to assign to the tab control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36824-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36824-113">Return value</span></span>

<span data-ttu-id="36824-114">Retourne le handle de la liste d’images précédente, ou **null** s’il n’existe aucune liste d’images précédente.</span><span class="sxs-lookup"><span data-stu-id="36824-114">Returns the handle to the previous image list, or **NULL** if there is no previous image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="36824-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36824-115">Requirements</span></span>



| <span data-ttu-id="36824-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36824-116">Requirement</span></span> | <span data-ttu-id="36824-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="36824-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36824-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36824-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36824-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36824-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36824-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36824-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36824-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36824-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36824-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="36824-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36824-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36824-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





