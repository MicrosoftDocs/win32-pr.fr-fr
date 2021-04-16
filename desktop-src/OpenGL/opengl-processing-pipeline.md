---
title: Pipeline de traitement OpenGL
description: Pipeline de traitement OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline de traitement
- pipeline de traitement OpenGL
- pipeline OpenGL
- framebuffers, pipeline de traitement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104557565"
---
# <a name="opengl-processing-pipeline"></a><span data-ttu-id="64679-107">Pipeline de traitement OpenGL</span><span class="sxs-lookup"><span data-stu-id="64679-107">OpenGL Processing Pipeline</span></span>

<span data-ttu-id="64679-108">De nombreuses fonctions OpenGL sont utilisées spécifiquement pour dessiner des objets tels que des points, des lignes, des polygones et des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="64679-108">Many OpenGL functions are used specifically for drawing objects such as points, lines, polygons, and bitmaps.</span></span> <span data-ttu-id="64679-109">Certaines fonctions contrôlent la façon dont une partie de ce dessin se produit (par exemple, celles qui permettent l’anticrénelage ou la texturation).</span><span class="sxs-lookup"><span data-stu-id="64679-109">Some functions control the way that some of this drawing occurs (such as those that enable antialiasing or texturing).</span></span> <span data-ttu-id="64679-110">D’autres fonctions sont spécifiquement concernées par la manipulation de trame.</span><span class="sxs-lookup"><span data-stu-id="64679-110">Other functions are specifically concerned with framebuffer manipulation.</span></span> <span data-ttu-id="64679-111">Les rubriques de cette section décrivent comment toutes les fonctions OpenGL fonctionnent ensemble pour créer le pipeline de traitement OpenGL.</span><span class="sxs-lookup"><span data-stu-id="64679-111">The topics in this section describe how all of the OpenGL functions work together to create the OpenGL processing pipeline.</span></span> <span data-ttu-id="64679-112">Cette section examine également de plus près les étapes dans lesquelles les données sont réellement traitées et associe ces étapes aux fonctions OpenGL.</span><span class="sxs-lookup"><span data-stu-id="64679-112">This section also takes a closer look at the stages in which data is actually processed, and ties these stages to OpenGL functions.</span></span>

<span data-ttu-id="64679-113">Le diagramme suivant détaille le pipeline de traitement OpenGL.</span><span class="sxs-lookup"><span data-stu-id="64679-113">The following diagram details the OpenGL processing pipeline.</span></span> <span data-ttu-id="64679-114">Pour la plupart du pipeline, vous pouvez voir trois flèches verticales entre les principales étapes.</span><span class="sxs-lookup"><span data-stu-id="64679-114">For most of the pipeline, you can see three vertical arrows between the major stages.</span></span> <span data-ttu-id="64679-115">Ces flèches représentent des vertex et les deux types de données principaux qui peuvent être associés à des vertex : des valeurs de couleur et des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="64679-115">These arrows represent vertices and the two primary types of data that can be associated with vertices: color values and texture coordinates.</span></span> <span data-ttu-id="64679-116">Notez également que les vertex sont assemblés en primitives, puis en fragments et enfin en pixels dans le trame.</span><span class="sxs-lookup"><span data-stu-id="64679-116">Also note that vertices are assembled into primitives, then into fragments, and finally into pixels in the framebuffer.</span></span> <span data-ttu-id="64679-117">Cette progression est traitée plus en détail dans les [vertex](vertices.md), les [primitives](primitives.md), les [fragments](fragments.md)et les [pixels](pixels.md).</span><span class="sxs-lookup"><span data-stu-id="64679-117">This progression is discussed in more detail in [Vertices](vertices.md), [Primitives](primitives.md), [Fragments](fragments.md), and [Pixels](pixels.md).</span></span>

![Diagramme montrant le pipeline de traitement OpenGL.](images/proc01.png)

 

 




