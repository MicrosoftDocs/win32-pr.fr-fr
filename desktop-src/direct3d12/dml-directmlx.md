---
title: DirectMLX
description: DirectMLX est une bibliothèque d’assistance en-tête C++ uniquement pour DirectML, conçue pour faciliter la composition d’opérateurs individuels en graphiques.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: ba7eca27a39b690f678bdac1ea0feba1991e8b40
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521186"
---
# <a name="directmlx"></a>DirectMLX

DirectMLX est une bibliothèque d’assistance en-tête C++ uniquement pour DirectML, conçue pour faciliter la composition d’opérateurs individuels en graphiques.

DirectMLX fournit des wrappers pratiques pour tous les types d’opérateur DirectML (DML), ainsi que des surcharges d’opérateur intuitives, ce qui simplifie l’instanciation des opérateurs DML et leur chaînage en graphiques complexes.

## <a name="where-to-find-directmlxh"></a>Emplacement de recherche `DirectMLX.h`

`DirectMLX.h` est distribué en tant que logiciel open source dans le cadre de la licence MIT. La dernière version se trouve sur le [GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Libraries).

## <a name="tensor-constraints"></a>Contraintes tenseur

DirectMLX requiert DirectML version 1.4.0 ou ultérieure (voir [l’historique des versions DirectML](dml-version-history.md#version-table)). Les versions antérieures de DirectML ne sont pas prises en charge.

DirectMLX. h requiert un compilateur C + 11, y compris (mais sans s’y limiter) :

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Notez qu’un compilateur C++ 17 (ou plus récent) est l’option que nous recommandons. La compilation pour C++ 11 est possible, mais elle nécessite l’utilisation de bibliothèques tierces (telles que [GSL](https://github.com/microsoft/GSL) et [abseil](https://github.com/abseil/abseil-cpp)) pour remplacer les fonctionnalités de la bibliothèque standard manquantes.

Si vous avez une configuration dont la compilation échoue `DirectMLX.h` , veuillez [Envoyer un problème sur notre GitHub](https://github.com/microsoft/DirectML/issues).

## <a name="basic-usage"></a>Utilisation de base

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Graph graph(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

Voici un autre exemple, qui crée un graphique DirectML pouvant calculer la [formule quadratique](https://en.wikipedia.org/wiki/Quadratic_formula).

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

dml::Graph graph(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(graph, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(graph, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a>Autres exemples

Vous trouverez des exemples complets à l’aide de DirectMLX sur le [référentiel GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Samples).

## <a name="compile-time-options"></a>Options de compilation

DirectMLX prend en charge les #define de compilation pour personnaliser différentes parties de l’en-tête.

|Option|Description|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Si #define, provoque l’appel d’erreurs `std::abort` plutôt que la levée d’une exception. Cette valeur est définie par défaut si les exceptions ne sont pas disponibles (par exemple, si les exceptions ont été désactivées dans les options du compilateur).|
|**DMLX_USE_WIL**|Si #define, les exceptions sont levées à l’aide des types d’exception de la [bibliothèque d’implémentation Windows](https://github.com/microsoft/wil) . Sinon, les types d’exceptions standard (tels que `std::runtime_error` ) sont utilisés à la place. Cette option n’a aucun effet si **DMLX_NO_EXCEPTIONS** est défini.|
|**DMLX_USE_ABSEIL**|Si #define, utilise [abseil](https://github.com/abseil/abseil-cpp) comme remplacements de suppression pour les types de bibliothèque standard non disponibles en c++ 11. Ces types incluent `absl::optional` (à la place de `std::optional` ), `absl::Span` (à la place de `std::span` ) et `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Détermine s’il faut utiliser [GSL](https://github.com/microsoft/GSL) comme remplacement de `std::span` . Si #define, les utilisations de `std::span` sont remplacées par `gsl::span` sur les compilateurs sans `std::span` implémentation native. Dans le cas contraire, une implémentation de dépôt Inline est fournie à la place. Notez que cette option est utilisée uniquement lors de la compilation sur un compilateur pré-C + + 20 sans prise en charge de `std::span` , et lorsqu’aucun autre remplacement de bibliothèque standard (comme abseil) n’est en cours d’utilisation.|

## <a name="controlling-tensor-layout"></a>Contrôle de la disposition tenseur

Pour la plupart des opérateurs, DirectMLX calcule les propriétés des dizaines de sortie de l’opérateur en votre nom. Par exemple, lorsque vous effectuez une opération `dml::Reduce` sur plusieurs axes `{ 0, 2, 3 }` avec un tenseur d’entrée de tailles `{ 3, 4, 5, 6 }` , DirectMLX calcule automatiquement les propriétés du tenseur de sortie, y compris la forme correcte de `{ 1, 4, 1, 1 }` .

Toutefois, les autres propriétés d’un tenseur de sortie incluent les *Strides*, *TotalTensorSizeInBytes* et *GuaranteedBaseOffsetAlignment*. Par défaut, DirectMLX définit ces propriétés de manière à ce que le tenseur n’ait aucun striding, aucun alignement de décalage de base garanti et une taille de tenseur totale en octets telle qu’elle est calculée par [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).

DirectMLX prend en charge la possibilité de personnaliser ces propriétés de tenseur de sortie, à l’aide d’objets appelés *stratégies tenseur*. Un **TensorPolicy** est un rappel personnalisable qui est appelé par DirectMLX, et retourne les propriétés tenseur de sortie en fonction du type de données, des indicateurs et des tailles de données calculés d’un tenseur.

Les stratégies tenseur peuvent être définies sur l’objet **DML :: Graph** et seront utilisées pour tous les opérateurs suivants sur ce graphique. Les stratégies tenseur peuvent également être définies directement lors de la construction d’un **TensorDesc**.

La disposition des dizaines produits par DirectMLX peut donc être contrôlée en définissant un **TensorPolicy** qui définit les Strides appropriés sur ses dizaines.

### <a name="example-1"></a>Exemple 1

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

// Set the policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a>Exemple 2

DirectMLX fournit également d’autres stratégies tenseur intégrées. La stratégie **InterleavedChannel** , par exemple, est fournie à des fins pratiques, et elle peut être utilisée pour produire des dizaines avec des Strides de telle sorte qu’elles soient écrites dans l’ordre des NHWC.

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Voir aussi

* [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Exemple DirectMLX yolov4](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Utilisation de Strides pour exprimer le remplissage et la disposition de la mémoire](./dml-strides.md)
* [Structure DML_GRAPH_DESC](/windows/win32/api/directml/ns-directml-dml_graph_desc)