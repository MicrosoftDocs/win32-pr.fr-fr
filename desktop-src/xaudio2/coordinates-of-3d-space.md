---
description: 'La position, la vélocité et l’orientation des sources et écouteurs du son dans l’espace 3D sont représentées par des coordonnées cartésiennes, qui sont des valeurs sur trois axes : l’axe des abscisses, l’axe des y et l’axe des z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordonnées de l’espace 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203631"
---
# <a name="coordinates-of-3d-space"></a><span data-ttu-id="494f8-103">Coordonnées de l’espace 3D</span><span class="sxs-lookup"><span data-stu-id="494f8-103">Coordinates of 3D Space</span></span>

<span data-ttu-id="494f8-104">La position, la vélocité et l’orientation des sources et écouteurs du son dans l’espace 3D sont représentées par des coordonnées cartésiennes, qui sont des valeurs sur trois axes : l’axe des abscisses, l’axe des y et l’axe des z.</span><span class="sxs-lookup"><span data-stu-id="494f8-104">The position, velocity, and orientation of sound sources and listeners in 3D space are represented by Cartesian coordinates, which are values on three axes: the x-axis, the y-axis, and the z-axis.</span></span>

<span data-ttu-id="494f8-105">Les axes sont relatifs à un point de vue établi par l’application.</span><span class="sxs-lookup"><span data-stu-id="494f8-105">The axes are relative to a viewpoint established by the application.</span></span> <span data-ttu-id="494f8-106">Les valeurs sur l’axe des x s’étendent de gauche à droite, sur l’axe des y de bas en haut et sur l’axe z de près à Far.</span><span class="sxs-lookup"><span data-stu-id="494f8-106">Values on the x-axis increase from left to right, on the y-axis from down to up, and on the z-axis from near to far.</span></span>

<span data-ttu-id="494f8-107">La **structure \_ vectorielle X3DAUDIO** contient des valeurs décrivant la position, la vélocité ou l’orientation sur les trois axes.</span><span class="sxs-lookup"><span data-stu-id="494f8-107">The **X3DAUDIO\_VECTOR** structure contains values describing position, velocity, or orientation on the three axes.</span></span>

<span data-ttu-id="494f8-108">D’un point de vue conventionnel, les vecteurs sont exprimés sous la forme de trois valeurs entre parenthèses et séparées par des virgules, dans l’ordre (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="494f8-108">Conventionally, vectors are expressed as three values enclosed in parentheses and separated by commas, in the order (x, y, z).</span></span>

<span data-ttu-id="494f8-109">Pour la position, les valeurs sont en unités universelles définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="494f8-109">For position, the values are in user-defined world units.</span></span>

<span data-ttu-id="494f8-110">Pour la vélocité, le vecteur décrit le taux de mouvement le long de chaque axe en unités universelles par seconde.</span><span class="sxs-lookup"><span data-stu-id="494f8-110">For velocity, the vector describes the rate of movement along each axis in world units per second.</span></span>

<span data-ttu-id="494f8-111">Pour l’orientation, les valeurs sont exprimées en unités arbitraires et sont relatives les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="494f8-111">For orientation, the values are in arbitrary units, and they are relative to one another.</span></span> <span data-ttu-id="494f8-112">Par exemple, si la vue de base du monde 3D est dirigée vers le nord vers l’horizon et que l’orientation de l’écouteur est (-1, 0, 1), l’écouteur est orienté nord-ouest.</span><span class="sxs-lookup"><span data-stu-id="494f8-112">For example, if the base view of the 3D world is facing north toward the horizon, and the orientation of the listener is (-1, 0, 1), then the listener is facing northwest.</span></span> <span data-ttu-id="494f8-113">Étant donné que les valeurs d’un vecteur ne sont pas en unités absolues, le vecteur peut être également exprimé sous la forme (-5, 0, 5) ou (-0,25, 0, 0,25).</span><span class="sxs-lookup"><span data-stu-id="494f8-113">Because the values within a vector are not in absolute units, the vector equally could be expressed as (-5, 0, 5) or (-0.25, 0, 0.25).</span></span>

<span data-ttu-id="494f8-114">les vecteurs 3D fonctionnent de la même façon que les vecteurs 2D, mais avec un axe supplémentaire dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="494f8-114">3D vectors work much like 2D vectors, but with an additional axis in the up-down direction.</span></span> <span data-ttu-id="494f8-115">Vous pouvez voir comment les vecteurs fonctionnent dans l’espace 2D en les dessinant sur une feuille de papier de graphique.</span><span class="sxs-lookup"><span data-stu-id="494f8-115">You can see how vectors work in 2D space by drawing them on a sheet of graph paper.</span></span> <span data-ttu-id="494f8-116">Laissez les valeurs augmenter du bas vers le haut du papier, et de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="494f8-116">Let the values increase from the bottom to the top of the paper, and from left to right.</span></span> <span data-ttu-id="494f8-117">Une ligne dessinée de (0,0) à (1,1) a la même orientation, ou direction, qu’une ligne tirée de (0,0) à (5, 5).</span><span class="sxs-lookup"><span data-stu-id="494f8-117">A line drawn from (0, 0) to (1, 1) has the same orientation, or direction, as one drawn from (0, 0) to (5, 5).</span></span> <span data-ttu-id="494f8-118">Toutefois, la deuxième ligne indique une distance ou une vélocité supérieure.</span><span class="sxs-lookup"><span data-stu-id="494f8-118">However, the second line indicates a greater distance, or velocity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="494f8-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="494f8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="494f8-120">Concepts audio courants</span><span class="sxs-lookup"><span data-stu-id="494f8-120">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="494f8-121">Présentation de X3DAudio</span><span class="sxs-lookup"><span data-stu-id="494f8-121">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> </dl>

 

 



