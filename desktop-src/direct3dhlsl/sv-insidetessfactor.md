---
title: SV_InsideTessFactor
description: Définit la quantité de pavage dans une surface corrective.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104971478"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="52a50-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="52a50-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="52a50-105">Définit la quantité de pavage dans une surface corrective.</span><span class="sxs-lookup"><span data-stu-id="52a50-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="52a50-106">Type</span><span class="sxs-lookup"><span data-stu-id="52a50-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="52a50-107">Type</span><span class="sxs-lookup"><span data-stu-id="52a50-107">Type</span></span>       | <span data-ttu-id="52a50-108">Topologie d’entrée</span><span class="sxs-lookup"><span data-stu-id="52a50-108">Input Topology</span></span> |
| <span data-ttu-id="52a50-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="52a50-109">float\[2\]</span></span> | <span data-ttu-id="52a50-110">correctif Quad</span><span class="sxs-lookup"><span data-stu-id="52a50-110">quad patch</span></span>     |
| <span data-ttu-id="52a50-111">float</span><span class="sxs-lookup"><span data-stu-id="52a50-111">float</span></span>      | <span data-ttu-id="52a50-112">correctif triple</span><span class="sxs-lookup"><span data-stu-id="52a50-112">tri patch</span></span>      |
| <span data-ttu-id="52a50-113">unused</span><span class="sxs-lookup"><span data-stu-id="52a50-113">unused</span></span>     | <span data-ttu-id="52a50-114">isoligne</span><span class="sxs-lookup"><span data-stu-id="52a50-114">isoline</span></span>        |



 

<span data-ttu-id="52a50-115">Les facteurs de pavage doivent être déclarés en tant que tableau ; ils ne peuvent pas être empaquetés dans un seul vecteur.</span><span class="sxs-lookup"><span data-stu-id="52a50-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="52a50-116">Notes</span><span class="sxs-lookup"><span data-stu-id="52a50-116">Remarks</span></span>

<span data-ttu-id="52a50-117">Cette valeur doit être définie au cours de la fonction de constante de patch du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="52a50-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="52a50-118">Valeur de sortie requise pour le nuanceur de coque si vous utilisez des correctifs quad ou tri.</span><span class="sxs-lookup"><span data-stu-id="52a50-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="52a50-119">Cette valeur est une entrée requise pour le nuanceur de domaine afin que le matériel corresponde aux signatures via le du paveur.</span><span class="sxs-lookup"><span data-stu-id="52a50-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="52a50-120">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="52a50-120">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="52a50-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="52a50-121">Vertex</span></span> | <span data-ttu-id="52a50-122">Forme</span><span class="sxs-lookup"><span data-stu-id="52a50-122">Hull</span></span> | <span data-ttu-id="52a50-123">Domain</span><span class="sxs-lookup"><span data-stu-id="52a50-123">Domain</span></span> | <span data-ttu-id="52a50-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="52a50-124">Geometry</span></span> | <span data-ttu-id="52a50-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="52a50-125">Pixel</span></span> | <span data-ttu-id="52a50-126">Compute</span><span class="sxs-lookup"><span data-stu-id="52a50-126">Compute</span></span> |
|        | <span data-ttu-id="52a50-127">x</span><span class="sxs-lookup"><span data-stu-id="52a50-127">x</span></span>    | <span data-ttu-id="52a50-128">x</span><span class="sxs-lookup"><span data-stu-id="52a50-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="52a50-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52a50-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a50-130">Sémantique</span><span class="sxs-lookup"><span data-stu-id="52a50-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="52a50-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="52a50-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




