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
ms.openlocfilehash: 4d047f7961868de020ac50ffce22b6ce02d078a5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996916"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="b71ee-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="b71ee-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="b71ee-105">Définit la quantité de pavage dans une surface corrective.</span><span class="sxs-lookup"><span data-stu-id="b71ee-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="b71ee-106">Type</span><span class="sxs-lookup"><span data-stu-id="b71ee-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="b71ee-107">Type</span><span class="sxs-lookup"><span data-stu-id="b71ee-107">Type</span></span>       | <span data-ttu-id="b71ee-108">Topologie d’entrée</span><span class="sxs-lookup"><span data-stu-id="b71ee-108">Input Topology</span></span> |
| <span data-ttu-id="b71ee-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b71ee-109">float\[2\]</span></span> | <span data-ttu-id="b71ee-110">correctif Quad</span><span class="sxs-lookup"><span data-stu-id="b71ee-110">quad patch</span></span>     |
| <span data-ttu-id="b71ee-111">float</span><span class="sxs-lookup"><span data-stu-id="b71ee-111">float</span></span>      | <span data-ttu-id="b71ee-112">correctif triple</span><span class="sxs-lookup"><span data-stu-id="b71ee-112">tri patch</span></span>      |
| <span data-ttu-id="b71ee-113">unused</span><span class="sxs-lookup"><span data-stu-id="b71ee-113">unused</span></span>     | <span data-ttu-id="b71ee-114">isoligne</span><span class="sxs-lookup"><span data-stu-id="b71ee-114">isoline</span></span>        |



 

<span data-ttu-id="b71ee-115">Les facteurs de pavage doivent être déclarés en tant que tableau ; ils ne peuvent pas être empaquetés dans un seul vecteur.</span><span class="sxs-lookup"><span data-stu-id="b71ee-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b71ee-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b71ee-116">Remarks</span></span>

<span data-ttu-id="b71ee-117">Cette valeur doit être définie au cours de la fonction de constante de patch du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="b71ee-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="b71ee-118">Valeur de sortie requise pour le nuanceur de coque si vous utilisez des correctifs quad ou tri.</span><span class="sxs-lookup"><span data-stu-id="b71ee-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="b71ee-119">Cette valeur est une entrée requise pour le nuanceur de domaine afin que le matériel corresponde aux signatures via le du paveur.</span><span class="sxs-lookup"><span data-stu-id="b71ee-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="b71ee-120">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b71ee-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b71ee-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="b71ee-121">Vertex</span></span> | <span data-ttu-id="b71ee-122">Forme</span><span class="sxs-lookup"><span data-stu-id="b71ee-122">Hull</span></span> | <span data-ttu-id="b71ee-123">Domain</span><span class="sxs-lookup"><span data-stu-id="b71ee-123">Domain</span></span> | <span data-ttu-id="b71ee-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b71ee-124">Geometry</span></span> | <span data-ttu-id="b71ee-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="b71ee-125">Pixel</span></span> | <span data-ttu-id="b71ee-126">Calcul</span><span class="sxs-lookup"><span data-stu-id="b71ee-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="b71ee-127">x</span><span class="sxs-lookup"><span data-stu-id="b71ee-127">x</span></span>    | <span data-ttu-id="b71ee-128">x</span><span class="sxs-lookup"><span data-stu-id="b71ee-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="b71ee-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b71ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b71ee-130">Sémantique</span><span class="sxs-lookup"><span data-stu-id="b71ee-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="b71ee-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b71ee-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




