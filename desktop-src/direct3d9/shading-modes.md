---
description: Le mode d’ombrage utilisé pour afficher un polygone a un effet profond sur son apparence. Les modes d’ombrage déterminent l’intensité de la couleur et de l’éclairage à n’importe quel point d’une face de polygone. Direct3D prend en charge deux modes d’ombrage.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modes d’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567164"
---
# <a name="shading-modes-direct3d-9"></a><span data-ttu-id="3c737-105">Modes d’ombrage (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3c737-105">Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="3c737-106">Le mode d’ombrage utilisé pour afficher un polygone a un effet profond sur son apparence.</span><span class="sxs-lookup"><span data-stu-id="3c737-106">The shading mode used to render a polygon has a profound effect on its appearance.</span></span> <span data-ttu-id="3c737-107">Les modes d’ombrage déterminent l’intensité de la couleur et de l’éclairage à n’importe quel point d’une face de polygone.</span><span class="sxs-lookup"><span data-stu-id="3c737-107">Shading modes determine the intensity of color and lighting at any point on a polygon face.</span></span> <span data-ttu-id="3c737-108">Direct3D prend en charge deux modes d’ombrage.</span><span class="sxs-lookup"><span data-stu-id="3c737-108">Direct3D supports two shading modes.</span></span>

-   [<span data-ttu-id="3c737-109">Ombrage plat</span><span class="sxs-lookup"><span data-stu-id="3c737-109">Flat Shading</span></span>](#flat-shading)
-   [<span data-ttu-id="3c737-110">Ombrage Gouraud</span><span class="sxs-lookup"><span data-stu-id="3c737-110">Gouraud Shading</span></span>](#gouraud-shading)

## <a name="flat-shading"></a><span data-ttu-id="3c737-111">Ombrage plat</span><span class="sxs-lookup"><span data-stu-id="3c737-111">Flat Shading</span></span>

<span data-ttu-id="3c737-112">Dans le mode d’ombrage plat, le pipeline de rendu Direct3D affiche un polygone, en utilisant la couleur du matériau polygonal à son premier vertex comme couleur de l’ensemble du polygone.</span><span class="sxs-lookup"><span data-stu-id="3c737-112">In the flat shading mode, the Direct3D rendering pipeline renders a polygon, using the color of the polygon material at its first vertex as the color for the entire polygon.</span></span> <span data-ttu-id="3c737-113">les objets 3D qui sont rendus avec un ombrage plat ont des bords nets visibles entre les polygones s’ils ne sont pas coplanés.</span><span class="sxs-lookup"><span data-stu-id="3c737-113">3D objects that are rendered with flat shading have visibly sharp edges between polygons if they are not coplanar.</span></span>

<span data-ttu-id="3c737-114">L’illustration suivante montre un rendu de théière avec un ombrage plat.</span><span class="sxs-lookup"><span data-stu-id="3c737-114">The following illustration shows a teapot rendered with flat shading.</span></span> <span data-ttu-id="3c737-115">Le contour de chaque polygone est clairement visible.</span><span class="sxs-lookup"><span data-stu-id="3c737-115">The outline of each polygon is clearly visible.</span></span> <span data-ttu-id="3c737-116">L’ombrage plat est la forme la plus rapide de l’ombrage.</span><span class="sxs-lookup"><span data-stu-id="3c737-116">Flat shading is the fastest form of shading.</span></span>

![illustration d’un théière à l’aide d’un ombrage plat](images/flattea.png)

## <a name="gouraud-shading"></a><span data-ttu-id="3c737-118">Ombrage Gouraud</span><span class="sxs-lookup"><span data-stu-id="3c737-118">Gouraud Shading</span></span>

<span data-ttu-id="3c737-119">Lorsque Direct3D effectue le rendu d’un polygone à l’aide de l’ombrage Gouraud, il calcule une couleur pour chaque vertex à l’aide des paramètres de normalisation et d’éclairage des vertex.</span><span class="sxs-lookup"><span data-stu-id="3c737-119">When Direct3D renders a polygon using Gouraud shading, it computes a color for each vertex by using the vertex normal and lighting parameters.</span></span> <span data-ttu-id="3c737-120">Ensuite, il interpole la couleur sur la face des polygones. l’interpolation est effectuée de façon linéaire.</span><span class="sxs-lookup"><span data-stu-id="3c737-120">Then, it interpolates the color across the face of the polygons The interpolation is done linearly.</span></span> <span data-ttu-id="3c737-121">Par exemple, si le composant rouge de la couleur du vertex 1 est 0,8 et que le composant rouge du Vertex 2 est 0,4, à l’aide du mode d’ombrage Gouraud et du modèle de couleurs RVB, le module d’éclairage Direct3D affecte un composant rouge de 0,6 au pixel situé au milieu de la ligne entre ces sommets.</span><span class="sxs-lookup"><span data-stu-id="3c737-121">For example, if the red component of the color of vertex 1 is 0.8 and the red component of vertex 2 is 0.4, using the Gouraud shading mode and the RGB color model, the Direct3D lighting module assigns a red component of 0.6 to the pixel at the midpoint of the line between these vertices.</span></span>

<span data-ttu-id="3c737-122">L’illustration suivante montre l’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="3c737-122">The following illustration demonstrates Gouraud shading.</span></span> <span data-ttu-id="3c737-123">Ce théière est composé de nombreux polygones plats et triangulaires.</span><span class="sxs-lookup"><span data-stu-id="3c737-123">This teapot is composed of many flat, triangular polygons.</span></span> <span data-ttu-id="3c737-124">Toutefois, l’ombrage Gouraud rend l’affichage courbé et lisse de la surface de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3c737-124">However, Gouraud shading makes the surface of the object appear curved and smooth.</span></span>

![illustration de théière à l’aide de l’ombrage Gouraud](images/gourtea.png)

<span data-ttu-id="3c737-126">L’ombrage Gouraud peut également être utilisé pour afficher des objets avec des bords tranchants.</span><span class="sxs-lookup"><span data-stu-id="3c737-126">Gouraud shading can also be used to display objects with sharp edges.</span></span>

<span data-ttu-id="3c737-127">Pour plus d’informations, consultez [vecteurs normaux de face et vertex (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="3c737-127">For more information, see [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c737-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c737-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c737-129">Ombrage</span><span class="sxs-lookup"><span data-stu-id="3c737-129">Shading</span></span>](shading.md)
</dt> </dl>

 

 



