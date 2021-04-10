---
title: Message TCM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942702"
---
# <a name="tcm_deleteitem-message"></a><span data-ttu-id="4da31-105">\_Message TCM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="4da31-105">TCM\_DELETEITEM message</span></span>

<span data-ttu-id="4da31-106">Supprime un élément d’un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="4da31-106">Removes an item from a tab control.</span></span> <span data-ttu-id="4da31-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="4da31-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4da31-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4da31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4da31-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4da31-110">Index de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="4da31-110">Index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="4da31-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4da31-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4da31-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4da31-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da31-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4da31-113">Return value</span></span>

<span data-ttu-id="4da31-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4da31-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da31-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4da31-115">Requirements</span></span>



| <span data-ttu-id="4da31-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4da31-116">Requirement</span></span> | <span data-ttu-id="4da31-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4da31-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4da31-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4da31-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4da31-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4da31-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4da31-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4da31-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4da31-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4da31-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4da31-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4da31-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da31-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da31-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





