---
title: Message LVM_ENSUREVISIBLE (commctrl. h)
description: Garantit qu’un élément de mode liste est entièrement ou partiellement visible, en faisant défiler le contrôle de liste si nécessaire. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView EnsureVisible.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941677"
---
# <a name="lvm_ensurevisible-message"></a><span data-ttu-id="8790b-105">\_Message ENSUREVISIBLE LVM</span><span class="sxs-lookup"><span data-stu-id="8790b-105">LVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="8790b-106">Garantit qu’un élément de mode liste est entièrement ou partiellement visible, en faisant défiler le contrôle de liste si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8790b-106">Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary.</span></span> <span data-ttu-id="8790b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="8790b-107">You can send this message explicitly or by using the [**ListView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8790b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8790b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8790b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8790b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8790b-110">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="8790b-110">The index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="8790b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8790b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8790b-112">Valeur qui spécifie si l’élément doit être entièrement visible.</span><span class="sxs-lookup"><span data-stu-id="8790b-112">A value specifying whether the item must be entirely visible.</span></span> <span data-ttu-id="8790b-113">Si ce paramètre a la **valeur true**, aucun défilement ne se produit si l’élément est au moins partiellement visible.</span><span class="sxs-lookup"><span data-stu-id="8790b-113">If this parameter is **TRUE**, no scrolling occurs if the item is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8790b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8790b-114">Return value</span></span>

<span data-ttu-id="8790b-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8790b-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8790b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8790b-116">Remarks</span></span>

<span data-ttu-id="8790b-117">Le message échoue si le style de fenêtre comprend [**LVS \_ NoScroll**](list-view-window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8790b-117">The message fails if the window style includes [**LVS\_NOSCROLL**](list-view-window-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8790b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8790b-118">Requirements</span></span>



| <span data-ttu-id="8790b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8790b-119">Requirement</span></span> | <span data-ttu-id="8790b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8790b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8790b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8790b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8790b-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8790b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8790b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8790b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8790b-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8790b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8790b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8790b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8790b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8790b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





