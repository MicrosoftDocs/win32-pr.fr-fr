---
title: Message LVM_SETSELECTIONMARK (commctrl. h)
description: Définit la marque de sélection dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetSelectionMark.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739933"
---
# <a name="lvm_setselectionmark-message"></a><span data-ttu-id="ea6de-105">\_Message SETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="ea6de-105">LVM\_SETSELECTIONMARK message</span></span>

<span data-ttu-id="ea6de-106">Définit la marque de sélection dans un contrôle de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="ea6de-106">Sets the selection mark in a list-view control.</span></span> <span data-ttu-id="ea6de-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="ea6de-107">You can send this message explicitly or use the [**ListView\_SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea6de-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea6de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea6de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea6de-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea6de-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ea6de-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ea6de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea6de-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea6de-112">Index de base zéro de la nouvelle marque de sélection.</span><span class="sxs-lookup"><span data-stu-id="ea6de-112">Zero-based index of the new selection mark.</span></span> <span data-ttu-id="ea6de-113">Si la valeur est-1, la marque de sélection est supprimée.</span><span class="sxs-lookup"><span data-stu-id="ea6de-113">If set to -1, the selection mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea6de-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea6de-114">Return value</span></span>

<span data-ttu-id="ea6de-115">Retourne la marque de sélection précédente, ou-1 s’il n’y a aucune marque de sélection précédente.</span><span class="sxs-lookup"><span data-stu-id="ea6de-115">Returns the previous selection mark, or -1 if there is no previous selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea6de-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ea6de-116">Remarks</span></span>

<span data-ttu-id="ea6de-117">La *marque de sélection* est l’index d’élément à partir duquel commence une sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="ea6de-117">The *selection mark* is the item index from which a multiple selection starts.</span></span> <span data-ttu-id="ea6de-118">Ce message n’affecte pas l’état de sélection de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ea6de-118">This message does not affect the selection state of the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea6de-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea6de-119">Requirements</span></span>



| <span data-ttu-id="ea6de-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea6de-120">Requirement</span></span> | <span data-ttu-id="ea6de-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea6de-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6de-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea6de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea6de-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea6de-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea6de-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea6de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea6de-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea6de-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea6de-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea6de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea6de-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea6de-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea6de-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea6de-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6de-129">**\_GETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="ea6de-129">**LVM\_GETSELECTIONMARK**</span></span>](lvm-getselectionmark.md)
</dt> </dl>

 

 





