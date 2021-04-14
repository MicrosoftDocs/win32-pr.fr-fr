---
title: Découpage (OpenGL)
description: Le découpage se produit en deux étapes
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Pipeline de traitement OpenGL, découpage
- découpage OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383672"
---
# <a name="clipping-opengl"></a><span data-ttu-id="aa62a-105">Découpage (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="aa62a-105">Clipping (OpenGL)</span></span>

<span data-ttu-id="aa62a-106">Le découpage se produit en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="aa62a-106">Clipping occurs in two steps:</span></span>

1.  <span data-ttu-id="aa62a-107">**Affichez le volume clippingApplication de découpage spécifique.**</span><span class="sxs-lookup"><span data-stu-id="aa62a-107">**View volume clippingApplication-specific clipping.**</span></span> <span data-ttu-id="aa62a-108">Immédiatement après l’assemblage des primitives, elles sont découpées en coordonnées oculaires, si nécessaire, pour tous les plans de découpage que vous avez définis avec [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="aa62a-108">Immediately after primitives are assembled, they're clipped in eye coordinates as necessary for any clipping planes you've defined with [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="aa62a-109">(OpenGL requiert la prise en charge d’au moins six plans de découpage spécifiques à l’application.)</span><span class="sxs-lookup"><span data-stu-id="aa62a-109">(OpenGL requires support for at least six such application-specific clipping planes.)</span></span>
2.  <span data-ttu-id="aa62a-110">Les primitives sont transformées par la matrice de projection en coordonnées de clip et découpées par le volume de la vue correspondante.</span><span class="sxs-lookup"><span data-stu-id="aa62a-110">Primitives are transformed by the projection matrix into clip coordinates and clipped by the corresponding view volume.</span></span> <span data-ttu-id="aa62a-111">Cette matrice peut être contrôlée par les fonctions de transformation de matrice (consultez [transformations de matrice](matrix-transformations.md)), mais elle est généralement spécifiée par [**glFrustum**](glfrustum.md) ou [**glOrtho**](glortho.md).</span><span class="sxs-lookup"><span data-stu-id="aa62a-111">This matrix can be controlled by the matrix transformation functions (see [Matrix Transformations](matrix-transformations.md)) but is typically specified by [**glFrustum**](glfrustum.md) or [**glOrtho**](glortho.md).</span></span>

<span data-ttu-id="aa62a-112">Les points, les segments de ligne et les polygones sont gérés différemment lors du découpage :</span><span class="sxs-lookup"><span data-stu-id="aa62a-112">Points, line segments, and polygons are handled differently during clipping:</span></span>

-   <span data-ttu-id="aa62a-113">Les points sont conservés dans leur état d’origine (s’ils sont à l’intérieur du volume du clip) ou ignorés (s’ils sont en dehors du volume du clip).</span><span class="sxs-lookup"><span data-stu-id="aa62a-113">Points are either retained in their original state (if they're inside the clip volume) or discarded (if they're outside the clip volume).</span></span>
-   <span data-ttu-id="aa62a-114">Si des parties de segments de ligne ou de polygones se trouvent en dehors du volume du clip, de nouveaux vertex sont générés au niveau des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="aa62a-114">If portions of line segments or polygons are outside the clip volume, new vertices are generated at the clip points.</span></span>
-   <span data-ttu-id="aa62a-115">Pour les polygones, il peut être nécessaire de construire un bord entier entre les nouveaux vertex générés au niveau des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="aa62a-115">For polygons, an entire edge may need to be constructed between new vertices generated at the clip points.</span></span>
-   <span data-ttu-id="aa62a-116">Pour les segments de ligne et les polygones qui sont découpés, les informations d’indicateur de périphérie, de couleur et de texture sont affectées à tous les nouveaux vertex.</span><span class="sxs-lookup"><span data-stu-id="aa62a-116">For line segments and polygons that are clipped, the edge flag, color, and texture information is assigned to all new vertices.</span></span>

 

 




