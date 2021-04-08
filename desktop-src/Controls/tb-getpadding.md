---
title: Message TB_GETPADDING (commctrl. h)
description: Récupère le remplissage pour un contrôle de barre d’outils.
ms.assetid: dde0f44d-5d22-4cab-a7f8-48d84b8995d3
keywords:
- TB_GETPADDING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15babf2fd5d97377991d1827ea8947e9d794600
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033202"
---
# <a name="tb_getpadding-message"></a><span data-ttu-id="5f5c0-104">TO \_ GETPADDING message</span><span class="sxs-lookup"><span data-stu-id="5f5c0-104">TB\_GETPADDING message</span></span>

<span data-ttu-id="5f5c0-105">Récupère le remplissage pour un contrôle de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="5f5c0-105">Retrieves the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f5c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f5c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f5c0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f5c0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f5c0-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5f5c0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5f5c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f5c0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f5c0-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5f5c0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f5c0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f5c0-111">Return value</span></span>

<span data-ttu-id="5f5c0-112">Retourne une valeur **DWORD** qui contient la marge intérieure horizontale dans le mot bas et la marge intérieure verticale dans le mot haut, en pixels.</span><span class="sxs-lookup"><span data-stu-id="5f5c0-112">Returns a **DWORD** value that contains the horizontal padding in the low word and the vertical padding in the high word, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5c0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f5c0-113">Requirements</span></span>



| <span data-ttu-id="5f5c0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f5c0-114">Requirement</span></span> | <span data-ttu-id="5f5c0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f5c0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5c0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f5c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5c0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f5c0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f5c0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f5c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5c0-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f5c0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f5c0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f5c0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5c0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f5c0-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f5c0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f5c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5c0-123">**TO \_ SETPADDING**</span><span class="sxs-lookup"><span data-stu-id="5f5c0-123">**TB\_SETPADDING**</span></span>](tb-setpadding.md)
</dt> </dl>

 

 





