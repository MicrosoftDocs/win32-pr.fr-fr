---
title: Message TTM_GETMAXTIPWIDTH (commctrl. h)
description: Récupère la largeur maximale d’une fenêtre d’info-bulle.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942147"
---
# <a name="ttm_getmaxtipwidth-message"></a><span data-ttu-id="72f11-104">\_Message atténuation GETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="72f11-104">TTM\_GETMAXTIPWIDTH message</span></span>

<span data-ttu-id="72f11-105">Récupère la largeur maximale d’une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="72f11-105">Retrieves the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="72f11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72f11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f11-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72f11-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="72f11-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="72f11-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="72f11-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72f11-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="72f11-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="72f11-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f11-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72f11-111">Return value</span></span>

<span data-ttu-id="72f11-112">Retourne une valeur **int** qui représente la largeur d’info-bulle maximale, en pixels.</span><span class="sxs-lookup"><span data-stu-id="72f11-112">Returns an **INT** value that represents the maximum tooltip width, in pixels.</span></span> <span data-ttu-id="72f11-113">Si aucune largeur maximale n’a été définie précédemment, le message retourne-1.</span><span class="sxs-lookup"><span data-stu-id="72f11-113">If no maximum width was set previously, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f11-114">Notes</span><span class="sxs-lookup"><span data-stu-id="72f11-114">Remarks</span></span>

<span data-ttu-id="72f11-115">La valeur de largeur d’info-bulle maximale n’indique pas la largeur réelle d’une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="72f11-115">The maximum tooltip width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="72f11-116">Au lieu de cela, si une chaîne d’info-bulle dépasse la largeur maximale, le contrôle divise le texte en plusieurs lignes, à l’aide d’espaces pour déterminer les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="72f11-116">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="72f11-117">Si le texte ne peut pas être segmenté en plusieurs lignes, il est affiché sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="72f11-117">If the text cannot be segmented into multiple lines, it will be displayed on a single line.</span></span> <span data-ttu-id="72f11-118">La longueur de cette ligne peut dépasser la largeur d’info-bulle maximale.</span><span class="sxs-lookup"><span data-stu-id="72f11-118">The length of this line may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f11-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72f11-119">Requirements</span></span>



| <span data-ttu-id="72f11-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72f11-120">Requirement</span></span> | <span data-ttu-id="72f11-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="72f11-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72f11-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72f11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="72f11-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72f11-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72f11-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72f11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="72f11-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72f11-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72f11-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="72f11-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f11-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f11-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f11-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72f11-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f11-129">**ATTÉNUATION \_ SETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="72f11-129">**TTM\_SETMAXTIPWIDTH**</span></span>](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





