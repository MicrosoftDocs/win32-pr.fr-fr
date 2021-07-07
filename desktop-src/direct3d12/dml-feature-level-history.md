---
title: Historique des niveaux de fonctionnalité DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282548"
---
# <a name="directml-feature-level-history"></a>Historique des niveaux de fonctionnalité DirectML

Pour un historique général des versions de DirectML, consultez [l’historique des versions DirectML](./dml-version-history.md).

## <a name="dml_feature_level_4_0"></a>DML_FEATURE_LEVEL_4_0

Introduit dans DirectML version 1.6.0.

Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.

* **DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**
* **DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**
* **DML_OPERATOR_ROI_ALIGN1**

Prise en charge des types de données étendus et du nombre de dimensions pour les opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Pour plus d’informations sur la prise en charge spécifique ajoutée dans [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), consultez la rubrique relative à la structure de chaque opérateur.

* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_CONVOLUTION**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_CUMULATIVE_PRODUCT**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**

## <a name="dml_feature_level_3_1"></a>DML_FEATURE_LEVEL_3_1

Introduit dans DirectML version 1.5.0.

Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.

* **DML_OPERATOR_ELEMENT_WISE_ATAN_YX**
* **DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**
* **DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**
* **DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**
* **DML_OPERATOR_CUMULATIVE_PRODUCT**
* **DML_OPERATOR_BATCH_NORMALIZATION_GRAD**

Le nombre maximal de dimensions prises en charge pour les opérateurs suivants est passé de 4 à 8.

* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_CAST**
* **DML_OPERATOR_JOIN**
* **DML_OPERATOR_LP_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_PADDING**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_TILE**
* **DML_OPERATOR_TOP_K**
* **DML_OPERATOR_TOP_K1**

## <a name="dml_feature_level_3_0"></a>DML_FEATURE_LEVEL_3_0

Introduit dans DirectML version 1.4.0.

Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.

* **DML_OPERATOR_ELEMENT_WISE_BIT_AND**
* **DML_OPERATOR_ELEMENT_WISE_BIT_OR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_XOR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_NOT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**
* **DML_OPERATOR_ACTIVATION_CELU**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_AVERAGE_POOLING_GRAD**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_RESAMPLE_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_ARGMIN**
* **DML_OPERATOR_ARGMAX**
* **DML_OPERATOR_ROI_ALIGN**
* **DML_OPERATOR_GATHER_ND1**

Ajout des améliorations suivantes :

* Le nombre maximal de dimensions de tenseur a été augmenté de 5 à 8. Consultez [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).
* Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.
  * **DML_OPERATOR_ELEMENT_WISE_POW**
  * **DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**
  * **DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** et **DML_OPERATOR_MAX_POOLING2**
  * **DML_OPERATOR_REDUCE**, lors de l’utilisation de **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**
* Les types de données 64 bits suivants ont été ajoutés et sont pris en charge par les opérateurs Select.
  * **DML_TENSOR_DATA_TYPE_FLOAT64**
  * **DML_TENSOR_DATA_TYPE_UINT64**
  * **DML_TENSOR_DATA_TYPE_INT64**

Fonctionnalités dépréciées.

* **DML_REDUCE_FUNCTION_ARGMAX** et **DML_REDUCE_FUNCTION_ARGMIN** ont été dépréciés. Il est préférable d’utiliser les opérateurs **DML_OPERATOR_ARGMIN** et **DML_OPERATOR_ARGMAX** autonomes à leur place.

## <a name="dml_feature_level_2_1"></a>DML_FEATURE_LEVEL_2_1

Introduit dans DirectML version 1.2.0.

Ajout des API suivantes.

* [Interface IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice1)
* Prise en charge des graphiques d’opérateur (consultez [IDMLDevice1 :: CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)

Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.

* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**
* **DML_OPERATOR_ELEMENT_WISE_ROUND**
* **DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**
* **DML_OPERATOR_GATHER_ELEMENTS**
* **DML_OPERATOR_GATHER_ND**
* **DML_OPERATOR_SCATTER_ND**
* **DML_OPERATOR_MAX_POOLING2**
* **DML_OPERATOR_SLICE1**
* **DML_OPERATOR_TOP_K1**
* **DML_OPERATOR_DEPTH_TO_SPACE1**
* **DML_OPERATOR_SPACE_TO_DEPTH1**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_RESAMPLE1**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**

Ajout des améliorations suivantes :

* Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.
  * **DML_OPERATOR_ELEMENT_WISE_IDENTITY**
  * **DML_OPERATOR_ELEMENT_WISE_ABS**
  * **DML_OPERATOR_ELEMENT_WISE_ADD**
  * **DML_OPERATOR_ELEMENT_WISE_CLIP**
  * **DML_OPERATOR_ELEMENT_WISE_DIVIDE**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_MAX**
  * **DML_OPERATOR_ELEMENT_WISE_MEAN**
  * **DML_OPERATOR_ELEMENT_WISE_MIN**
  * **DML_OPERATOR_ELEMENT_WISE_MULTIPLY**
  * **DML_OPERATOR_ELEMENT_WISE_SUBTRACT**
  * **DML_OPERATOR_ELEMENT_WISE_THRESHOLD**
  * **DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_SIGN**
  * **DML_OPERATOR_ELEMENT_WISE_IF**
  * **DML_OPERATOR_ACTIVATION_SHRINK**
  * **DML_OPERATOR_PADDING**
  * **DML_OPERATOR_GATHER**
  * **DML_OPERATOR_SCATTER**
  * **DML_OPERATOR_DEPTH_TO_SPACE**
  * **DML_OPERATOR_SPACE_TO_DEPTH**
  * **DML_OPERATOR_TILE**
  * **DML_OPERATOR_TOP_K** et **DML_OPERATOR_TOP_K1**
  * **DML_OPERATOR_ONE_HOT**
  * **DML_OPERATOR_REDUCE**, lors de l’utilisation de l’une des fonctions de réduction suivantes.
    * **DML_REDUCE_FUNCTION_ARGMIN**
    * **DML_REDUCE_FUNCTION_ARGMAX**
    * **DML_REDUCE_FUNCTION_MAX**
    * **DML_REDUCE_FUNCTION_MIN**
    * **DML_REDUCE_FUNCTION_MULTIPLY**
    * **DML_REDUCE_FUNCTION_SUM**
* Restrictions de forme de tenseur souple pour **DML_OPERATOR_GATHER**

## <a name="dml_feature_level_2_0"></a>DML_FEATURE_LEVEL_2_0

Introduit dans DirectML version 1.1.0.

Ajout des API suivantes.
* [Fonction DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [Énumération DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* Requêtes au niveau des fonctionnalités (voir [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))

Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.

* **DML_OPERATOR_ELEMENT_WISE_SIGN**
* **DML_OPERATOR_ELEMENT_WISE_IS_NAN**
* **DML_OPERATOR_ELEMENT_WISE_ERF**
* **DML_OPERATOR_ELEMENT_WISE_SINH**
* **DML_OPERATOR_ELEMENT_WISE_COSH**
* **DML_OPERATOR_ELEMENT_WISE_TANH**
* **DML_OPERATOR_ELEMENT_WISE_ASINH**
* **DML_OPERATOR_ELEMENT_WISE_ACOSH**
* **DML_OPERATOR_ELEMENT_WISE_ATANH**
* **DML_OPERATOR_ELEMENT_WISE_IF**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_MAX_POOLING1**
* **DML_OPERATOR_MAX_UNPOOLING**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_SCATTER_ELEMENTS**
* **DML_OPERATOR_SCATTER**
* **DML_OPERATOR_ONE_HOT**
* **DML_OPERATOR_RESAMPLE**

Ajout des améliorations suivantes :

* Lors de la liaison d’une ressource d’entrée pour la distribution d’un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), il est maintenant légal de fournir une ressource avec [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (en plus de **D3D12_HEAP_TYPE_DEFAULT**), à condition que les propriétés de tas appropriées soient également définies. Consultez [liaison dans DirectML](./dml-binding.md).
* Les opérateurs booléens logiques suivants prennent désormais en charge les dizaines de temps de sortie **UINT8** , en plus de la prise en charge existante de **UInt32**.
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**
* 5J les fonctions d’activation prennent désormais en charge l’utilisation de Strides sur leurs dizaines d’entrée et de sortie.

## <a name="dml_feature_level_1_0"></a>DML_FEATURE_LEVEL_1_0

Niveau de fonctionnalité dans lequel DirectML a été introduit.

## <a name="see-also"></a>Voir aussi

* [Historique des versions DirectML](./dml-version-history.md)
* [Énumération DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Fonction DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [Structure DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
