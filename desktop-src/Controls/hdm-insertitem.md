---
title: Message HDM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle header. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro en-tête \_ InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465375"
---
# <a name="hdm_insertitem-message"></a><span data-ttu-id="3b28c-105">\_Message HDM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="3b28c-105">HDM\_INSERTITEM message</span></span>

<span data-ttu-id="3b28c-106">Insère un nouvel élément dans un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="3b28c-106">Inserts a new item into a header control.</span></span> <span data-ttu-id="3b28c-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**en-tête \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="3b28c-107">You can send this message explicitly or use the [**Header\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b28c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b28c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b28c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b28c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b28c-110">Index de l’élément après lequel le nouvel élément doit être inséré.</span><span class="sxs-lookup"><span data-stu-id="3b28c-110">The index of the item after which the new item is to be inserted.</span></span> <span data-ttu-id="3b28c-111">Le nouvel élément est inséré à la fin du contrôle header si *wParam* est supérieur ou égal au nombre d’éléments dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3b28c-111">The new item is inserted at the end of the header control if *wParam* is greater than or equal to the number of items in the control.</span></span> <span data-ttu-id="3b28c-112">Si *wParam* est égal à zéro, le nouvel élément est inséré au début du contrôle header.</span><span class="sxs-lookup"><span data-stu-id="3b28c-112">If *wParam* is zero, the new item is inserted at the beginning of the header control.</span></span>

</dd> <dt>

<span data-ttu-id="3b28c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b28c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b28c-114">Pointeur vers une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) qui contient des informations sur le nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="3b28c-114">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains information about the new item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b28c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b28c-115">Return value</span></span>

<span data-ttu-id="3b28c-116">Retourne l’index du nouvel élément en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3b28c-116">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b28c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b28c-117">Requirements</span></span>



| <span data-ttu-id="3b28c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b28c-118">Requirement</span></span> | <span data-ttu-id="3b28c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b28c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b28c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b28c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b28c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b28c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b28c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b28c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b28c-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b28c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b28c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b28c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b28c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b28c-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3b28c-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="3b28c-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3b28c-127">**HDM \_ INSERTITEMW** (Unicode) et **HDM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3b28c-127">**HDM\_INSERTITEMW** (Unicode) and **HDM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





