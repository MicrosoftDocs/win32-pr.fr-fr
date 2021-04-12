---
description: Une primitive 3D est une collection de vertex qui forment une seule entité 3D. La primitive la plus simple est une collection de points dans un système de coordonnées 3D, appelée liste de points.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitives (graphiques Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108455"
---
# <a name="primitives-direct3d-9-graphics"></a><span data-ttu-id="f8e36-104">Primitives (graphiques Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f8e36-104">Primitives (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="f8e36-105">Une primitive 3D est une collection de vertex qui forment une seule entité 3D.</span><span class="sxs-lookup"><span data-stu-id="f8e36-105">A 3D primitive is a collection of vertices that form a single 3D entity.</span></span> <span data-ttu-id="f8e36-106">La primitive la plus simple est une collection de points dans un système de coordonnées 3D, appelée liste de points.</span><span class="sxs-lookup"><span data-stu-id="f8e36-106">The simplest primitive is a collection of points in a 3D coordinate system, which is called a point list.</span></span>

<span data-ttu-id="f8e36-107">Souvent, les primitives 3D sont des polygones.</span><span class="sxs-lookup"><span data-stu-id="f8e36-107">Often, 3D primitives are polygons.</span></span> <span data-ttu-id="f8e36-108">Un polygone est une figure 3D fermée délimitée par au moins trois vertex.</span><span class="sxs-lookup"><span data-stu-id="f8e36-108">A polygon is a closed 3D figure delineated by at least three vertices.</span></span> <span data-ttu-id="f8e36-109">Le polygone le plus simple est un triangle.</span><span class="sxs-lookup"><span data-stu-id="f8e36-109">The simplest polygon is a triangle.</span></span> <span data-ttu-id="f8e36-110">Microsoft Direct3D utilise des triangles pour composer la plupart de ses polygones, car les trois vertex d’un triangle sont assurés comme étant coplanaires.</span><span class="sxs-lookup"><span data-stu-id="f8e36-110">Microsoft Direct3D uses triangles to compose most of its polygons because all three vertices in a triangle are guaranteed to be coplanar.</span></span> <span data-ttu-id="f8e36-111">Le rendu des vertex non planés est inefficace.</span><span class="sxs-lookup"><span data-stu-id="f8e36-111">Rendering nonplanar vertices is inefficient.</span></span> <span data-ttu-id="f8e36-112">Vous pouvez combiner des triangles pour former des polygones et des maillages de grande taille et complexes.</span><span class="sxs-lookup"><span data-stu-id="f8e36-112">You can combine triangles to form large, complex polygons and meshes.</span></span>

<span data-ttu-id="f8e36-113">L’illustration suivante montre un cube.</span><span class="sxs-lookup"><span data-stu-id="f8e36-113">The following illustration shows a cube.</span></span> <span data-ttu-id="f8e36-114">Deux triangles forment chaque face du cube.</span><span class="sxs-lookup"><span data-stu-id="f8e36-114">Two triangles form each face of the cube.</span></span> <span data-ttu-id="f8e36-115">Le jeu entier de triangles forme une primitive cubique.</span><span class="sxs-lookup"><span data-stu-id="f8e36-115">The entire set of triangles forms one cubic primitive.</span></span> <span data-ttu-id="f8e36-116">Vous pouvez appliquer des textures et des matériaux aux surfaces de primitives pour qu’elles apparaissent comme une forme unie unique.</span><span class="sxs-lookup"><span data-stu-id="f8e36-116">You can apply textures and materials to the surfaces of primitives to make them appear to be a single solid form.</span></span> <span data-ttu-id="f8e36-117">Pour plus d’informations, consultez [Materials (Direct3D 9)](materials.md) et [textures Direct3D (Direct3D 9)](direct3d-textures.md).</span><span class="sxs-lookup"><span data-stu-id="f8e36-117">For details, see [Materials (Direct3D 9)](materials.md) and [Direct3D Textures (Direct3D 9)](direct3d-textures.md).</span></span>

![illustration d’un cube avec deux triangles sur chaque visage](images/cube3d.png)

<span data-ttu-id="f8e36-119">Vous pouvez également utiliser des triangles pour créer des primitives dont les surfaces semblent être des courbes lissées.</span><span class="sxs-lookup"><span data-stu-id="f8e36-119">You can also use triangles to create primitives whose surfaces appear to be smooth curves.</span></span> <span data-ttu-id="f8e36-120">L’illustration suivante montre comment une sphère peut être simulée avec des triangles.</span><span class="sxs-lookup"><span data-stu-id="f8e36-120">The following illustration shows how a sphere can be simulated with triangles.</span></span> <span data-ttu-id="f8e36-121">Une fois qu’un matériau est appliqué, le cercle est courbé lorsqu’il est rendu.</span><span class="sxs-lookup"><span data-stu-id="f8e36-121">After a material is applied, the sphere looks curved when it is rendered.</span></span> <span data-ttu-id="f8e36-122">Cela est particulièrement vrai si vous utilisez l’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="f8e36-122">This is especially true if you use Gouraud shading.</span></span> <span data-ttu-id="f8e36-123">Pour plus d’informations, consultez l' [Ombrage Gouraud](shading-modes.md).</span><span class="sxs-lookup"><span data-stu-id="f8e36-123">For details, see [Gouraud Shading](shading-modes.md).</span></span>

![illustration d’une sphère simulée à l’aide d’un triangle](images/sphere3d.png)

<span data-ttu-id="f8e36-125">Les périphériques Direct3D peuvent créer et manipuler les types de primitives suivants.</span><span class="sxs-lookup"><span data-stu-id="f8e36-125">Direct3D devices can create and manipulate the following types of primitives.</span></span>

-   [<span data-ttu-id="f8e36-126">Listes de points</span><span class="sxs-lookup"><span data-stu-id="f8e36-126">Point Lists</span></span>](point-lists.md)
-   [<span data-ttu-id="f8e36-127">Listes de lignes</span><span class="sxs-lookup"><span data-stu-id="f8e36-127">Line Lists</span></span>](line-lists.md)
-   [<span data-ttu-id="f8e36-128">Bandes</span><span class="sxs-lookup"><span data-stu-id="f8e36-128">Line Strips</span></span>](line-strips.md)
-   [<span data-ttu-id="f8e36-129">Listes de triangles</span><span class="sxs-lookup"><span data-stu-id="f8e36-129">Triangle Lists</span></span>](triangle-lists.md)
-   [<span data-ttu-id="f8e36-130">Bandes triangulaires</span><span class="sxs-lookup"><span data-stu-id="f8e36-130">Triangle Strips</span></span>](triangle-strips.md)
-   [<span data-ttu-id="f8e36-131">Ventilateurs triangulaires (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f8e36-131">Triangle Fans (Direct3D 9)</span></span>](triangle-fans.md)

<span data-ttu-id="f8e36-132">Vous pouvez restituer des types primitifs à partir d’une application C++ avec l’une des méthodes de rendu de l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="f8e36-132">You can render primitive types from a C++ application with any of the rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8e36-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8e36-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e36-134">Périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="f8e36-134">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
