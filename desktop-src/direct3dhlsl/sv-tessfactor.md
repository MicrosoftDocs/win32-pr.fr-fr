---
title: SV_TessFactor
description: Définit la quantité de pavage sur chaque bord d’un correctif.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104971479"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="6752d-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="6752d-104">SV\_TessFactor</span></span>

<span data-ttu-id="6752d-105">Définit la quantité de pavage sur chaque bord d’un correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="6752d-106">Type</span><span class="sxs-lookup"><span data-stu-id="6752d-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="6752d-107">Type</span><span class="sxs-lookup"><span data-stu-id="6752d-107">Type</span></span>       | <span data-ttu-id="6752d-108">Topologie d’entrée</span><span class="sxs-lookup"><span data-stu-id="6752d-108">Input Topology</span></span> |
| <span data-ttu-id="6752d-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="6752d-109">float\[4\]</span></span> | <span data-ttu-id="6752d-110">correctif Quad</span><span class="sxs-lookup"><span data-stu-id="6752d-110">quad patch</span></span>     |
| <span data-ttu-id="6752d-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="6752d-111">float\[3\]</span></span> | <span data-ttu-id="6752d-112">correctif triple</span><span class="sxs-lookup"><span data-stu-id="6752d-112">tri patch</span></span>      |
| <span data-ttu-id="6752d-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="6752d-113">float\[2\]</span></span> | <span data-ttu-id="6752d-114">isoligne</span><span class="sxs-lookup"><span data-stu-id="6752d-114">isoline</span></span>        |



 

<span data-ttu-id="6752d-115">Les facteurs de pavage doivent être déclarés en tant que tableau ; ils ne peuvent pas être empaquetés dans un seul vecteur.</span><span class="sxs-lookup"><span data-stu-id="6752d-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6752d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6752d-116">Remarks</span></span>

<span data-ttu-id="6752d-117">La valeur du facteur de pavage doit être définie au cours de la fonction de constante de patch du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="6752d-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="6752d-118">Valeur de sortie requise pour le nuanceur de coque si vous utilisez des correctifs quad ou tri.</span><span class="sxs-lookup"><span data-stu-id="6752d-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="6752d-119">Cette valeur est également une valeur d’entrée obligatoire pour que le nuanceur de domaine corresponde aux signatures de données à constante de correctif entre les étapes de pavage.</span><span class="sxs-lookup"><span data-stu-id="6752d-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="6752d-120">Pour une isoligne, la première valeur de SV \_ TessFactor est le facteur de pavage de densité de ligne, la deuxième valeur est le facteur de pavage de détail de ligne.</span><span class="sxs-lookup"><span data-stu-id="6752d-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="6752d-121">Facteurs de pavage de correctif tri</span><span class="sxs-lookup"><span data-stu-id="6752d-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="6752d-122">Le premier composant fournit le facteur géométrique pour le bord u = = 0 du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="6752d-123">Le deuxième composant fournit le facteur géométrique pour le bord v = = 0 du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="6752d-124">Le troisième composant fournit le facteur géométrique pour le bord w = = 0 du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="6752d-125">Facteurs de pavage Quad patch</span><span class="sxs-lookup"><span data-stu-id="6752d-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="6752d-126">Le premier composant fournit le facteur géométrique pour le bord u = = 0 du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="6752d-127">Le deuxième composant fournit le facteur géométrique pour le bord v = = 0 du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="6752d-128">Le troisième composant fournit le facteur géométrique pour le bord u = = 1 du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="6752d-129">Le quatrième composant fournit le facteur géométrique pour le bord v = = 1 du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="6752d-130">L’ordre des bords est dans le sens inverse des aiguilles d’une montre, à partir du bord u = = 0, qui est le côté gauche du correctif, et à partir du bord v = = 0, qui est le haut du correctif.</span><span class="sxs-lookup"><span data-stu-id="6752d-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="6752d-131">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="6752d-131">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6752d-132">Sommet</span><span class="sxs-lookup"><span data-stu-id="6752d-132">Vertex</span></span> | <span data-ttu-id="6752d-133">Forme</span><span class="sxs-lookup"><span data-stu-id="6752d-133">Hull</span></span> | <span data-ttu-id="6752d-134">Domain</span><span class="sxs-lookup"><span data-stu-id="6752d-134">Domain</span></span> | <span data-ttu-id="6752d-135">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6752d-135">Geometry</span></span> | <span data-ttu-id="6752d-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="6752d-136">Pixel</span></span> | <span data-ttu-id="6752d-137">Compute</span><span class="sxs-lookup"><span data-stu-id="6752d-137">Compute</span></span> |
|        | <span data-ttu-id="6752d-138">x</span><span class="sxs-lookup"><span data-stu-id="6752d-138">x</span></span>    | <span data-ttu-id="6752d-139">x</span><span class="sxs-lookup"><span data-stu-id="6752d-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="6752d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6752d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6752d-141">Sémantique</span><span class="sxs-lookup"><span data-stu-id="6752d-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="6752d-142">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6752d-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




