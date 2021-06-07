---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Définit des constantes qui spécifient un type de bord du graphique. Consultez [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) pour connaître l’utilisation de cette énumération.
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417416"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a>Énumération DML_GRAPH_EDGE_TYPE (directml. h)

Définit des constantes qui spécifient un type de bord du graphique. Consultez [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) pour connaître l’utilisation de cette énumération.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a>Constantes

| Nom | Description |
| ---- |:---- |
| DML_GRAPH_EDGE_TYPE_INVALID | Spécifie un type de périphérie de graphique inconnu et n’est jamais valide. L’utilisation de cette valeur génère une erreur. |
| DML_GRAPH_EDGE_TYPE_INPUT | Spécifie que le bord du graphique est décrit par la structure [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) . |
| DML_GRAPH_EDGE_TYPE_OUTPUT | Spécifie que le bord du graphique est décrit par la structure [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) . |
| DML_GRAPH_EDGE_TYPE_INTERMEDIATE | Spécifie que le bord du graphique est décrit par la structure [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) .<br><br># # Disponibilité<br><br>Cette API a été introduite dans la version DirectML `1.1.0` . |


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

* [IDMLDevice1 :: CompileGraph, méthode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Structure DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)     
* [Structure DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)
* [Structure DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md)
* [Structure DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md)
* [Structure DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md)