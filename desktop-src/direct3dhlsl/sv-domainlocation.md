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
ms.openlocfilehash: 3c5195881df438c94cdaed7de8484d0df65e4d54
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380969"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="04165-104">SV \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="04165-104">SV\_DomainLocation</span></span>

<span data-ttu-id="04165-105">Définit l’emplacement sur la coque du point de domaine actuel en cours d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="04165-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="04165-106">Type</span><span class="sxs-lookup"><span data-stu-id="04165-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="04165-107">Type</span><span class="sxs-lookup"><span data-stu-id="04165-107">Type</span></span>   | <span data-ttu-id="04165-108">Topologie d’entrée</span><span class="sxs-lookup"><span data-stu-id="04165-108">Input Topology</span></span> |
| <span data-ttu-id="04165-109">float2</span><span class="sxs-lookup"><span data-stu-id="04165-109">float2</span></span> | <span data-ttu-id="04165-110">correctif Quad</span><span class="sxs-lookup"><span data-stu-id="04165-110">quad patch</span></span>     |
| <span data-ttu-id="04165-111">float3</span><span class="sxs-lookup"><span data-stu-id="04165-111">float3</span></span> | <span data-ttu-id="04165-112">correctif triple</span><span class="sxs-lookup"><span data-stu-id="04165-112">tri patch</span></span>      |
| <span data-ttu-id="04165-113">float2</span><span class="sxs-lookup"><span data-stu-id="04165-113">float2</span></span> | <span data-ttu-id="04165-114">isoligne</span><span class="sxs-lookup"><span data-stu-id="04165-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="04165-115">Notes</span><span class="sxs-lookup"><span data-stu-id="04165-115">Remarks</span></span>

<span data-ttu-id="04165-116">Cette valeur système est requise.</span><span class="sxs-lookup"><span data-stu-id="04165-116">This system value is required.</span></span>

<span data-ttu-id="04165-117">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="04165-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="04165-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="04165-118">Vertex</span></span> | <span data-ttu-id="04165-119">Forme</span><span class="sxs-lookup"><span data-stu-id="04165-119">Hull</span></span> | <span data-ttu-id="04165-120">Domain</span><span class="sxs-lookup"><span data-stu-id="04165-120">Domain</span></span> | <span data-ttu-id="04165-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="04165-121">Geometry</span></span> | <span data-ttu-id="04165-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="04165-122">Pixel</span></span> | <span data-ttu-id="04165-123">Compute</span><span class="sxs-lookup"><span data-stu-id="04165-123">Compute</span></span> |
|        |      | <span data-ttu-id="04165-124">x</span><span class="sxs-lookup"><span data-stu-id="04165-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="04165-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04165-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04165-126">Sémantique</span><span class="sxs-lookup"><span data-stu-id="04165-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="04165-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="04165-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




