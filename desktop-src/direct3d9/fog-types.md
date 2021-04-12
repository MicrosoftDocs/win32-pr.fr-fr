---
description: 'Il existe deux façons d’ajouter un brouillard à une scène : avec le brouillard de pixel et/ou le brouillard de vertex.'
ms.assetid: 96531830-2df1-40d4-af46-09b1ca153834
title: Types de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5dd845373ac4a42a32ab7a9965501df4894568
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108746"
---
# <a name="fog-types-direct3d-9"></a><span data-ttu-id="fc359-103">Types de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc359-103">Fog Types (Direct3D 9)</span></span>

<span data-ttu-id="fc359-104">Il existe deux façons d’ajouter un brouillard à une scène : avec le brouillard de pixel et/ou le brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="fc359-104">There are two ways to add fog to a scene: with pixel fog and/or vertex fog.</span></span> <span data-ttu-id="fc359-105">Les rubriques suivantes illustrent les formules utilisées dans les équations de brouillard, ainsi que l’implémentation du brouillard de vertex et de pixel.</span><span class="sxs-lookup"><span data-stu-id="fc359-105">The following topics illustrate the formulas used in fog equations, as well as implementing vertex and pixel fog.</span></span> <span data-ttu-id="fc359-106">Une application peut implémenter un brouillard avec un nuanceur de sommets et un brouillard de pixel simultanément, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="fc359-106">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

-   [<span data-ttu-id="fc359-107">Formules de brouillard</span><span class="sxs-lookup"><span data-stu-id="fc359-107">Fog Formulas</span></span>](fog-formulas.md)
-   [<span data-ttu-id="fc359-108">Paramètres de brouillard</span><span class="sxs-lookup"><span data-stu-id="fc359-108">Fog Parameters</span></span>](fog-parameters.md)
-   [<span data-ttu-id="fc359-109">Fusion de brouillard</span><span class="sxs-lookup"><span data-stu-id="fc359-109">Fog Blending</span></span>](fog-blending.md)
-   [<span data-ttu-id="fc359-110">Couleur de brouillard</span><span class="sxs-lookup"><span data-stu-id="fc359-110">Fog Color</span></span>](fog-color.md)
-   [<span data-ttu-id="fc359-111">Brouillard du vertex</span><span class="sxs-lookup"><span data-stu-id="fc359-111">Vertex Fog</span></span>](vertex-fog.md)
-   [<span data-ttu-id="fc359-112">Brouillard de pixel</span><span class="sxs-lookup"><span data-stu-id="fc359-112">Pixel Fog</span></span>](pixel-fog.md)

<span data-ttu-id="fc359-113">La fusion de brouillard est contrôlée par les États de rendu ; il ne fait pas partie du pipeline de pixels programmable.</span><span class="sxs-lookup"><span data-stu-id="fc359-113">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc359-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc359-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc359-115">Mémoire tampon de trame</span><span class="sxs-lookup"><span data-stu-id="fc359-115">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 



