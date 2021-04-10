---
title: Message LVM_UPDATE (commctrl. h)
description: Met à jour un élément d’affichage de liste. Si le contrôle List-View a le \_ style de réorganisation LVS, cette macro provoque la disposition du contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro Update de ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843145"
---
# <a name="lvm_update-message"></a><span data-ttu-id="8c83e-106">\_Message de mise à jour LVM</span><span class="sxs-lookup"><span data-stu-id="8c83e-106">LVM\_UPDATE message</span></span>

<span data-ttu-id="8c83e-107">Met à jour un élément d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="8c83e-107">Updates a list-view item.</span></span> <span data-ttu-id="8c83e-108">Si le contrôle List-View a le style de [**\_ réorganisation LVS**](list-view-window-styles.md) , cette macro provoque la disposition du contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="8c83e-108">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, this macro causes the list-view control to be arranged.</span></span> <span data-ttu-id="8c83e-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ Update de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .</span><span class="sxs-lookup"><span data-stu-id="8c83e-109">You can send this message explicitly or by using the [**ListView\_Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c83e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c83e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c83e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c83e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c83e-112">Index de l’élément à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="8c83e-112">Index of the item to update.</span></span>

</dd> <dt>

<span data-ttu-id="8c83e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c83e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8c83e-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8c83e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c83e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c83e-115">Return value</span></span>

<span data-ttu-id="8c83e-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8c83e-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c83e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c83e-117">Requirements</span></span>



| <span data-ttu-id="8c83e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c83e-118">Requirement</span></span> | <span data-ttu-id="8c83e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c83e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c83e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c83e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c83e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c83e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c83e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c83e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c83e-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c83e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c83e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c83e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c83e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c83e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





