---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Remplit un tenseur de sortie avec des bits générés de façon déterministe, Pseudo-aléatoire et distribué uniformément. Cet opérateur peut éventuellement également générer un état de générateur interne mis à jour, qui peut être utilisé lors des exécutions ultérieures de l’opérateur.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 19e01ec8dc47e65ace996deef5954c35e21bf5bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106529516"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="9058e-104">Structure DML_RANDOM_GENERATOR_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="9058e-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="9058e-105">Remplit un tenseur de sortie avec des bits générés de façon déterministe, Pseudo-aléatoire et distribué uniformément.</span><span class="sxs-lookup"><span data-stu-id="9058e-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="9058e-106">Cet opérateur peut éventuellement également générer un état de générateur interne mis à jour, qui peut être utilisé lors des exécutions ultérieures de l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="9058e-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="9058e-107">Cet opérateur est déterministe et se comporte comme s’il s’agissait d’une fonction pure &mdash; qui est, son exécution ne produit aucun effet secondaire et n’utilise pas d’état global.</span><span class="sxs-lookup"><span data-stu-id="9058e-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="9058e-108">La sortie Pseudo-aléatoire produite par cet opérateur dépend uniquement des valeurs fournies dans le *InputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="9058e-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="9058e-109">Les générateurs implémentés par cet opérateur ne sont pas sécurisés par chiffrement ; par conséquent, cet opérateur ne doit pas être utilisé pour le chiffrement, la génération de clés ou d’autres applications qui nécessitent une génération de nombres aléatoires sécurisés par chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9058e-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9058e-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="9058e-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="9058e-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9058e-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9058e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9058e-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="9058e-113">Membres</span><span class="sxs-lookup"><span data-stu-id="9058e-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="9058e-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9058e-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9058e-115">Tenseur d’entrée contenant l’état du générateur interne.</span><span class="sxs-lookup"><span data-stu-id="9058e-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="9058e-116">La taille et le format de ce tenseur d’entrée dépend de la [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span><span class="sxs-lookup"><span data-stu-id="9058e-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="9058e-117">Pour **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, ce tenseur doit être de type **UInt32** et avoir des tailles `{1,1,1,6}` .</span><span class="sxs-lookup"><span data-stu-id="9058e-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="9058e-118">Les premières valeurs de 4 32 bits contiennent un compteur de 128 bits qui croît de façon monotone.</span><span class="sxs-lookup"><span data-stu-id="9058e-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="9058e-119">Les dernières valeurs de 2 32 bits contiennent la valeur de clé de 64 bits pour le générateur.</span><span class="sxs-lookup"><span data-stu-id="9058e-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="9058e-120">Lorsque vous initialisez l’état d’entrée du générateur pour la première fois, en général le compteur 128 bits (les premières valeurs UINT32 4 32 bits) doit être initialisé à 0.</span><span class="sxs-lookup"><span data-stu-id="9058e-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="9058e-121">La clé peut être choisie arbitrairement ; des valeurs de clés différentes produiront différentes séquences de nombres.</span><span class="sxs-lookup"><span data-stu-id="9058e-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="9058e-122">La valeur de la clé est généralement générée à l’aide d’une valeur *initiale* fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9058e-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="9058e-123">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9058e-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9058e-124">Tenseur de sortie qui contient les valeurs Pseudo-aléatoires résultantes.</span><span class="sxs-lookup"><span data-stu-id="9058e-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="9058e-125">Ce tenseur peut être de n’importe quelle taille.</span><span class="sxs-lookup"><span data-stu-id="9058e-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="9058e-126">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9058e-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9058e-127">Tenseur de sortie facultatif qui contient l’état de générateur interne mis à jour.</span><span class="sxs-lookup"><span data-stu-id="9058e-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="9058e-128">S’il est fourni, cet opérateur utilise *InputStateTensor* pour calculer un état de générateur mis à jour approprié et écrit le résultat dans le *OutputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="9058e-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="9058e-129">En règle générale, les appelants enregistrent ce résultat et le fournissent comme état d’entrée lors de l’exécution suivante de cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="9058e-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="9058e-130">Type : **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="9058e-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="9058e-131">L’une des valeurs de l’énumération [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , indiquant le type de générateur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9058e-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="9058e-132">Actuellement, la seule valeur valide est **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, qui génère des nombres pseudo-aléatoires en fonction de l' [algorithme 4X32-10 PHILOX](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span><span class="sxs-lookup"><span data-stu-id="9058e-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="9058e-133">Notes</span><span class="sxs-lookup"><span data-stu-id="9058e-133">Remarks</span></span>
<span data-ttu-id="9058e-134">À chaque exécution de cet opérateur, le compteur 128 bits doit être incrémenté.</span><span class="sxs-lookup"><span data-stu-id="9058e-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="9058e-135">Si le *OutputStateTensor* est fourni, cet opérateur incrémente le compteur avec la valeur correcte en votre nom et écrit le résultat dans le *OutputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="9058e-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="9058e-136">La quantité qui doit être incrémentée en fonction du nombre d’éléments de sortie 32 bits générés et du type du générateur.</span><span class="sxs-lookup"><span data-stu-id="9058e-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="9058e-137">Par **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, le compteur 128 bits doit être incrémenté de à `ceil(outputSize / 4)` chaque exécution, où `outputSize` est le nombre d’éléments dans le *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="9058e-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="9058e-138">Prenons un exemple où la valeur du compteur de bits 128 est actuellement `0x48656c6c'6f46726f'6d536561'74746c65` , et la taille de OutputTensor est `{3,3,20,7219}` .</span><span class="sxs-lookup"><span data-stu-id="9058e-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="9058e-139">Après l’exécution de cet opérateur une fois, le compteur doit être incrémenté de 324 855 (le nombre d’éléments de sortie générés divisé par 4, arrondi vers le haut), entraînant une valeur de compteur de `0x48656c6c'6f46726f'6d536561'746f776e` .</span><span class="sxs-lookup"><span data-stu-id="9058e-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="9058e-140">Cette valeur mise à jour doit ensuite être fournie en tant qu’entrée pour la prochaine exécution de cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="9058e-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="9058e-141">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="9058e-141">Availability</span></span>
<span data-ttu-id="9058e-142">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="9058e-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9058e-143">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="9058e-143">Tensor constraints</span></span>
<span data-ttu-id="9058e-144">`InputStateTensor` et `OutputStateTensor` doivent avoir les mêmes *tailles*.</span><span class="sxs-lookup"><span data-stu-id="9058e-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9058e-145">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="9058e-145">Tensor support</span></span>
| <span data-ttu-id="9058e-146">Tenseur</span><span class="sxs-lookup"><span data-stu-id="9058e-146">Tensor</span></span> | <span data-ttu-id="9058e-147">Type</span><span class="sxs-lookup"><span data-stu-id="9058e-147">Kind</span></span> | <span data-ttu-id="9058e-148">Dimensions</span><span class="sxs-lookup"><span data-stu-id="9058e-148">Dimensions</span></span> | <span data-ttu-id="9058e-149">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="9058e-149">Supported dimension counts</span></span> | <span data-ttu-id="9058e-150">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="9058e-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="9058e-151">InputStateTensor</span><span class="sxs-lookup"><span data-stu-id="9058e-151">InputStateTensor</span></span> | <span data-ttu-id="9058e-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="9058e-152">Input</span></span> | <span data-ttu-id="9058e-153">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="9058e-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="9058e-154">4</span><span class="sxs-lookup"><span data-stu-id="9058e-154">4</span></span> | <span data-ttu-id="9058e-155">UINT32</span><span class="sxs-lookup"><span data-stu-id="9058e-155">UINT32</span></span> |
| <span data-ttu-id="9058e-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="9058e-156">OutputTensor</span></span> | <span data-ttu-id="9058e-157">Output</span><span class="sxs-lookup"><span data-stu-id="9058e-157">Output</span></span> | <span data-ttu-id="9058e-158">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="9058e-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="9058e-159">4</span><span class="sxs-lookup"><span data-stu-id="9058e-159">4</span></span> | <span data-ttu-id="9058e-160">UINT32</span><span class="sxs-lookup"><span data-stu-id="9058e-160">UINT32</span></span> |
| <span data-ttu-id="9058e-161">OutputStateTensor</span><span class="sxs-lookup"><span data-stu-id="9058e-161">OutputStateTensor</span></span> | <span data-ttu-id="9058e-162">Sortie facultative</span><span class="sxs-lookup"><span data-stu-id="9058e-162">Optional output</span></span> | <span data-ttu-id="9058e-163">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="9058e-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="9058e-164">4</span><span class="sxs-lookup"><span data-stu-id="9058e-164">4</span></span> | <span data-ttu-id="9058e-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="9058e-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="9058e-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9058e-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9058e-167">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="9058e-167">**Header**</span></span> | <span data-ttu-id="9058e-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="9058e-168">directml.h</span></span> |