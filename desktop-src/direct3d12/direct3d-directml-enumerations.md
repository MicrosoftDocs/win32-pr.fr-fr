---
title: Énumérations DirectML
description: Les énumérations suivantes sont déclarées dans DirectML. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: 2a761dba639ece37eba347115a831d3c6803a618
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293591"
---
# <a name="directml-enumerations"></a>Énumérations DirectML

Les énumérations suivantes sont déclarées dans DirectML. h.

## <a name="in-this-section"></a>Dans cette section

| Rubrique et description |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_axis_direction). Définit des constantes qui spécifient la direction d’une opération le long de l’axe donné pour l’opérateur (par exemple, la somme, en sélectionnant les éléments les plus hauts, en sélectionnant l’élément minimum). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Définit des constantes qui spécifient la nature de la ou des ressources référencées par une description de liaison [DML_BINDING_DESC structure](/windows/desktop/api/directml/ns-directml-dml_binding_desc). |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Définit des constantes qui spécifient une direction pour l’opérateur de convolution DirectML (comme décrit par la [structure DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Définit des constantes qui spécifient un mode pour l’opérateur de convolution DirectML (comme décrit par la [structure DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Fournit des options de création d’appareils supplémentaires à [DMLCreateDevice](/windows/desktop/api/directml/nf-directml-dmlcreatedevice). |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/api/directml/ne-directml-dml_depth_space_order). Définit des constantes contrôlant la transformation appliquée dans les opérateurs DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) et **DML_OPERATOR_SPACE_TO_DEPTH1**. |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Fournit des options à DirectML pour contrôler l’exécution des opérateurs. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Définit un ensemble de fonctionnalités facultatives qui peuvent être interrogées à partir de l’appareil DirectML. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_edge_type). Définit des constantes qui spécifient un type de bord du graphique. Consultez [DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) pour connaître l’utilisation de cette énumération. |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_node_type). Définit des constantes qui spécifient un type de nœud de graphique. Consultez [DML_GRAPH_NODE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_node_desc) pour connaître l’utilisation de cette énumération. |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Définit des constantes qui spécifient un mode pour l’opérateur DirectML-D exemple 2-D (comme décrit par la [structure DML_UPSAMPLE_2D_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc)). |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Définit des constantes qui spécifient une transformation de matrice à appliquer à un tenseur DirectML. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Définit le type d’une description d’opérateur. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Définit des constantes qui spécifient un mode pour l’opérateur DirectML Pad (comme décrit par la [structure DML_PADDING_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc)). |
| [**DML_RANDOM_GENERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_random_generator_type). Définit des constantes qui spécifient des types de générateur de nombres aléatoires aléatoires. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Définit des constantes qui spécifient la direction d’un opérateur DirectML à jour. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Définit des constantes qui spécifient l’algorithme de réduction spécifique à utiliser pour l’opérateur DirectML Reduce (comme décrit par la [structure DML_REDUCE_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)). |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Spécifie le type de données des valeurs dans un tenseur. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Spécifie des options supplémentaires dans une description de tenseur. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Identifie un type de description tenseur. |

## <a name="related-topics"></a>Rubriques connexes

* [Référence DirectML](direct3d-directml-reference.md)
* [Référence de base](direct3d-12-core-reference.md)
* [Référence de Direct3D 12](direct3d-12-reference.md)