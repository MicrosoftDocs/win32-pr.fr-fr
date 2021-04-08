---
title: Message LVM_DELETECOLUMN (commctrl. h)
description: Supprime une colonne d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView DeleteColumn.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739972"
---
# <a name="lvm_deletecolumn-message"></a><span data-ttu-id="95323-105">\_Message DELETECOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="95323-105">LVM\_DELETECOLUMN message</span></span>

<span data-ttu-id="95323-106">Supprime une colonne d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="95323-106">Removes a column from a list-view control.</span></span> <span data-ttu-id="95323-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .</span><span class="sxs-lookup"><span data-stu-id="95323-107">You can send this message explicitly or by using the [**ListView\_DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="95323-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95323-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95323-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95323-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95323-110">Index de la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="95323-110">The index of the column to delete.</span></span>

</dd> <dt>

<span data-ttu-id="95323-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95323-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="95323-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="95323-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95323-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95323-113">Return value</span></span>

<span data-ttu-id="95323-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="95323-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="95323-115">Notes</span><span class="sxs-lookup"><span data-stu-id="95323-115">Remarks</span></span>

<span data-ttu-id="95323-116">La suppression de la colonne zéro d’un contrôle List-View est uniquement prise en charge dans ComCtl32.dll version 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="95323-116">Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later.</span></span> <span data-ttu-id="95323-117">La version 5 prend également en charge la suppression de la colonne zéro, mais uniquement après avoir utilisé [**CCM \_ SETVERSION**](ccm-setversion.md) pour définir la version sur 5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="95323-117">Version 5 also supports deleting column zero, but only after you use [**CCM\_SETVERSION**](ccm-setversion.md) to set the version to 5 or later.</span></span> <span data-ttu-id="95323-118">Dans les versions antérieures à la version 5, si vous devez supprimer la colonne zéro, insérez une colonne factice de longueur égale à zéro et supprimez la colonne un et les autres.</span><span class="sxs-lookup"><span data-stu-id="95323-118">In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above.</span></span>

## <a name="requirements"></a><span data-ttu-id="95323-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95323-119">Requirements</span></span>



| <span data-ttu-id="95323-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95323-120">Requirement</span></span> | <span data-ttu-id="95323-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="95323-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95323-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95323-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95323-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95323-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95323-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95323-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95323-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95323-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95323-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="95323-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95323-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95323-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





