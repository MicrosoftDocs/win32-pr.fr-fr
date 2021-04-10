---
title: Message LVM_GETORIGIN (commctrl. h)
description: Récupère l’origine de la vue actuelle pour un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetOrigin.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105496"
---
# <a name="lvm_getorigin-message"></a><span data-ttu-id="c9e0b-105">\_Message GETORIGIN LVM</span><span class="sxs-lookup"><span data-stu-id="c9e0b-105">LVM\_GETORIGIN message</span></span>

<span data-ttu-id="c9e0b-106">Récupère l’origine de la vue actuelle pour un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="c9e0b-106">Retrieves the current view origin for a list-view control.</span></span> <span data-ttu-id="c9e0b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) .</span><span class="sxs-lookup"><span data-stu-id="c9e0b-107">You can send this message explicitly or by using the [**ListView\_GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9e0b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9e0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9e0b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9e0b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c9e0b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c9e0b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c9e0b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9e0b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9e0b-112">Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui reçoit l’origine de la vue.</span><span class="sxs-lookup"><span data-stu-id="c9e0b-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the view origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9e0b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9e0b-113">Return value</span></span>

<span data-ttu-id="c9e0b-114">Retourne la **valeur true** en cas de réussite, ou **false** si la vue actuelle est une liste ou un affichage des rapports.</span><span class="sxs-lookup"><span data-stu-id="c9e0b-114">Returns **TRUE** if successful, or **FALSE** if the current view is list or report view.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e0b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9e0b-115">Requirements</span></span>



| <span data-ttu-id="c9e0b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9e0b-116">Requirement</span></span> | <span data-ttu-id="c9e0b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9e0b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e0b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9e0b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9e0b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9e0b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9e0b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9e0b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9e0b-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9e0b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9e0b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9e0b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9e0b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9e0b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

