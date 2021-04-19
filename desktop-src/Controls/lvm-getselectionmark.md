---
title: Message LVM_GETSELECTIONMARK (commctrl. h)
description: Récupère la marque de sélection à partir d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetSelectionMark.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518104"
---
# <a name="lvm_getselectionmark-message"></a><span data-ttu-id="cef84-105">\_Message GETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="cef84-105">LVM\_GETSELECTIONMARK message</span></span>

<span data-ttu-id="cef84-106">Récupère la marque de sélection à partir d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="cef84-106">Retrieves the selection mark from a list-view control.</span></span> <span data-ttu-id="cef84-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="cef84-107">You can send this message explicitly or use the [**ListView\_GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cef84-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cef84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef84-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cef84-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cef84-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cef84-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cef84-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cef84-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cef84-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cef84-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cef84-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cef84-113">Return value</span></span>

<span data-ttu-id="cef84-114">Retourne la marque de sélection de base zéro ou-1 s’il n’y a aucune marque de sélection.</span><span class="sxs-lookup"><span data-stu-id="cef84-114">Returns the zero-based selection mark, or -1 if there is no selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="cef84-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cef84-115">Remarks</span></span>

<span data-ttu-id="cef84-116">La *marque de sélection* est l’index d’élément à partir duquel commence une sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="cef84-116">The *selection mark* is the item index from which a multiple selection starts.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef84-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cef84-117">Requirements</span></span>



| <span data-ttu-id="cef84-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cef84-118">Requirement</span></span> | <span data-ttu-id="cef84-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cef84-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cef84-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cef84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cef84-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cef84-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cef84-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cef84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cef84-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cef84-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cef84-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cef84-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cef84-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cef84-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cef84-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cef84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef84-127">**\_SETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="cef84-127">**LVM\_SETSELECTIONMARK**</span></span>](lvm-setselectionmark.md)
</dt> </dl>

 

 





