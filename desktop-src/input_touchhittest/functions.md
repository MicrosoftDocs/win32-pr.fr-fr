---
title: Fonctions (test d’atteinte tactile)
description: Les rubriques de cette section fournissent les spécifications de référence pour les fonctions tactiles de test de positionnement.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- intervention de l'utilisateur
- entrée
- pointeur
- interface tactile
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106534936"
---
# <a name="touch-hit-testing-functions"></a><span data-ttu-id="3eb1d-107">Fonctions de test de positionnement tactile</span><span class="sxs-lookup"><span data-stu-id="3eb1d-107">Touch Hit Testing functions</span></span>

<span data-ttu-id="3eb1d-108">Les rubriques de cette section fournissent les spécifications de référence pour les [fonctions tactiles de test de positionnement](functions.md).</span><span class="sxs-lookup"><span data-stu-id="3eb1d-108">The topics in this section provide the reference specifications for [Touch Hit Testing functions](functions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3eb1d-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3eb1d-109">In this section</span></span>

| <span data-ttu-id="3eb1d-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3eb1d-110">Topic</span></span> | <span data-ttu-id="3eb1d-111">Description</span><span class="sxs-lookup"><span data-stu-id="3eb1d-111">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="3eb1d-112">**EvaluateProximityToPolygon**</span><span class="sxs-lookup"><span data-stu-id="3eb1d-112">**EvaluateProximityToPolygon**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | <span data-ttu-id="3eb1d-113">Retourne le score d’un polygone en tant que cible tactile probable (par rapport à tous les autres polygones qui croisent la zone de contact tactile) et un point tactile ajusté dans le polygone.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-113">Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.</span></span> <br/> |
| [<span data-ttu-id="3eb1d-114">**EvaluateProximityToRect**</span><span class="sxs-lookup"><span data-stu-id="3eb1d-114">**EvaluateProximityToRect**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | <span data-ttu-id="3eb1d-115">Retourne le score d’un rectangle en tant que cible tactile probable, par rapport à tous les autres rectangles qui croisent la zone de contact tactile et un point tactile ajusté dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-115">Returns the score of a rectangle as the probable touch target, compared to all other rectangles that intersect the touch contact area, and an adjusted touch point within the rectangle.</span></span> <br/> |
| [<span data-ttu-id="3eb1d-116">**PackTouchHitTestingProximityEvaluation**</span><span class="sxs-lookup"><span data-stu-id="3eb1d-116">**PackTouchHitTestingProximityEvaluation**</span></span>](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | <span data-ttu-id="3eb1d-117">Retourne le score d’évaluation de proximité et les coordonnées de point tactile ajustées comme valeur compressée pour le rappel de [message WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb1d-117">Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the [WM_TOUCHHITTESTING message](../inputmsg/wm-touchhittesting.md) callback.</span></span> <br/> |
| [<span data-ttu-id="3eb1d-118">**RegisterTouchHitTestingWindow**</span><span class="sxs-lookup"><span data-stu-id="3eb1d-118">**RegisterTouchHitTestingWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | <span data-ttu-id="3eb1d-119">Inscrit une fenêtre pour traiter l' [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span><span class="sxs-lookup"><span data-stu-id="3eb1d-119">Registers a window to process the [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="3eb1d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3eb1d-120">Related topics</span></span>

[<span data-ttu-id="3eb1d-121">Référence de test de positionnement tactile</span><span class="sxs-lookup"><span data-stu-id="3eb1d-121">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)
