---
title: Message TTM_SETMAXTIPWIDTH (commctrl. h)
description: Définit la largeur maximale d’une fenêtre d’info-bulle.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200553"
---
# <a name="ttm_setmaxtipwidth-message"></a><span data-ttu-id="8d320-104">\_Message atténuation SETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="8d320-104">TTM\_SETMAXTIPWIDTH message</span></span>

<span data-ttu-id="8d320-105">Définit la largeur maximale d’une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="8d320-105">Sets the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d320-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d320-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d320-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d320-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8d320-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d320-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d320-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d320-110">Largeur maximale de la fenêtre d’info-bulle, ou-1 pour autoriser toute largeur.</span><span class="sxs-lookup"><span data-stu-id="8d320-110">Maximum tooltip window width, or -1 to allow any width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d320-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d320-111">Return value</span></span>

<span data-ttu-id="8d320-112">Retourne la largeur d’info-bulle maximale précédente.</span><span class="sxs-lookup"><span data-stu-id="8d320-112">Returns the previous maximum tooltip width.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d320-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8d320-113">Remarks</span></span>

<span data-ttu-id="8d320-114">La valeur de largeur maximale n’indique pas la largeur réelle d’une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="8d320-114">The maximum width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="8d320-115">Au lieu de cela, si une chaîne d’info-bulle dépasse la largeur maximale, le contrôle divise le texte en plusieurs lignes, à l’aide d’espaces pour déterminer les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="8d320-115">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="8d320-116">Si le texte ne peut pas être segmenté en plusieurs lignes, il est affiché sur une seule ligne, qui peut dépasser la largeur d’info-bulle maximale.</span><span class="sxs-lookup"><span data-stu-id="8d320-116">If the text cannot be segmented into multiple lines, it is displayed on a single line, which may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d320-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d320-117">Requirements</span></span>



| <span data-ttu-id="8d320-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d320-118">Requirement</span></span> | <span data-ttu-id="8d320-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d320-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d320-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d320-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d320-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d320-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d320-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d320-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d320-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d320-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d320-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d320-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d320-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d320-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d320-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d320-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d320-127">**ATTÉNUATION \_ GETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="8d320-127">**TTM\_GETMAXTIPWIDTH**</span></span>](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





