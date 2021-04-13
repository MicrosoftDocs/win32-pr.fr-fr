---
title: Message RB_GETCOLORSCHEME (commctrl. h)
description: Récupère les informations de modèle de couleur à partir du contrôle rebar.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- RB_GETCOLORSCHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508909"
---
# <a name="rb_getcolorscheme-message"></a><span data-ttu-id="72c1d-104">\_Message GETCOLORSCHEME RB</span><span class="sxs-lookup"><span data-stu-id="72c1d-104">RB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="72c1d-105">Récupère les informations de modèle de couleur à partir du contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="72c1d-105">Retrieves the color scheme information from the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="72c1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72c1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72c1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72c1d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="72c1d-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="72c1d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="72c1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72c1d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72c1d-110">Pointeur vers une structure [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) qui recevra les informations de modèle de couleurs.</span><span class="sxs-lookup"><span data-stu-id="72c1d-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="72c1d-111">Vous devez définir le membre **dwSize nul** de cette structure sur **sizeof**(COLORSCHEME) avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="72c1d-111">You must set the **dwSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72c1d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72c1d-112">Return value</span></span>

<span data-ttu-id="72c1d-113">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="72c1d-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="72c1d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72c1d-114">Requirements</span></span>



| <span data-ttu-id="72c1d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72c1d-115">Requirement</span></span> | <span data-ttu-id="72c1d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="72c1d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72c1d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72c1d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72c1d-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72c1d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72c1d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72c1d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72c1d-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72c1d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72c1d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="72c1d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72c1d-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72c1d-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72c1d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72c1d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c1d-124">**\_SETCOLORSCHEME RB**</span><span class="sxs-lookup"><span data-stu-id="72c1d-124">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
</dt> </dl>

 

 





