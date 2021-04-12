---
title: Message TCM_GETITEMCOUNT (commctrl. h)
description: Récupère le nombre d’onglets dans le contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- TCM_GETITEMCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105742"
---
# <a name="tcm_getitemcount-message"></a><span data-ttu-id="edc71-105">\_Message GETITEMCOUNT TCM</span><span class="sxs-lookup"><span data-stu-id="edc71-105">TCM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="edc71-106">Récupère le nombre d’onglets dans le contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="edc71-106">Retrieves the number of tabs in the tab control.</span></span> <span data-ttu-id="edc71-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="edc71-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="edc71-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edc71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc71-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edc71-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="edc71-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="edc71-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="edc71-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edc71-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="edc71-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="edc71-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc71-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edc71-113">Return value</span></span>

<span data-ttu-id="edc71-114">Retourne le nombre d’éléments en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="edc71-114">Returns the number of items if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc71-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edc71-115">Requirements</span></span>



| <span data-ttu-id="edc71-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edc71-116">Requirement</span></span> | <span data-ttu-id="edc71-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="edc71-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edc71-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edc71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="edc71-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edc71-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edc71-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edc71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="edc71-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edc71-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edc71-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="edc71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="edc71-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="edc71-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





