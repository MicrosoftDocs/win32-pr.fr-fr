---
description: La fusion de vertex indexée étend la prise en charge de la fusion de vertex dans Direct3D pour permettre l’utilisation de matrices pour la fusion.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Fusion de vertex indexée (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480713"
---
# <a name="indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="0bdd5-103">Fusion de vertex indexée (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0bdd5-103">Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="0bdd5-104">La fusion de vertex indexée étend la prise en charge de la fusion de vertex dans Direct3D pour permettre l’utilisation de matrices pour la fusion.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-104">Indexed vertex blending extends the vertex blending support in Direct3D to allow matrices to be used for blending.</span></span> <span data-ttu-id="0bdd5-105">Ces matrices sont référencées à l’aide d’un index de matrice.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-105">These matrices are referred to by using a matrix index.</span></span> <span data-ttu-id="0bdd5-106">Ces index sont fournis sur la base de chaque vertex et font référence à une palette allant jusqu’à 256 matrices.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-106">These indices are supplied on a per-vertex basis and refer to a palette of up to 256 matrices.</span></span> <span data-ttu-id="0bdd5-107">Chaque index est constitué de 8 bits et chaque vertex peut avoir jusqu’à quatre index, ce qui permet de mélanger quatre matrices par vertex.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-107">Each index is 8 bits and each vertex can have up to four indices, which allows four matrices to be blended per vertex.</span></span> <span data-ttu-id="0bdd5-108">Les index sont empaquetés dans un DWORD.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-108">The indices are packed into a DWORD.</span></span> <span data-ttu-id="0bdd5-109">Étant donné que les index sont spécifiés sur une base par vertex, jusqu’à 12 matrices peuvent affecter un seul triangle, et toute matrice de la palette peut affecter les vertex d’un appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-109">Because indices are specified on a per-vertex basis, up to 12 matrices can affect a single triangle, and any matrix in the palette can affect the vertices of one draw call.</span></span> <span data-ttu-id="0bdd5-110">Cette approche présente les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="0bdd5-110">This approach has the following advantages.</span></span>

-   <span data-ttu-id="0bdd5-111">Il permet à plus de matrices d’affecter un seul triangle.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-111">It enables more matrices to affect a single triangle.</span></span>
-   <span data-ttu-id="0bdd5-112">Il permet à d’autres triangles mélangés d’être passés dans le même appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-112">It enables more blended triangles to be passed in the same draw call.</span></span>
-   <span data-ttu-id="0bdd5-113">Il rend la fusion de vertex indépendante des indices de triangle.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-113">It makes vertex blending independent of triangle indices.</span></span> <span data-ttu-id="0bdd5-114">Cela permet aux maillages progressifs de fonctionner conjointement avec la fusion de vertex.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-114">This enables progressive meshes to work in conjunction with vertex blending.</span></span>

<span data-ttu-id="0bdd5-115">L’un des inconvénients de cette approche est qu’elle ne fonctionne pas avec les primitives de surface courbée quand le pavage se produit avant le traitement du vertex.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-115">One disadvantage of this approach is that it does not work with curved-surface primitives when tessellation occurs before vertex processing.</span></span>

<span data-ttu-id="0bdd5-116">Le diagramme suivant montre comment quatre matrices peuvent affecter un vertex.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-116">The following diagram demonstrates how four matrices can affect a vertex.</span></span> <span data-ttu-id="0bdd5-117">Chaque vertex compte jusqu’à quatre index, quatre matrices peuvent donc être mélangées par vertex.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-117">Each vertex has up to four indices, so four matrices can be blended per vertex.</span></span> <span data-ttu-id="0bdd5-118">Le diagramme utilise les matrices indexées à 0, 2, 5 et 6.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-118">The diagram uses the matrices indexed at 0, 2, 5, and 6.</span></span>

![diagramme de la fusion des vertex indexés à l’aide de 4 matrices disponibles de 256](images/dword1.png)

<span data-ttu-id="0bdd5-120">Le diagramme suivant montre comment 12 matrices au maximum peuvent affecter un triangle.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-120">The following diagram demonstrates how up to 12 matrices can affect a triangle.</span></span> <span data-ttu-id="0bdd5-121">L’utilisation des index spécifiés sur une base par vertex, jusqu’à 12 matrices peut affecter le triangle.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-121">Using indices specified on a per-vertex basis, up to 12 matrices can affect the triangle.</span></span>

![diagramme de la fusion des vertex indexés pour un triangle à l’aide de 12 matrices disponibles de 12 256](images/dword2.png)

<span data-ttu-id="0bdd5-123">L’équation suivante détermine le cas général de l’effet des matrices sur un sommet.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-123">The following equation determines the general case for how matrices effect a vertex.</span></span>

![équation de la fusion des vertex indexés](images/indexedvblend.png)

<span data-ttu-id="0bdd5-125">Le <sub>modèle</sub> V est la position du vertex de l’espace du modèle d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-125">V <sub>model</sub> is the input model space vertex position.</span></span> <span data-ttu-id="0bdd5-126">Index0.. Index3 sont les index de matrice par vertex compressés dans une valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-126">Index0..Index3 are the per-vertex matrix indices packed into a DWORD.</span></span> <span data-ttu-id="0bdd5-127">M \[ \] est le tableau de matrices universelles qui sont indexées dans.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-127">M\[\] is the array of world matrices that get indexed into.</span></span> <span data-ttu-id="0bdd5-128">b ₀.. b ₂ sont les pondérations de fusion.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-128">b₀..b₂ are the blend weights.</span></span> <span data-ttu-id="0bdd5-129">Le<sub>monde</sub> V est la position du sommet de l’espace universel de sortie.</span><span class="sxs-lookup"><span data-stu-id="0bdd5-129">V<sub>world</sub> is the output world space vertex position.</span></span>

<span data-ttu-id="0bdd5-130">Pour plus d’informations sur la fusion des vertex indexés, consultez Utilisation de la [fusion de vertex indexée (Direct3D 9)](using-indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="0bdd5-130">For more information about indexed vertex blending, see [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bdd5-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0bdd5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bdd5-132">Fusion géométrique</span><span class="sxs-lookup"><span data-stu-id="0bdd5-132">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



