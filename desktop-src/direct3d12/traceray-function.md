---
description: Envoie un rayon dans une recherche de correspondances dans une structure d’accélération.
ms.assetid: ''
title: Fonction TraceRay
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106532366"
---
# <a name="traceray-function"></a><span data-ttu-id="3841d-103">Fonction TraceRay</span><span class="sxs-lookup"><span data-stu-id="3841d-103">TraceRay function</span></span>

<span data-ttu-id="3841d-104">Envoie un rayon dans une recherche de correspondances dans une structure d’accélération.</span><span class="sxs-lookup"><span data-stu-id="3841d-104">Sends a ray into a search for hits in an acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3841d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3841d-105">Syntax</span></span>
<span data-ttu-id="3841d-106">Cette définition de fonction intrinsèque est équivalente au modèle de fonction suivant :</span><span class="sxs-lookup"><span data-stu-id="3841d-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a><span data-ttu-id="3841d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3841d-107">Parameters</span></span>

`AccelerationStructure`

<span data-ttu-id="3841d-108">Structure d’accélération de niveau supérieur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3841d-108">The top-level acceleration structure to use.</span></span> <span data-ttu-id="3841d-109">La spécification d’une structure d’accélération NULL force un échec.</span><span class="sxs-lookup"><span data-stu-id="3841d-109">Specifying a NULL acceleration structure forces a miss.</span></span>

`RayFlags`

<span data-ttu-id="3841d-110">Combinaison valide de valeurs de [ray_flag](ray_flag.md) .</span><span class="sxs-lookup"><span data-stu-id="3841d-110">Valid combination of [ray_flag](ray_flag.md) values.</span></span> <span data-ttu-id="3841d-111">Seuls les indicateurs de rayon définis sont propagés par le système, c’est-à-dire qu’ils sont visibles par l’intrinsèque du nuanceur [RayFlags](rayflags.md) .</span><span class="sxs-lookup"><span data-stu-id="3841d-111">Only defined ray flags are propagated by the system, i.e. are visible to the [RayFlags](rayflags.md) shader intrinsic.</span></span>

`InstanceInclusionMask`

<span data-ttu-id="3841d-112">Entier non signé, dont les 8 derniers bits sont utilisés pour inclure ou rejeter des instances geometry en fonction du InstanceMask dans chaque instance.</span><span class="sxs-lookup"><span data-stu-id="3841d-112">An unsigned integer, the bottom 8 bits of which are used to include or reject geometry instances based on the InstanceMask in each instance.</span></span> <span data-ttu-id="3841d-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3841d-113">For example:</span></span>
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

<span data-ttu-id="3841d-114">Entier non signé spécifiant le décalage à ajouter aux calculs d’adressage dans les tables de nuanceur pour l’indexation de groupe d’accès.</span><span class="sxs-lookup"><span data-stu-id="3841d-114">An unsigned integer specifying the offset to add into addressing calculations within shader tables for hit group indexing.</span></span>  <span data-ttu-id="3841d-115">Seuls les 4 derniers bits de cette valeur sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="3841d-115">Only the bottom 4 bits of this value are used.</span></span>

`MultiplierForGeometryContributionToHitGroupIndex`

<span data-ttu-id="3841d-116">Entier non signé spécifiant le STRIDE à multiplier par *GeometryContributionToHitGroupIndex*, qui est simplement l’index de base 0 dans lequel la géométrie a été fournie par l’application dans sa structure d’accélération de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="3841d-116">An unsigned integer specifying the stride to multiply by *GeometryContributionToHitGroupIndex*, which is just the 0 based index the geometry was supplied by the app into its bottom-level acceleration structure.</span></span> <span data-ttu-id="3841d-117">Seuls les 16 bits inférieurs de cette valeur de multiplicateur sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="3841d-117">Only the bottom 16 bits of this multiplier value are used.</span></span>

`MissShaderIndex`

<span data-ttu-id="3841d-118">Entier non signé spécifiant l’index du nuanceur d’absence dans une table de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3841d-118">An unsigned integer specifying the index of the miss shader within a shader table.</span></span>

`Ray`

<span data-ttu-id="3841d-119">[**RayDesc**](raydesc.md) représentant le rayon à tracer.</span><span class="sxs-lookup"><span data-stu-id="3841d-119">A [**RayDesc**](raydesc.md) representing the ray to be traced.</span></span>

`Payload`

<span data-ttu-id="3841d-120">Une charge utile de rayon définie par l’utilisateur, accessible à la fois pour l’entrée et la sortie par les nuanceurs appelés pendant Raytracing.</span><span class="sxs-lookup"><span data-stu-id="3841d-120">A user defined ray payload accessed both for both input and output by shaders invoked during raytracing.</span></span>  <span data-ttu-id="3841d-121">Une fois [**TraceRay**](traceray-function.md) terminé, l’appelant peut également accéder à la charge utile.</span><span class="sxs-lookup"><span data-stu-id="3841d-121">After [**TraceRay**](traceray-function.md) completes, the caller can access the payload as well.</span></span>

## <a name="return-value"></a><span data-ttu-id="3841d-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3841d-122">Return Value</span></span>

<span data-ttu-id="3841d-123">**void**</span><span class="sxs-lookup"><span data-stu-id="3841d-123">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="3841d-124">Notes</span><span class="sxs-lookup"><span data-stu-id="3841d-124">Remarks</span></span>

<span data-ttu-id="3841d-125">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="3841d-125">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="3841d-126">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="3841d-126">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="3841d-127">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="3841d-127">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="3841d-128">**Nuanceur de création de rayon**</span><span class="sxs-lookup"><span data-stu-id="3841d-128">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="3841d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3841d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3841d-130">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="3841d-130">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




