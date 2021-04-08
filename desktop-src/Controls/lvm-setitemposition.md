---
title: Message LVM_SETITEMPOSITION (commctrl. h)
description: Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône). Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemPosition.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843666"
---
# <a name="lvm_setitemposition-message"></a><span data-ttu-id="d54b8-105">\_Message SETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="d54b8-105">LVM\_SETITEMPOSITION message</span></span>

<span data-ttu-id="d54b8-106">Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône).</span><span class="sxs-lookup"><span data-stu-id="d54b8-106">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="d54b8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .</span><span class="sxs-lookup"><span data-stu-id="d54b8-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d54b8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d54b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d54b8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d54b8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d54b8-110">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="d54b8-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="d54b8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d54b8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d54b8-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la nouvelle position x du coin supérieur gauche de l’élément, dans les coordonnées de la vue.</span><span class="sxs-lookup"><span data-stu-id="d54b8-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new x-position of the item's upper-left corner, in view coordinates.</span></span> <span data-ttu-id="d54b8-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la nouvelle position y du coin supérieur gauche de l’élément, dans les coordonnées de la vue.</span><span class="sxs-lookup"><span data-stu-id="d54b8-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new y-position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d54b8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d54b8-114">Return value</span></span>

<span data-ttu-id="d54b8-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d54b8-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d54b8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d54b8-116">Remarks</span></span>

<span data-ttu-id="d54b8-117">Si le contrôle de vue de liste a le style de [**\_ réorganisation LVS**](list-view-window-styles.md) , les éléments du contrôle d’affichage de liste sont disposés après la définition de la position de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d54b8-117">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, the items in the list-view control are arranged after the position of the item is set.</span></span>

<span data-ttu-id="d54b8-118">Sur Windows Vista, l’envoi de ce message à un contrôle List-View avec le style [**\_ AutoArrange LVS**](list-view-window-styles.md) ne fait rien, et la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="d54b8-118">On Windows Vista, sending this message to a list-view control with the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style does nothing, and the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d54b8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d54b8-119">Requirements</span></span>



| <span data-ttu-id="d54b8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d54b8-120">Requirement</span></span> | <span data-ttu-id="d54b8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d54b8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d54b8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d54b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d54b8-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d54b8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d54b8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d54b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d54b8-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d54b8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d54b8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d54b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d54b8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d54b8-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

