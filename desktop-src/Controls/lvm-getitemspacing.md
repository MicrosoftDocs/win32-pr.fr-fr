---
title: Message LVM_GETITEMSPACING (commctrl. h)
description: Détermine l’espacement entre les éléments d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemSpacing.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942650"
---
# <a name="lvm_getitemspacing-message"></a><span data-ttu-id="66b17-105">\_Message GETITEMSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="66b17-105">LVM\_GETITEMSPACING message</span></span>

<span data-ttu-id="66b17-106">Détermine l’espacement entre les éléments d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="66b17-106">Determines the spacing between items in a list-view control.</span></span> <span data-ttu-id="66b17-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .</span><span class="sxs-lookup"><span data-stu-id="66b17-107">You can send this message explicitly or by using the [**ListView\_GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="66b17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66b17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b17-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66b17-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66b17-110">Vue pour laquelle récupérer l’espacement des éléments.</span><span class="sxs-lookup"><span data-stu-id="66b17-110">View for which to retrieve the item spacing.</span></span> <span data-ttu-id="66b17-111">Ce paramètre est **vrai** pour la vue petite icône ou **false** pour la vue icône.</span><span class="sxs-lookup"><span data-stu-id="66b17-111">This parameter is **TRUE** for small icon view, or **FALSE** for icon view.</span></span>

</dd> <dt>

<span data-ttu-id="66b17-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66b17-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="66b17-113">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="66b17-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b17-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66b17-114">Return value</span></span>

<span data-ttu-id="66b17-115">Retourne la quantité d’espacement entre les éléments.</span><span class="sxs-lookup"><span data-stu-id="66b17-115">Returns the amount of spacing between items.</span></span> <span data-ttu-id="66b17-116">L’espacement horizontal est contenu dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et l’espacement vertical est contenu dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="66b17-116">The horizontal spacing is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical spacing is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="66b17-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66b17-117">Requirements</span></span>



| <span data-ttu-id="66b17-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66b17-118">Requirement</span></span> | <span data-ttu-id="66b17-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="66b17-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66b17-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66b17-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66b17-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66b17-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66b17-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66b17-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66b17-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66b17-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66b17-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="66b17-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b17-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b17-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

