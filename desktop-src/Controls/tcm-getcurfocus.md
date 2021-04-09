---
title: Message TCM_GETCURFOCUS (commctrl. h)
description: Retourne l’index de l’élément qui a le focus dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetCurFocus.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942700"
---
# <a name="tcm_getcurfocus-message"></a><span data-ttu-id="146a8-105">\_Message GETCURFOCUS TCM</span><span class="sxs-lookup"><span data-stu-id="146a8-105">TCM\_GETCURFOCUS message</span></span>

<span data-ttu-id="146a8-106">Retourne l’index de l’élément qui a le focus dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="146a8-106">Returns the index of the item that has the focus in a tab control.</span></span> <span data-ttu-id="146a8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="146a8-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="146a8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="146a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="146a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="146a8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="146a8-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="146a8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="146a8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="146a8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="146a8-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="146a8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="146a8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="146a8-113">Return value</span></span>

<span data-ttu-id="146a8-114">Retourne l’index de l’élément d’onglet qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="146a8-114">Returns the index of the tab item that has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="146a8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="146a8-115">Remarks</span></span>

<span data-ttu-id="146a8-116">L’élément qui a le focus peut être différent de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="146a8-116">The item that has the focus may be different than the selected item.</span></span>

## <a name="requirements"></a><span data-ttu-id="146a8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="146a8-117">Requirements</span></span>



| <span data-ttu-id="146a8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="146a8-118">Requirement</span></span> | <span data-ttu-id="146a8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="146a8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="146a8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="146a8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="146a8-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="146a8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="146a8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="146a8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="146a8-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="146a8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="146a8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="146a8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="146a8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="146a8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





