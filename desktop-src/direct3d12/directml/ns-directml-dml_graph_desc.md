---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Décrit un graphique des opérateurs DirectML utilisés pour compiler un opérateur combiné optimisé.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802876"
---
# <a name="dml_graph_desc-structure-directmlh"></a>Structure DML_GRAPH_DESC (directml. h)

Décrit un graphique des opérateurs DirectML utilisés pour compiler un opérateur combiné optimisé. Consultez [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a>Membres

`InputCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre d’entrées du graphique global. Chaque entrée de graphique peut être connectée à un nombre variable de nœuds internes. par conséquent, elle peut être différente de *InputEdgeCount*.


`OutputCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de sorties de l’ensemble du graphique. Chaque sortie de graphique peut être connectée à un nombre variable de nœuds internes. par conséquent, elle peut être différente de *OutputEdgeCount*.


`NodeCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de nœuds internes dans le graphique.


`Nodes`

Type : \_ taille du champ \_ \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Nœuds internes du graphique.


`InputEdgeCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de connexions entre les entrées de graphique et les entrées de nœuds internes dans le graphique.


`InputEdges`

Type : \_ taille du champ \_ \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Tableau de connexions entre les entrées de graphique et les entrées de nœuds internes dans le graphique. Le champ de *type* de chaque élément doit avoir la valeur [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).


`OutputEdgeCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de connexions entre les sorties de graphique et les sorties de nœuds internes dans le graphique.


`OutputEdges`

Type : \_ taille du champ \_ \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Tableau de connexions entre les sorties de graphique et les sorties de nœuds internes dans le graphique. Le champ de *type* de chaque élément doit avoir la valeur [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).


`IntermediateEdgeCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de connexions internes entre les nœuds dans le graphique.


`IntermediateEdges`

Type : \_ taille du champ \_ \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Tableau de connexions entre les entrées et les sorties des nœuds internes du graphique. Le champ de type de chaque élément doit avoir la valeur [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Notes 
Le graphique décrit par cette structure doit être un graphique acycliques orienté. Vous devez définir une connexion pour l’entrée et la sortie de chaque nœud fourni, à l’exception des entrées et des sorties qui sont facultatives pour l’opérateur associé.

Les nœuds peuvent utiliser des opérateurs qui ont été créés à l’aide de l’indicateur [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) pour certaines entrées. Toutes les entrées d’opérateur à l’aide de cet indicateur doivent être connectées aux entrées de graphique. Toutes les entrées d’opérateur connectées à la même entrée de graphique doivent utiliser ou omettre cet indicateur de façon équivalente.

Il est légal de connecter les opérateurs dont les entrées et les sorties connectées utilisent des nombres de dimensions, des tailles et des types de données différents. Cela implique que l’objet blob de données tenseur est interprété différemment par chaque opérateur. Toutefois, le champ *TotalTensorSizeInBytes* des entrées et sorties tenseur connectées doit être identique. Les opérateurs doivent uniquement lire les régions de dizaines écrits par des opérateurs antérieurs. Il n’est pas garanti que les zones de remplissage dans la sortie d’une opération (résultant de l’utilisation de Strides) soient lues comme zéro par les opérateurs en aval.

## <a name="availability"></a>Disponibilité

Cette API a été introduite dans la version DirectML `1.1.0` .


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

* [IDMLDevice1 :: CompileGraph, méthode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Struct DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)
* [Struct DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)