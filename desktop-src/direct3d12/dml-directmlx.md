---
title: DirectMLX
description: DirectMLX est une bibliothèque d’assistance en-tête C++ uniquement pour DirectML, conçue pour faciliter la composition d’opérateurs individuels en graphiques.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 8388edd51b6ad3ca30fe1c65947167cee7dac5e6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548623"
---
# <a name="directmlx"></a><span data-ttu-id="f14cb-103">DirectMLX</span><span class="sxs-lookup"><span data-stu-id="f14cb-103">DirectMLX</span></span>

<span data-ttu-id="f14cb-104">DirectMLX est une bibliothèque d’assistance en-tête C++ uniquement pour DirectML, conçue pour faciliter la composition d’opérateurs individuels en graphiques.</span><span class="sxs-lookup"><span data-stu-id="f14cb-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="f14cb-105">DirectMLX fournit des wrappers pratiques pour tous les types d’opérateur DirectML (DML), ainsi que des surcharges d’opérateur intuitives, ce qui simplifie l’instanciation des opérateurs DML et leur chaînage en graphiques complexes.</span><span class="sxs-lookup"><span data-stu-id="f14cb-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="f14cb-106">Emplacement de recherche `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="f14cb-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="f14cb-107">`DirectMLX.h` est distribué en tant que logiciel open source dans le cadre de la licence MIT.</span><span class="sxs-lookup"><span data-stu-id="f14cb-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="f14cb-108">La dernière version se trouve sur le [GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Libraries).</span><span class="sxs-lookup"><span data-stu-id="f14cb-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f14cb-109">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="f14cb-109">Tensor constraints</span></span>

<span data-ttu-id="f14cb-110">DirectMLX requiert DirectML version 1.4.0 ou ultérieure (voir [l’historique des versions DirectML](dml-version-history.md#version-table)).</span><span class="sxs-lookup"><span data-stu-id="f14cb-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="f14cb-111">Les versions antérieures de DirectML ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f14cb-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="f14cb-112">DirectMLX. h requiert un compilateur C + 11, y compris (mais sans s’y limiter) :</span><span class="sxs-lookup"><span data-stu-id="f14cb-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="f14cb-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="f14cb-113">Visual Studio 2017</span></span>
* <span data-ttu-id="f14cb-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="f14cb-114">Visual Studio 2019</span></span>
* <span data-ttu-id="f14cb-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="f14cb-115">Clang 10</span></span>

<span data-ttu-id="f14cb-116">Notez qu’un compilateur C++ 17 (ou plus récent) est une option que nous recommandons.</span><span class="sxs-lookup"><span data-stu-id="f14cb-116">Note that a C++17 (or newer) compiler is options that we recommend.</span></span> <span data-ttu-id="f14cb-117">La compilation pour C++ 11 est possible, mais elle nécessite l’utilisation de bibliothèques tierces (telles que [GSL](https://github.com/microsoft/GSL) et [abseil](https://github.com/abseil/abseil-cpp)) pour remplacer les fonctionnalités de la bibliothèque standard manquantes.</span><span class="sxs-lookup"><span data-stu-id="f14cb-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="f14cb-118">Si vous avez une configuration dont la compilation échoue `DirectMLX.h` , veuillez [Envoyer un problème sur notre GitHub](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="f14cb-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="f14cb-119">Utilisation de base</span><span class="sxs-lookup"><span data-stu-id="f14cb-119">Basic Usage</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Scope scope(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

<span data-ttu-id="f14cb-120">Voici un autre exemple, qui crée un graphique DirectML pouvant calculer la [formule quadratique](https://en.wikipedia.org/wiki/Quadratic_formula).</span><span class="sxs-lookup"><span data-stu-id="f14cb-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

std::pair<dml::Expression, dml::Expression>
    QuadraticFormula(dml::Expression a, dml::Expression b, dml::Expression c)
{
    // Quadratic formula: given an equation of the form ax^2 + bx + c = 0, x can be found by:
    //   x = -b +/- sqrt(b^2 - 4ac) / (2a)
    // https://en.wikipedia.org/wiki/Quadratic_formula

    // Note: DirectMLX provides operator overloads for common mathematical expressions. So for 
    // example a*c is equivalent to dml::Multiply(a, c).
    auto x1 = -b + dml::Sqrt(b*b - 4*a*c) / (2*a);
    auto x2 = -b - dml::Sqrt(b*b - 4*a*c) / (2*a);

    return { x1, x2 };
}

/* ... */

dml::Scope scope(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(scope, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(scope, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a><span data-ttu-id="f14cb-121">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="f14cb-121">More examples</span></span>

<span data-ttu-id="f14cb-122">Vous trouverez des exemples complets à l’aide de DirectMLX sur le [référentiel GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Samples).</span><span class="sxs-lookup"><span data-stu-id="f14cb-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="f14cb-123">Options de Compile-Time</span><span class="sxs-lookup"><span data-stu-id="f14cb-123">Compile-Time Options</span></span>

<span data-ttu-id="f14cb-124">DirectMLX prend en charge les #define de compilation pour personnaliser différentes parties de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f14cb-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="f14cb-125">Option</span><span class="sxs-lookup"><span data-stu-id="f14cb-125">Option</span></span>|<span data-ttu-id="f14cb-126">Description</span><span class="sxs-lookup"><span data-stu-id="f14cb-126">Description</span></span>|
|-|-|
|<span data-ttu-id="f14cb-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="f14cb-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="f14cb-128">Si #define, provoque l’appel d’erreurs `std::abort` plutôt que la levée d’une exception.</span><span class="sxs-lookup"><span data-stu-id="f14cb-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="f14cb-129">Cette valeur est définie par défaut si les exceptions ne sont pas disponibles (par exemple, si les exceptions ont été désactivées dans les options du compilateur).</span><span class="sxs-lookup"><span data-stu-id="f14cb-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="f14cb-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="f14cb-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="f14cb-131">Si #define, les exceptions sont levées à l’aide des types d’exception de la [bibliothèque d’implémentation Windows](https://github.com/microsoft/wil) .</span><span class="sxs-lookup"><span data-stu-id="f14cb-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="f14cb-132">Sinon, les types d’exceptions standard (tels que `std::runtime_error` ) sont utilisés à la place.</span><span class="sxs-lookup"><span data-stu-id="f14cb-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="f14cb-133">Cette option n’a aucun effet si **DMLX_NO_EXCEPTIONS** est défini.</span><span class="sxs-lookup"><span data-stu-id="f14cb-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="f14cb-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="f14cb-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="f14cb-135">Si #define, utilise [abseil](https://github.com/abseil/abseil-cpp) comme remplacements de suppression pour les types de bibliothèque standard non disponibles en c++ 11.</span><span class="sxs-lookup"><span data-stu-id="f14cb-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="f14cb-136">Ces types incluent `absl::optional` (à la place de `std::optional` ), `absl::Span` (à la place de `std::span` ) et `absl::InlinedVector` .</span><span class="sxs-lookup"><span data-stu-id="f14cb-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="f14cb-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="f14cb-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="f14cb-138">Détermine s’il faut utiliser [GSL](https://github.com/microsoft/GSL) comme remplacement de `std::span` .</span><span class="sxs-lookup"><span data-stu-id="f14cb-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="f14cb-139">Si #define, les utilisations de `std::span` sont remplacées par `gsl::span` sur les compilateurs sans `std::span` implémentation native.</span><span class="sxs-lookup"><span data-stu-id="f14cb-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="f14cb-140">Dans le cas contraire, une implémentation de dépôt Inline est fournie à la place.</span><span class="sxs-lookup"><span data-stu-id="f14cb-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="f14cb-141">Notez que cette option est utilisée uniquement lors de la compilation sur un compilateur pré-C + + 20 sans prise en charge de `std::span` , et lorsqu’aucun autre remplacement de bibliothèque standard (comme abseil) n’est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f14cb-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="f14cb-142">Contrôle de la disposition tenseur</span><span class="sxs-lookup"><span data-stu-id="f14cb-142">Controlling Tensor Layout</span></span>

<span data-ttu-id="f14cb-143">Pour la plupart des opérateurs, DirectMLX calcule les propriétés des dizaines de sortie de l’opérateur en votre nom.</span><span class="sxs-lookup"><span data-stu-id="f14cb-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="f14cb-144">Par exemple, lorsque vous effectuez une opération `dml::Reduce` sur plusieurs axes `{ 0, 2, 3 }` avec un tenseur d’entrée de tailles `{ 3, 4, 5, 6 }` , DirectMLX calcule automatiquement les propriétés du tenseur de sortie, y compris la forme correcte de `{ 1, 4, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="f14cb-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="f14cb-145">Toutefois, les autres propriétés d’un tenseur de sortie incluent les *Strides*, *TotalTensorSizeInBytes* et *GuaranteedBaseOffsetAlignment*.</span><span class="sxs-lookup"><span data-stu-id="f14cb-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="f14cb-146">Par défaut, DirectMLX définit ces propriétés de manière à ce que le tenseur n’ait aucun striding, aucun alignement de décalage de base garanti et une taille de tenseur totale en octets telle qu’elle est calculée par [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span><span class="sxs-lookup"><span data-stu-id="f14cb-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="f14cb-147">DirectMLX prend en charge la possibilité de personnaliser ces propriétés de tenseur de sortie, à l’aide d’objets appelés *stratégies tenseur*.</span><span class="sxs-lookup"><span data-stu-id="f14cb-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="f14cb-148">Un **TensorPolicy** est un rappel personnalisable qui est appelé par DirectMLX, et retourne les propriétés tenseur de sortie en fonction du type de données, des indicateurs et des tailles de données calculés d’un tenseur.</span><span class="sxs-lookup"><span data-stu-id="f14cb-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="f14cb-149">Les stratégies tenseur peuvent être définies sur l’objet **DML :: Scope** et seront utilisées pour tous les opérateurs suivants sur ce graphique.</span><span class="sxs-lookup"><span data-stu-id="f14cb-149">Tensor policies can be set on the **dml::Scope** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="f14cb-150">Les stratégies tenseur peuvent également être définies directement lors de la construction d’un **TensorDesc**.</span><span class="sxs-lookup"><span data-stu-id="f14cb-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="f14cb-151">La disposition des dizaines produits par DirectMLX peut donc être contrôlée en définissant un **TensorPolicy** qui définit les Strides appropriés sur ses dizaines.</span><span class="sxs-lookup"><span data-stu-id="f14cb-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="f14cb-152">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="f14cb-152">Example 1</span></span>

```cpp
// Define a policy, which is a function that returns a TensorProperties given a data type,
// flags, and sizes.
dml::TensorProperties MyCustomPolicy(
    DML_TENSOR_DATA_TYPE dataType,
    DML_TENSOR_FLAGS flags,
    Span<const uint32_t> sizes)
{
    // Compute your custom strides, total tensor size in bytes, and guaranteed base
    // offset alignment
    dml::TensorProperties props;
    props.strides = /* ... */;
    props.totalTensorSizeInBytes = /* ... */;
    props.guaranteedBaseOffsetAlignment = /* ... */;
    return props;
};

// Set the policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a><span data-ttu-id="f14cb-153">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="f14cb-153">Example 2</span></span>

<span data-ttu-id="f14cb-154">DirectMLX fournit également d’autres stratégies tenseur intégrées.</span><span class="sxs-lookup"><span data-stu-id="f14cb-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="f14cb-155">La stratégie **InterleavedChannel** , par exemple, est fournie à des fins pratiques, et elle peut être utilisée pour produire des dizaines avec des Strides de telle sorte qu’elles soient écrites dans l’ordre des NHWC.</span><span class="sxs-lookup"><span data-stu-id="f14cb-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="f14cb-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f14cb-156">See also</span></span>

* [<span data-ttu-id="f14cb-157">DirectML GitHub</span><span class="sxs-lookup"><span data-stu-id="f14cb-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="f14cb-158">Exemple DirectMLX yolov4</span><span class="sxs-lookup"><span data-stu-id="f14cb-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="f14cb-159">Utilisation de Strides pour exprimer le remplissage et la disposition de la mémoire</span><span class="sxs-lookup"><span data-stu-id="f14cb-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="f14cb-160">Structure DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="f14cb-160">DML_GRAPH_DESC structure</span></span>](./directml/ns-directml-dml_graph_desc.md)