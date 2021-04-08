---
title: Message LVM_GETSELECTEDCOUNT (commctrl. h)
description: Détermine le nombre d’éléments sélectionnés dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetSelectedCount.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- LVM_GETSELECTEDCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844093"
---
# <a name="lvm_getselectedcount-message"></a><span data-ttu-id="78732-105">\_Message GETSELECTEDCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="78732-105">LVM\_GETSELECTEDCOUNT message</span></span>

<span data-ttu-id="78732-106">Détermine le nombre d’éléments sélectionnés dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="78732-106">Determines the number of selected items in a list-view control.</span></span> <span data-ttu-id="78732-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) .</span><span class="sxs-lookup"><span data-stu-id="78732-107">You can send this message explicitly or by using the [**ListView\_GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="78732-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78732-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78732-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78732-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="78732-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="78732-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="78732-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78732-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="78732-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="78732-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78732-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78732-113">Return value</span></span>

<span data-ttu-id="78732-114">Retourne le nombre d’éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="78732-114">Returns the number of selected items.</span></span>

## <a name="requirements"></a><span data-ttu-id="78732-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78732-115">Requirements</span></span>



| <span data-ttu-id="78732-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78732-116">Requirement</span></span> | <span data-ttu-id="78732-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="78732-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78732-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78732-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78732-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78732-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78732-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78732-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78732-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78732-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78732-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="78732-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78732-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78732-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





