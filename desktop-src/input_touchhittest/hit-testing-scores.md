---
title: Scores de test d’atteinte tactile
description: Les constantes suivantes identifient les scores de test de positionnement possibles pour un objet, par rapport aux autres objets qui croisent la zone de contact tactile.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508469"
---
# <a name="touch-hit-testing-scores"></a><span data-ttu-id="234b1-103">Scores de test d’atteinte tactile</span><span class="sxs-lookup"><span data-stu-id="234b1-103">Touch Hit Testing Scores</span></span>

<span data-ttu-id="234b1-104">Les constantes suivantes identifient les scores de test de positionnement possibles pour un objet, par rapport aux autres objets qui croisent la zone de contact tactile.</span><span class="sxs-lookup"><span data-stu-id="234b1-104">The following constants identify the possible hit test scores for an object, relative to other objects that intersect the touch contact area.</span></span>

| <span data-ttu-id="234b1-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="234b1-105">Constant/value</span></span> | <span data-ttu-id="234b1-106">Description</span><span class="sxs-lookup"><span data-stu-id="234b1-106">Description</span></span> |
|---|---|
| <span data-ttu-id="234b1-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span><span class="sxs-lookup"><span data-stu-id="234b1-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span></span>      | <span data-ttu-id="234b1-108">L’objet est la cible la plus probable.</span><span class="sxs-lookup"><span data-stu-id="234b1-108">The object is the most probable target.</span></span><br/>  |
| <span data-ttu-id="234b1-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span><span class="sxs-lookup"><span data-stu-id="234b1-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span></span> | <span data-ttu-id="234b1-110">L’objet est la cible la moins probable.</span><span class="sxs-lookup"><span data-stu-id="234b1-110">The object is the least probable target.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="234b1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="234b1-111">Requirements</span></span>

| <span data-ttu-id="234b1-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="234b1-112">Requirement</span></span> | <span data-ttu-id="234b1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="234b1-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="234b1-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="234b1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="234b1-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="234b1-115">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="234b1-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="234b1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="234b1-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="234b1-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="234b1-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="234b1-118">Header</span></span><br/>                   | <span data-ttu-id="234b1-119">Winuser. h</span><span class="sxs-lookup"><span data-stu-id="234b1-119">Winuser.h</span></span> |
