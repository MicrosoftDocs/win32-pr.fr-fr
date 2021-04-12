---
title: Message TB_GETCOLORSCHEME (commctrl. h)
description: Récupère les informations de modèle de couleur à partir du contrôle ToolBar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- TB_GETCOLORSCHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465567"
---
# <a name="tb_getcolorscheme-message"></a><span data-ttu-id="14cb9-104">TO \_ GETCOLORSCHEME message</span><span class="sxs-lookup"><span data-stu-id="14cb9-104">TB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="14cb9-105">Récupère les informations de modèle de couleur à partir du contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="14cb9-105">Retrieves the color scheme information from the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="14cb9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14cb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14cb9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14cb9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="14cb9-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="14cb9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="14cb9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14cb9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14cb9-110">Pointeur vers une structure [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) qui recevra les informations de modèle de couleurs.</span><span class="sxs-lookup"><span data-stu-id="14cb9-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="14cb9-111">Vous devez définir le membre **cbSize** de cette structure sur **sizeof**(COLORSCHEME) avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="14cb9-111">You must set the **cbSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14cb9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14cb9-112">Return value</span></span>

<span data-ttu-id="14cb9-113">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="14cb9-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="14cb9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14cb9-114">Requirements</span></span>



| <span data-ttu-id="14cb9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14cb9-115">Requirement</span></span> | <span data-ttu-id="14cb9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="14cb9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14cb9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14cb9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14cb9-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14cb9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14cb9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14cb9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14cb9-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14cb9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14cb9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="14cb9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14cb9-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14cb9-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14cb9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14cb9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14cb9-124">**TO \_ SETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="14cb9-124">**TB\_SETCOLORSCHEME**</span></span>](tb-setcolorscheme.md)
</dt> </dl>

 

 





