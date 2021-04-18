---
description: Pendant le rendu, le pipeline interpole les données de vertex sur chaque triangle.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolation de triangle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513300"
---
# <a name="triangle-interpolation-direct3d-9"></a><span data-ttu-id="08980-103">Interpolation de triangle (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="08980-103">Triangle Interpolation (Direct3D 9)</span></span>

<span data-ttu-id="08980-104">Pendant le rendu, le pipeline interpole les données de vertex sur chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="08980-104">During rendering, the pipeline interpolates vertex data across each triangle.</span></span> <span data-ttu-id="08980-105">Les données de vertex peuvent être une grande variété de données et peuvent inclure (sans s’y limiter) : couleur diffuse, couleur spéculaire, alpha diffuse (opacité du triangle), alpha spéculaire et un facteur de brouillard (issu de l’alpha spéculaire pour le pipeline de la fonction fixe et du registre de brouillard pour le pipeline de vertex programmable).</span><span class="sxs-lookup"><span data-stu-id="08980-105">Vertex data can be a broad variety of data and can include (but is not limited to): diffuse color, specular color, diffuse alpha (triangle opacity), specular alpha, and a fog factor (taken from specular alpha for fixed function vertex pipeline and from fog register for programmable vertex pipeline).</span></span> <span data-ttu-id="08980-106">Les données de vertex sont définies par la [déclaration de vertex (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="08980-106">The vertex data is defined by the [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

<span data-ttu-id="08980-107">Pour certaines données de vertex, l’interpolation dépend du mode de trame actuel, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="08980-107">For some vertex data, the interpolation is dependent on the current shading mode, as shown in the following table.</span></span>



| <span data-ttu-id="08980-108">Mode d’ombrage</span><span class="sxs-lookup"><span data-stu-id="08980-108">Shading mode</span></span> | <span data-ttu-id="08980-109">Description</span><span class="sxs-lookup"><span data-stu-id="08980-109">Description</span></span>                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08980-110">À deux dimensions</span><span class="sxs-lookup"><span data-stu-id="08980-110">Flat</span></span>         | <span data-ttu-id="08980-111">Seul le facteur de brouillard est interpolé en mode ombré plat.</span><span class="sxs-lookup"><span data-stu-id="08980-111">Only the fog factor is interpolated in flat shade mode.</span></span> <span data-ttu-id="08980-112">Pour toutes les autres valeurs interpolées, la couleur du premier vertex du triangle est appliquée sur l’ensemble du visage.</span><span class="sxs-lookup"><span data-stu-id="08980-112">For all other interpolated values, the color of the first vertex in the triangle is applied across the entire face.</span></span> |
| <span data-ttu-id="08980-113">Gouraud</span><span class="sxs-lookup"><span data-stu-id="08980-113">Gouraud</span></span>      | <span data-ttu-id="08980-114">L’interpolation linéaire est effectuée entre les trois vertex.</span><span class="sxs-lookup"><span data-stu-id="08980-114">Linear interpolation is performed between all three vertices.</span></span>                                                                                                               |



 

<span data-ttu-id="08980-115">La couleur diffuse et la couleur spéculaire sont traitées différemment, en fonction du modèle de couleurs.</span><span class="sxs-lookup"><span data-stu-id="08980-115">The diffuse color and specular color are treated differently, depending on the color model.</span></span> <span data-ttu-id="08980-116">Dans le modèle de couleurs RVB, le système utilise les composants de couleur rouge, vert et bleu dans l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="08980-116">In the RGB color model, the system uses the red, green, and blue color components in the interpolation.</span></span>

<span data-ttu-id="08980-117">Le composant alpha d’une couleur est traité comme une valeur interpolée distincte, car les pilotes de périphérique peuvent implémenter la transparence de deux manières différentes : à l’aide de la fusion de texture ou à l’aide de stippling.</span><span class="sxs-lookup"><span data-stu-id="08980-117">The alpha component of a color is treated as a separate interpolated value because device drivers can implement transparency in two different ways: by using texture blending or by using stippling.</span></span>

<span data-ttu-id="08980-118">Utilisez le membre ShadeCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour déterminer les formes d’interpolation prises en charge par le pilote de périphérique actuel.</span><span class="sxs-lookup"><span data-stu-id="08980-118">Use the ShadeCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine what forms of interpolation the current device driver supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08980-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08980-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08980-120">Systèmes de coordonnées et géométrie</span><span class="sxs-lookup"><span data-stu-id="08980-120">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



