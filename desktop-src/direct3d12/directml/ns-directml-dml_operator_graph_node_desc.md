---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: 'Décrit un nœud dans un graphique d’opérateurs DirectML définis par [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) et passé à [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/05/2020
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 997f441de76a60229b76f2f7d67b7acf1a26ed5f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417232"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a><span data-ttu-id="ad837-103">Structure DML_OPERATOR_GRAPH_NODE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ad837-103">DML_OPERATOR_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="ad837-104">Décrit un nœud dans un graphique d’opérateurs DirectML définis par [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) et passé à [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="ad837-104">Decribes a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

<span data-ttu-id="ad837-105">Le comportement de ce nœud est défini par un opérateur DirectML.</span><span class="sxs-lookup"><span data-stu-id="ad837-105">The behavior of this node is defined by a DirectML operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad837-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ad837-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ad837-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ad837-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad837-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad837-108">Syntax</span></span>
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a><span data-ttu-id="ad837-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ad837-109">Members</span></span>

`Operator`

<span data-ttu-id="ad837-110">Type : <b> [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span><span class="sxs-lookup"><span data-stu-id="ad837-110">Type: <b>[IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span></span>

<span data-ttu-id="ad837-111">Opérateur DirectML définissant le comportement du nœud.</span><span class="sxs-lookup"><span data-stu-id="ad837-111">A DirectML operator defining the behavior of the node.</span></span>


`Name`

<span data-ttu-id="ad837-112">Type : \_ champ \_ z \_ \_ MAYBENULL \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="ad837-112">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="ad837-113">Nom facultatif pour la connexion du graphique.</span><span class="sxs-lookup"><span data-stu-id="ad837-113">An optional name for the graph connection.</span></span> <span data-ttu-id="ad837-114">S’il est fourni, il peut être utilisé dans certains messages d’erreur émis par la couche de débogage DirectML.</span><span class="sxs-lookup"><span data-stu-id="ad837-114">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="ad837-115">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="ad837-115">Availability</span></span>

<span data-ttu-id="ad837-116">Cette API a été introduite dans la version DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="ad837-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="ad837-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ad837-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ad837-118">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="ad837-118">**Header**</span></span> | <span data-ttu-id="ad837-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="ad837-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ad837-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad837-120">See also</span></span>

* [<span data-ttu-id="ad837-121">IDMLDevice1 :: CompileGraph, méthode</span><span class="sxs-lookup"><span data-stu-id="ad837-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="ad837-122">Structure DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="ad837-122">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="ad837-123">Structure DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="ad837-123">DML_GRAPH_NODE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)