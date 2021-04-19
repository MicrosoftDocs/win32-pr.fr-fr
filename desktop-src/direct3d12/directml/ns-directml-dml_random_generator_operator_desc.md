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
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>Structure DML_RANDOM_GENERATOR_OPERATOR_DESC (directml. h)

Remplit un tenseur de sortie avec des bits générés de façon déterministe, Pseudo-aléatoire et distribué uniformément. Cet opérateur peut éventuellement également générer un état de générateur interne mis à jour, qui peut être utilisé lors des exécutions ultérieures de l’opérateur.

Cet opérateur est déterministe et se comporte comme s’il s’agissait d’une fonction pure &mdash; qui est, son exécution ne produit aucun effet secondaire et n’utilise pas d’état global. La sortie Pseudo-aléatoire produite par cet opérateur dépend uniquement des valeurs fournies dans le *InputStateTensor*.

Les générateurs implémentés par cet opérateur ne sont pas sécurisés par chiffrement ; par conséquent, cet opérateur ne doit pas être utilisé pour le chiffrement, la génération de clés ou d’autres applications qui nécessitent une génération de nombres aléatoires sécurisés par chiffrement.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a>Membres

`InputStateTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur d’entrée contenant l’état du générateur interne. La taille et le format de ce tenseur d’entrée dépend de la [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).

Pour **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, ce tenseur doit être de type **UInt32** et avoir des tailles `{1,1,1,6}` . Les premières valeurs de 4 32 bits contiennent un compteur de 128 bits qui croît de façon monotone. Les dernières valeurs de 2 32 bits contiennent la valeur de clé de 64 bits pour le générateur.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

Lorsque vous initialisez l’état d’entrée du générateur pour la première fois, en général le compteur 128 bits (les premières valeurs UINT32 4 32 bits) doit être initialisé à 0. La clé peut être choisie arbitrairement ; des valeurs de clés différentes produiront différentes séquences de nombres. La valeur de la clé est généralement générée à l’aide d’une valeur *initiale* fournie par l’utilisateur.

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie qui contient les valeurs Pseudo-aléatoires résultantes. Ce tenseur peut être de n’importe quelle taille.

`OutputStateTensor`

Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie facultatif qui contient l’état de générateur interne mis à jour. S’il est fourni, cet opérateur utilise *InputStateTensor* pour calculer un état de générateur mis à jour approprié et écrit le résultat dans le *OutputStateTensor*. En règle générale, les appelants enregistrent ce résultat et le fournissent comme état d’entrée lors de l’exécution suivante de cet opérateur.

`Type`

Type : **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

L’une des valeurs de l’énumération [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , indiquant le type de générateur à utiliser. Actuellement, la seule valeur valide est **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, qui génère des nombres pseudo-aléatoires en fonction de l' [algorithme 4X32-10 PHILOX](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).

## <a name="remarks"></a>Notes
À chaque exécution de cet opérateur, le compteur 128 bits doit être incrémenté. Si le *OutputStateTensor* est fourni, cet opérateur incrémente le compteur avec la valeur correcte en votre nom et écrit le résultat dans le *OutputStateTensor*. La quantité qui doit être incrémentée en fonction du nombre d’éléments de sortie 32 bits générés et du type du générateur.

Par **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, le compteur 128 bits doit être incrémenté de à `ceil(outputSize / 4)` chaque exécution, où `outputSize` est le nombre d’éléments dans le *OutputTensor*.

Prenons un exemple où la valeur du compteur de bits 128 est actuellement `0x48656c6c'6f46726f'6d536561'74746c65` , et la taille de OutputTensor est `{3,3,20,7219}` . Après l’exécution de cet opérateur une fois, le compteur doit être incrémenté de 324 855 (le nombre d’éléments de sortie générés divisé par 4, arrondi vers le haut), entraînant une valeur de compteur de `0x48656c6c'6f46726f'6d536561'746f776e` . Cette valeur mise à jour doit ensuite être fournie en tant qu’entrée pour la prochaine exécution de cet opérateur.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
`InputStateTensor` et `OutputStateTensor` doivent avoir les mêmes *tailles*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Dimensions | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputStateTensor | Entrée | {1, 1, 1, 6} | 4 | UINT32 |
| OutputTensor | Output | {D0, D1, D2, D3} | 4 | UINT32 |
| OutputStateTensor | Sortie facultative | {1, 1, 1, 6} | 4 | UINT32 |

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |