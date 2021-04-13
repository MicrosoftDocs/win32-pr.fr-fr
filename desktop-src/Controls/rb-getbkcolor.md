---
title: Message RB_GETBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan par défaut d’un contrôle rebar.
ms.assetid: be90d1ce-a1f8-446d-ae64-001f7174ab05
keywords:
- RB_GETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0c6f2348dfa54dc02ddc40658fd1289885ff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466079"
---
# <a name="rb_getbkcolor-message"></a><span data-ttu-id="2f0ac-104">\_Message GETBKCOLOR RB</span><span class="sxs-lookup"><span data-stu-id="2f0ac-104">RB\_GETBKCOLOR message</span></span>

<span data-ttu-id="2f0ac-105">Récupère la couleur d’arrière-plan par défaut d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-105">Retrieves a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f0ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f0ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f0ac-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f0ac-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f0ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f0ac-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f0ac-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f0ac-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f0ac-111">Return value</span></span>

<span data-ttu-id="2f0ac-112">Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan par défaut actuelle.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represent the current default background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f0ac-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f0ac-113">Requirements</span></span>



| <span data-ttu-id="2f0ac-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f0ac-114">Requirement</span></span> | <span data-ttu-id="2f0ac-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f0ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0ac-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f0ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f0ac-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f0ac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f0ac-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f0ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f0ac-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f0ac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f0ac-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f0ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f0ac-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f0ac-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f0ac-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f0ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f0ac-123">**\_SETBKCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="2f0ac-123">**RB\_SETBKCOLOR**</span></span>](rb-setbkcolor.md)
</dt> </dl>

 

