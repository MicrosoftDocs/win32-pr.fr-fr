---
UID: NE:directml.DML_GRAPH_NODE_TYPE
title: DML_GRAPH_NODE_TYPE
description: Définit des constantes qui spécifient un type de nœud de graphique. Consultez [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) pour connaître l’utilisation de cette énumération.
helpviewer_keywords:
- DML_GRAPH_NODE_TYPE
- DML_GRAPH_NODE_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_GRAPH_NODE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_TYPE, DML_GRAPH_NODE_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
- directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
ms.openlocfilehash: 0bb0712370da35c4b8c9278ad7721d2ffc7d875d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417180"
---
# <a name="dml_graph_node_type-enumeration-directmlh"></a><span data-ttu-id="49465-104">Énumération DML_GRAPH_NODE_TYPE (directml. h)</span><span class="sxs-lookup"><span data-stu-id="49465-104">DML_GRAPH_NODE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="49465-105">Définit des constantes qui spécifient un type de nœud de graphique.</span><span class="sxs-lookup"><span data-stu-id="49465-105">Defines constants that specify a type of graph node.</span></span> <span data-ttu-id="49465-106">Consultez [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) pour connaître l’utilisation de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="49465-106">See [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49465-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="49465-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="49465-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="49465-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="49465-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49465-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a><span data-ttu-id="49465-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="49465-110">Constants</span></span>

| <span data-ttu-id="49465-111">Nom</span><span class="sxs-lookup"><span data-stu-id="49465-111">Name</span></span> | <span data-ttu-id="49465-112">Description</span><span class="sxs-lookup"><span data-stu-id="49465-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="49465-113">DML_GRAPH_NODE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="49465-113">DML_GRAPH_NODE_TYPE_INVALID</span></span> | <span data-ttu-id="49465-114">Spécifie un type de périphérie de graphique inconnu et n’est jamais valide.</span><span class="sxs-lookup"><span data-stu-id="49465-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="49465-115">L’utilisation de cette valeur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="49465-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="49465-116">DML_GRAPH_NODE_TYPE_OPERATOR</span><span class="sxs-lookup"><span data-stu-id="49465-116">DML_GRAPH_NODE_TYPE_OPERATOR</span></span> | <span data-ttu-id="49465-117">Spécifie que le bord du graphique est décrit par la structure [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="49465-117">Specifies that the graph edge is described by the [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) structure.</span></span><br><br><span data-ttu-id="49465-118"># # Disponibilité</span><span class="sxs-lookup"><span data-stu-id="49465-118">## Availability</span></span><br><br><span data-ttu-id="49465-119">Cette API a été introduite dans la version DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="49465-119">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="49465-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="49465-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="49465-121">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="49465-121">**Header**</span></span> | <span data-ttu-id="49465-122">directml. h</span><span class="sxs-lookup"><span data-stu-id="49465-122">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="49465-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49465-123">See also</span></span>

* [<span data-ttu-id="49465-124">IDMLDevice1 :: CompileGraph, méthode</span><span class="sxs-lookup"><span data-stu-id="49465-124">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="49465-125">Structure DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="49465-125">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="49465-126">Structure DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="49465-126">DML_GRAPH_NODE_DESC structure</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="49465-127">DML_OPERATOR_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="49465-127">DML_OPERATOR_GRAPH_NODE_DESC</span></span>](./ns-directml-dml_operator_graph_node_desc.md)