---
description: Les primitives qui se trouvent partiellement à l’intérieur (ou complètement à l’extérieur) de la vue frustum peuvent être découpées afin que seule la partie visible de la primitive soit rendue.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: État de découpage primitif (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392884"
---
# <a name="primitive-clipping-state-direct3d-9"></a><span data-ttu-id="9abba-103">État de découpage primitif (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9abba-103">Primitive Clipping State (Direct3D 9)</span></span>

<span data-ttu-id="9abba-104">Les primitives qui se trouvent partiellement à l’intérieur (ou complètement à l’extérieur) de la [vue frustum](viewports-and-clipping.md) peuvent être découpées afin que seule la partie visible de la primitive soit rendue.</span><span class="sxs-lookup"><span data-stu-id="9abba-104">Primitives that lie partially inside (or completely outside) the [view frustum](viewports-and-clipping.md) can be clipped so that only the visible portion of the primitive will be rendered.</span></span> <span data-ttu-id="9abba-105">Le découpage réduit la quantité de travail qui est effectuée uniquement pour les primitives ou les parties d’une primitive qui seront visibles.</span><span class="sxs-lookup"><span data-stu-id="9abba-105">Clipping reduces the amount of work that is done to only those primitives or portions of a primitive that will be visible.</span></span>

<span data-ttu-id="9abba-106">Pour utiliser le pipeline pour le découpage, définissez l' \_ État de rendu du découpage D3DRS sur **true** (valeur par défaut) pour activer le découpage, ou sur **false** pour désactiver le découpage Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9abba-106">To use the pipeline for clipping, set the D3DRS\_CLIPPING render state to **TRUE** (the default value) to enable clipping, or to **FALSE** to disable Direct3D clipping.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9abba-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9abba-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9abba-108">États de rendu</span><span class="sxs-lookup"><span data-stu-id="9abba-108">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



