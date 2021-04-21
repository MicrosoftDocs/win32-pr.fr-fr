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
ms.openlocfilehash: 00fcece76f4cb7ac46589914df4d74321d957fbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802890"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="66cb0-104">Structure DML_INPUT_GRAPH_EDGE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="66cb0-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="66cb0-105">Décrit une connexion dans un graphique d’opérateurs DirectML définis par [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) et passé à [IDMLDevice1 :: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="66cb0-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="66cb0-106">Cette structure est utilisée pour définir une connexion d’une entrée de graphique à une entrée d’un nœud interne.</span><span class="sxs-lookup"><span data-stu-id="66cb0-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66cb0-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="66cb0-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="66cb0-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="66cb0-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="66cb0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66cb0-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="66cb0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="66cb0-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="66cb0-111">Type : **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="66cb0-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="66cb0-112">Index de l’entrée de graphique à partir de laquelle une connexion à une entrée de nœud interne est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="66cb0-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="66cb0-113">Type : **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="66cb0-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="66cb0-114">Index du nœud interne sur lequel la connexion à partir de l’entrée de graphique est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="66cb0-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="66cb0-115">Type : **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="66cb0-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="66cb0-116">Index de l’entrée sur le nœud interne où la connexion est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="66cb0-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="66cb0-117">Type : \_ champ \_ z \_ \_ MAYBENULL \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="66cb0-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="66cb0-118">Nom facultatif pour la connexion du graphique.</span><span class="sxs-lookup"><span data-stu-id="66cb0-118">An optional name for the graph connection.</span></span> <span data-ttu-id="66cb0-119">S’il est fourni, il peut être utilisé dans certains messages d’erreur émis par la couche de débogage DirectML.</span><span class="sxs-lookup"><span data-stu-id="66cb0-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="66cb0-120">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="66cb0-120">Availability</span></span>

<span data-ttu-id="66cb0-121">Cette API a été introduite dans la version DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="66cb0-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="66cb0-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="66cb0-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="66cb0-123">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="66cb0-123">**Header**</span></span> | <span data-ttu-id="66cb0-124">directml. h</span><span class="sxs-lookup"><span data-stu-id="66cb0-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="66cb0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66cb0-125">See also</span></span>

* [<span data-ttu-id="66cb0-126">IDMLDevice1 :: CompileGraph, méthode</span><span class="sxs-lookup"><span data-stu-id="66cb0-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="66cb0-127">Structure DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="66cb0-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="66cb0-128">Structure DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="66cb0-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)