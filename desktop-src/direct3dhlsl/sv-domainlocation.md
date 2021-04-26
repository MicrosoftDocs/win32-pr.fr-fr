---
title: SV_DomainLocation
description: Définit l’emplacement sur la coque du point de domaine actuel en cours d’évaluation.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb9265734663881981f1626db6e23c6b7dd9415a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996506"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="59d41-104">SV \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="59d41-104">SV\_DomainLocation</span></span>

<span data-ttu-id="59d41-105">Définit l’emplacement sur la coque du point de domaine actuel en cours d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="59d41-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="59d41-106">Type</span><span class="sxs-lookup"><span data-stu-id="59d41-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="59d41-107">Type</span><span class="sxs-lookup"><span data-stu-id="59d41-107">Type</span></span>   | <span data-ttu-id="59d41-108">Topologie d’entrée</span><span class="sxs-lookup"><span data-stu-id="59d41-108">Input Topology</span></span> |
| <span data-ttu-id="59d41-109">float2</span><span class="sxs-lookup"><span data-stu-id="59d41-109">float2</span></span> | <span data-ttu-id="59d41-110">correctif Quad</span><span class="sxs-lookup"><span data-stu-id="59d41-110">quad patch</span></span>     |
| <span data-ttu-id="59d41-111">float3</span><span class="sxs-lookup"><span data-stu-id="59d41-111">float3</span></span> | <span data-ttu-id="59d41-112">correctif triple</span><span class="sxs-lookup"><span data-stu-id="59d41-112">tri patch</span></span>      |
| <span data-ttu-id="59d41-113">float2</span><span class="sxs-lookup"><span data-stu-id="59d41-113">float2</span></span> | <span data-ttu-id="59d41-114">isoligne</span><span class="sxs-lookup"><span data-stu-id="59d41-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="59d41-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="59d41-115">Remarks</span></span>

<span data-ttu-id="59d41-116">Cette valeur système est requise.</span><span class="sxs-lookup"><span data-stu-id="59d41-116">This system value is required.</span></span>

<span data-ttu-id="59d41-117">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="59d41-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="59d41-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="59d41-118">Vertex</span></span> | <span data-ttu-id="59d41-119">Forme</span><span class="sxs-lookup"><span data-stu-id="59d41-119">Hull</span></span> | <span data-ttu-id="59d41-120">Domain</span><span class="sxs-lookup"><span data-stu-id="59d41-120">Domain</span></span> | <span data-ttu-id="59d41-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="59d41-121">Geometry</span></span> | <span data-ttu-id="59d41-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="59d41-122">Pixel</span></span> | <span data-ttu-id="59d41-123">Calcul</span><span class="sxs-lookup"><span data-stu-id="59d41-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="59d41-124">x</span><span class="sxs-lookup"><span data-stu-id="59d41-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="59d41-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59d41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d41-126">Sémantique</span><span class="sxs-lookup"><span data-stu-id="59d41-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="59d41-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="59d41-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




