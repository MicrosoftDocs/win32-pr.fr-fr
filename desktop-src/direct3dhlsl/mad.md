---
title: mad (fonction)
description: Effectue une opération de multiplication/ajout arithmétique sur trois valeurs.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- fonction Mad (HLSL)
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462590"
---
# <a name="mad-function"></a><span data-ttu-id="720f2-104">mad (fonction)</span><span class="sxs-lookup"><span data-stu-id="720f2-104">mad function</span></span>

<span data-ttu-id="720f2-105">Effectue une opération de multiplication/ajout arithmétique sur trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="720f2-105">Performs an arithmetic multiply/add operation on three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="720f2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="720f2-106">Syntax</span></span>

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a><span data-ttu-id="720f2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="720f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720f2-108">*mvalue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="720f2-108">*mvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="720f2-109">Type : **numérique**</span><span class="sxs-lookup"><span data-stu-id="720f2-109">Type: **numeric**</span></span>

<span data-ttu-id="720f2-110">Valeur de multiplication.</span><span class="sxs-lookup"><span data-stu-id="720f2-110">The multiplication value.</span></span>

</dd> <dt>

<span data-ttu-id="720f2-111">*une valeurqui* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="720f2-111">*avalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="720f2-112">Type : **numérique**</span><span class="sxs-lookup"><span data-stu-id="720f2-112">Type: **numeric**</span></span>

<span data-ttu-id="720f2-113">Première valeur d’addition.</span><span class="sxs-lookup"><span data-stu-id="720f2-113">The first addition value.</span></span>

</dd> <dt>

<span data-ttu-id="720f2-114">*bValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="720f2-114">*bvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="720f2-115">Type : **numérique**</span><span class="sxs-lookup"><span data-stu-id="720f2-115">Type: **numeric**</span></span>

<span data-ttu-id="720f2-116">Deuxième valeur d’addition.</span><span class="sxs-lookup"><span data-stu-id="720f2-116">The second addition value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720f2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="720f2-117">Return value</span></span>

<span data-ttu-id="720f2-118">Type : **numérique**</span><span class="sxs-lookup"><span data-stu-id="720f2-118">Type: **numeric**</span></span>

<span data-ttu-id="720f2-119">Résultat de *mvalue* \* *une valeurqui*  +  *bValue*.</span><span class="sxs-lookup"><span data-stu-id="720f2-119">The result of *mvalue* \* *avalue* + *bvalue*.</span></span>

## <a name="remarks"></a><span data-ttu-id="720f2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="720f2-120">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="720f2-121">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="720f2-121">Minimum Shader Model</span></span>

<span data-ttu-id="720f2-122">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="720f2-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="720f2-123">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="720f2-123">Shader Model</span></span>                                                                | <span data-ttu-id="720f2-124">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="720f2-124">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="720f2-125">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="720f2-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="720f2-126">Oui</span><span class="sxs-lookup"><span data-stu-id="720f2-126">yes</span></span>       |



 

<span data-ttu-id="720f2-127">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="720f2-127">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="720f2-128">Sommet</span><span class="sxs-lookup"><span data-stu-id="720f2-128">Vertex</span></span> | <span data-ttu-id="720f2-129">Forme</span><span class="sxs-lookup"><span data-stu-id="720f2-129">Hull</span></span> | <span data-ttu-id="720f2-130">Domain</span><span class="sxs-lookup"><span data-stu-id="720f2-130">Domain</span></span> | <span data-ttu-id="720f2-131">Géométrie</span><span class="sxs-lookup"><span data-stu-id="720f2-131">Geometry</span></span> | <span data-ttu-id="720f2-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="720f2-132">Pixel</span></span> | <span data-ttu-id="720f2-133">Compute</span><span class="sxs-lookup"><span data-stu-id="720f2-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="720f2-134">x</span><span class="sxs-lookup"><span data-stu-id="720f2-134">x</span></span>      | <span data-ttu-id="720f2-135">x</span><span class="sxs-lookup"><span data-stu-id="720f2-135">x</span></span>    | <span data-ttu-id="720f2-136">x</span><span class="sxs-lookup"><span data-stu-id="720f2-136">x</span></span>      | <span data-ttu-id="720f2-137">x</span><span class="sxs-lookup"><span data-stu-id="720f2-137">x</span></span>        | <span data-ttu-id="720f2-138">x</span><span class="sxs-lookup"><span data-stu-id="720f2-138">x</span></span>     | <span data-ttu-id="720f2-139">x</span><span class="sxs-lookup"><span data-stu-id="720f2-139">x</span></span>       |



 

<span data-ttu-id="720f2-140">Les auteurs de nuanceur peuvent utiliser le intrinsèques **Mad** pour cibler explicitement l’instruction matérielle **Mad** dans la sortie de nuanceur compilé, ce qui est particulièrement utile avec les nuanceurs qui marquent les résultats avec le mot clé [precise](dx-graphics-hlsl-appendix-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="720f2-140">Shader authors can use the **mad** instrinsic to explicitly target the **mad** hardware instruction in the compiled shader output, which is particularly useful with shaders that mark results with the [precise](dx-graphics-hlsl-appendix-keywords.md) keyword.</span></span> <span data-ttu-id="720f2-141">L’instruction **Mad** peut être implémentée dans le matériel en tant que « fusible », ce qui offre une plus grande précision que l’implémentation d’une instruction **mul** suivie d’une instruction **Add** ou d’un ajout de **mul**  +  .</span><span class="sxs-lookup"><span data-stu-id="720f2-141">The **mad** instruction can be implemented in hardware as either "fused," which offers higher precision than implementing a **mul** instruction followed by an **add** instruction, or as a **mul** + **add**.</span></span>

<span data-ttu-id="720f2-142">Si les auteurs de nuanceur utilisent le intrinsèques **Mad** pour calculer un résultat marqué comme précis par le nuanceur, ils indiquent au matériel d’utiliser toute implémentation valide de l’instruction **Mad** (à fusible ou non) tant que l’implémentation est cohérente pour toutes les utilisations de cet intrinsèque **Mad** dans tout nuanceur sur ce matériel.</span><span class="sxs-lookup"><span data-stu-id="720f2-142">If shader authors use the **mad** instrinsic to calculate a result that the shader marked as precise, they indicate to the hardware to use any valid implementation of the **mad** instruction (fused or not) as long as the implementation is consistent for all uses of that **mad** intrinsic in any shader on that hardware.</span></span> <span data-ttu-id="720f2-143">Les nuanceurs peuvent ensuite tirer parti des améliorations potentielles en matière de performances à l’aide d’une instruction **Mad** native (par opposition à l’ajout d' **mul**  +  ) sur un matériel.</span><span class="sxs-lookup"><span data-stu-id="720f2-143">Shaders can then take advantage of potential performance improvements by using a native **mad** instruction (versus **mul** + **add**) on some hardware.</span></span> <span data-ttu-id="720f2-144">Le résultat de l’exécution d’une instruction matérielle **Mad** Native peut être différent de l’exécution d’un **mul** suivi d’un **Ajout**.</span><span class="sxs-lookup"><span data-stu-id="720f2-144">The result of performing a native **mad** hardware instruction might or might not be different than performing a **mul** followed by an **add**.</span></span> <span data-ttu-id="720f2-145">Toutefois, quel que soit le résultat, le résultat doit être cohérent pour que la même opération se produise dans plusieurs nuanceurs ou différentes parties d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="720f2-145">However, whatever the result is, the result must be consistent for the same operation to occur in multiple shaders or different parts of a shader.</span></span>

## <a name="see-also"></a><span data-ttu-id="720f2-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="720f2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="720f2-147">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="720f2-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="720f2-148">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="720f2-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




