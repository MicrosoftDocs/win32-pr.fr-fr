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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417356"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="4fe84-103">Structure DML_GRAPH_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="4fe84-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="4fe84-104">Décrit un graphique des opérateurs DirectML utilisés pour compiler un opérateur combiné optimisé.</span><span class="sxs-lookup"><span data-stu-id="4fe84-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="4fe84-105">Consultez [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="4fe84-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fe84-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4fe84-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4fe84-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="4fe84-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe84-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fe84-108">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="4fe84-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4fe84-109">Members</span></span>

`InputCount`

<span data-ttu-id="4fe84-110">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fe84-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fe84-111">Nombre d’entrées du graphique global.</span><span class="sxs-lookup"><span data-stu-id="4fe84-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="4fe84-112">Chaque entrée de graphique peut être connectée à un nombre variable de nœuds internes. par conséquent, elle peut être différente de *InputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="4fe84-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="4fe84-113">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fe84-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fe84-114">Nombre de sorties de l’ensemble du graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="4fe84-115">Chaque sortie de graphique peut être connectée à un nombre variable de nœuds internes. par conséquent, elle peut être différente de *OutputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="4fe84-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="4fe84-116">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fe84-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fe84-117">Nombre de nœuds internes dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="4fe84-118">Type : \_ taille du champ \_ \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="4fe84-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="4fe84-119">Nœuds internes du graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="4fe84-120">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fe84-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fe84-121">Nombre de connexions entre les entrées de graphique et les entrées de nœuds internes dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="4fe84-122">Type : \_ taille du champ \_ \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="4fe84-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="4fe84-123">Tableau de connexions entre les entrées de graphique et les entrées de nœuds internes dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="4fe84-124">Le champ de *type* de chaque élément doit avoir la valeur [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="4fe84-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="4fe84-125">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fe84-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fe84-126">Nombre de connexions entre les sorties de graphique et les sorties de nœuds internes dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="4fe84-127">Type : \_ taille du champ \_ \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="4fe84-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="4fe84-128">Tableau de connexions entre les sorties de graphique et les sorties de nœuds internes dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="4fe84-129">Le champ de *type* de chaque élément doit avoir la valeur [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="4fe84-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="4fe84-130">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fe84-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fe84-131">Nombre de connexions internes entre les nœuds dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="4fe84-132">Type : \_ taille du champ \_ \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="4fe84-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="4fe84-133">Tableau de connexions entre les entrées et les sorties des nœuds internes du graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="4fe84-134">Le champ de type de chaque élément doit avoir la valeur [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="4fe84-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="4fe84-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="4fe84-135">Remarks</span></span>
<span data-ttu-id="4fe84-136">Le graphique décrit par cette structure doit être un graphique acycliques orienté.</span><span class="sxs-lookup"><span data-stu-id="4fe84-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="4fe84-137">Vous devez définir une connexion pour l’entrée et la sortie de chaque nœud fourni, à l’exception des entrées et des sorties qui sont facultatives pour l’opérateur associé.</span><span class="sxs-lookup"><span data-stu-id="4fe84-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="4fe84-138">Les nœuds peuvent utiliser des opérateurs qui ont été créés à l’aide de l’indicateur [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) pour certaines entrées.</span><span class="sxs-lookup"><span data-stu-id="4fe84-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="4fe84-139">Toutes les entrées d’opérateur à l’aide de cet indicateur doivent être connectées aux entrées de graphique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="4fe84-140">Toutes les entrées d’opérateur connectées à la même entrée de graphique doivent utiliser ou omettre cet indicateur de façon équivalente.</span><span class="sxs-lookup"><span data-stu-id="4fe84-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="4fe84-141">Il est légal de connecter les opérateurs dont les entrées et les sorties connectées utilisent des nombres de dimensions, des tailles et des types de données différents.</span><span class="sxs-lookup"><span data-stu-id="4fe84-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="4fe84-142">Cela implique que l’objet blob de données tenseur est interprété différemment par chaque opérateur.</span><span class="sxs-lookup"><span data-stu-id="4fe84-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="4fe84-143">Toutefois, le champ *TotalTensorSizeInBytes* des entrées et sorties tenseur connectées doit être identique.</span><span class="sxs-lookup"><span data-stu-id="4fe84-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="4fe84-144">Les opérateurs doivent uniquement lire les régions de dizaines écrits par des opérateurs antérieurs.</span><span class="sxs-lookup"><span data-stu-id="4fe84-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="4fe84-145">Il n’est pas garanti que les zones de remplissage dans la sortie d’une opération (résultant de l’utilisation de Strides) soient lues comme zéro par les opérateurs en aval.</span><span class="sxs-lookup"><span data-stu-id="4fe84-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="4fe84-146">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="4fe84-146">Availability</span></span>

<span data-ttu-id="4fe84-147">Cette API a été introduite dans la version DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="4fe84-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="4fe84-148">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4fe84-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4fe84-149">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="4fe84-149">**Header**</span></span> | <span data-ttu-id="4fe84-150">directml. h</span><span class="sxs-lookup"><span data-stu-id="4fe84-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="4fe84-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fe84-151">See also</span></span>

* [<span data-ttu-id="4fe84-152">IDMLDevice1 :: CompileGraph, méthode</span><span class="sxs-lookup"><span data-stu-id="4fe84-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="4fe84-153">Struct DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="4fe84-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="4fe84-154">Struct DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="4fe84-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)