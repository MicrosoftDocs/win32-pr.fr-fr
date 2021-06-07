---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Définit des constantes contrôlant la transformation appliquée dans les opérateurs DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) et **DML_OPERATOR_SPACE_TO_DEPTH1**.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417215"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="fd4b5-103">Énumération DML_DEPTH_SPACE_ORDER (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fd4b5-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="fd4b5-104">Définit des constantes contrôlant la transformation appliquée dans les opérateurs DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) et **DML_OPERATOR_SPACE_TO_DEPTH1**.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="fd4b5-105">Elles sont utilisées dans les structures [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="fd4b5-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd4b5-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="fd4b5-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fd4b5-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4b5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd4b5-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="fd4b5-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="fd4b5-109">Constants</span></span>

| <span data-ttu-id="fd4b5-110">Nom</span><span class="sxs-lookup"><span data-stu-id="fd4b5-110">Name</span></span> | <span data-ttu-id="fd4b5-111">Description</span><span class="sxs-lookup"><span data-stu-id="fd4b5-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="fd4b5-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="fd4b5-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="fd4b5-113">Provoque l’interprétation des dizaines d' [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et des [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) avec les dispositions suivantes, où les dimensions entre parenthèses sont aplaties ensemble.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="fd4b5-114">- **Version de profondeur**: [lot, (BlockHeight, BlockWidth, canaux), hauteur, largeur]</span><span class="sxs-lookup"><span data-stu-id="fd4b5-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="fd4b5-115">- **Version d’espace**: [lot, canaux, (hauteur, BlockHeight), (largeur, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="fd4b5-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="fd4b5-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="fd4b5-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="fd4b5-117">Provoque l’interprétation des dizaines d' [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et des [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) avec les dispositions suivantes, où les dimensions entre parenthèses sont aplaties ensemble.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="fd4b5-118">- **Version de profondeur**: [lot, (canaux, BlockHeight, BlockWidth), hauteur, largeur]</span><span class="sxs-lookup"><span data-stu-id="fd4b5-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="fd4b5-119">- **Version d’espace**: [lot, canaux, (hauteur, BlockHeight), (largeur, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="fd4b5-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="fd4b5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd4b5-120">Remarks</span></span>

<span data-ttu-id="fd4b5-121">Pour obtenir des exemples illustrant l’effet de ces valeurs, consultez la documentation [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="fd4b5-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd4b5-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd4b5-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fd4b5-123">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="fd4b5-123">**Header**</span></span> | <span data-ttu-id="fd4b5-124">directml. h</span><span class="sxs-lookup"><span data-stu-id="fd4b5-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="fd4b5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd4b5-125">See also</span></span>

* [<span data-ttu-id="fd4b5-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="fd4b5-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="fd4b5-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="fd4b5-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="fd4b5-128">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="fd4b5-128">Availability</span></span>
<span data-ttu-id="fd4b5-129">Cette énumération a été introduite dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fd4b5-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>