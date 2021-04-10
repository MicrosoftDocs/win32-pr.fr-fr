---
title: Message HDM_GETITEMCOUNT (commctrl. h)
description: Obtient le nombre d’éléments dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetItemCount.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- HDM_GETITEMCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104485"
---
# <a name="hdm_getitemcount-message"></a><span data-ttu-id="ace38-105">\_Message HDM GETITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="ace38-105">HDM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="ace38-106">Obtient le nombre d’éléments dans un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="ace38-106">Gets a count of the items in a header control.</span></span> <span data-ttu-id="ace38-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="ace38-107">You can send this message explicitly or use the [**Header\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ace38-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ace38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace38-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ace38-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ace38-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ace38-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ace38-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ace38-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ace38-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ace38-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace38-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ace38-113">Return value</span></span>

<span data-ttu-id="ace38-114">Retourne le nombre d’éléments en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ace38-114">Returns the number of items if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace38-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ace38-115">Requirements</span></span>



| <span data-ttu-id="ace38-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ace38-116">Requirement</span></span> | <span data-ttu-id="ace38-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ace38-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ace38-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ace38-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ace38-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ace38-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ace38-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ace38-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ace38-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ace38-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace38-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace38-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





