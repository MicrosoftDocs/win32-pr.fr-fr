---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: 'Conteneur générique pour une connexion dans un graphique d’opérateurs DirectML définis par [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) et passés à [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_GRAPH_EDGE_DESC
- DML_GRAPH_EDGE_DESC structure
- direct3d12.dml_graph_edge_desc
- directml/DML_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
- directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
ms.openlocfilehash: 58cdf22dd85b1464d68cf1db75ff47a34817514c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802923"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a>Structure DML_GRAPH_EDGE_DESC (directml. h)
Conteneur générique pour une connexion dans un graphique d’opérateurs DirectML définis par [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) et passés à [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>Membres

`Type`

Type : **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**

Type de l’arête du graphique. Consultez [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) pour connaître les types disponibles et [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) pour savoir où utiliser chaque type.


`Desc`

Type : \_ taille du champ \_ \_ ( \_ Inexpressible \_ (« dépendant du type de périphérie »)) **const void \***

Pointeur vers la description de l’arête du graphique. Le type du struct pointé doit correspondre à la valeur spécifiée dans *type*.

## <a name="availability"></a>Disponibilité

Cette API a été introduite dans la version DirectML `1.1.0` .



## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

* [IDMLDevice1 :: CompileGraph, méthode](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Structure DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)