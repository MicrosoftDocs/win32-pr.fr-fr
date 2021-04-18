---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: 'Décrit une connexion dans un graphique d’opérateurs DirectML définis par [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) et passé à [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Cette structure est utilisée pour définir une connexion d’une entrée de graphique à une entrée d’un nœud interne.'
helpviewer_keywords:
- DML_INPUT_GRAPH_EDGE_DESC
- DML_INPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_input_graph_edge_desc
- directml/DML_INPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
- directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 180bfc89a37aad2ba0b6f287c302aa30b0b04110
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106523098"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a>Structure DML_INPUT_GRAPH_EDGE_DESC (directml. h)
Décrit une connexion dans un graphique d’opérateurs DirectML définis par [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) et passé à [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Cette structure est utilisée pour définir une connexion d’une entrée de graphique à une entrée d’un nœud interne.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Membres

`GraphInputIndex`

Type : **[uint](/windows/desktop/winprog/windows-data-types)**

Index de l’entrée de graphique à partir de laquelle une connexion à une entrée de nœud interne est spécifiée.


`ToNodeIndex`

Type : **[uint](/windows/desktop/winprog/windows-data-types)**

Index du nœud interne sur lequel la connexion à partir de l’entrée de graphique est spécifiée.


`ToNodeInputIndex`

Type : **[uint](/windows/desktop/winprog/windows-data-types)**

Index de l’entrée sur le nœud interne où la connexion est spécifiée.


`Name`

Type : \_ champ \_ z \_ \_ MAYBENULL \_ **const char \***

Nom facultatif pour la connexion du graphique. S’il est fourni, il peut être utilisé dans certains messages d’erreur émis par la couche de débogage DirectML.

## <a name="availability"></a>Disponibilité

Cette API a été introduite dans la version DirectML `1.1.0` .



## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

* [IDMLDevice1 :: CompileGraph, méthode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Structure DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [Structure DML_GRAPH_EDGE_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)