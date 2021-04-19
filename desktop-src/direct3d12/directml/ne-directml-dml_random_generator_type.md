---
UID: NE:directml.DML_RANDOM_GENERATOR_TYPE
title: DML_RANDOM_GENERATOR_TYPE
description: Définit des constantes qui spécifient des types de générateur de nombres aléatoires aléatoires.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_TYPE
- DML_RANDOM_GENERATOR_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_RANDOM_GENERATOR_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_TYPE, DML_RANDOM_GENERATOR_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
- directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
ms.openlocfilehash: bcb79fe7737e8b9ddb461c8da8a901960a4b23f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106538247"
---
# <a name="dml_random_generator_type-enumeration-directmlh"></a><span data-ttu-id="98c64-103">Énumération DML_RANDOM_GENERATOR_TYPE (directml. h)</span><span class="sxs-lookup"><span data-stu-id="98c64-103">DML_RANDOM_GENERATOR_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="98c64-104">Définit des constantes qui spécifient des types de générateur de nombres aléatoires aléatoires.</span><span class="sxs-lookup"><span data-stu-id="98c64-104">Defines constants that specify types of random random-number generator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98c64-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="98c64-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="98c64-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="98c64-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="98c64-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98c64-107">Syntax</span></span>
```cpp
enum DML_RANDOM_GENERATOR_TYPE
{
  DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10
};
```

## <a name="constants"></a><span data-ttu-id="98c64-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="98c64-108">Constants</span></span>

| <span data-ttu-id="98c64-109">Nom</span><span class="sxs-lookup"><span data-stu-id="98c64-109">Name</span></span> | <span data-ttu-id="98c64-110">Description</span><span class="sxs-lookup"><span data-stu-id="98c64-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="98c64-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span><span class="sxs-lookup"><span data-stu-id="98c64-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span></span> | <span data-ttu-id="98c64-112">Spécifie un générateur de nombres pseudo-aléatoires en fonction de l' [algorithme Philox 4x32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span><span class="sxs-lookup"><span data-stu-id="98c64-112">Specifies a generator for pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span> |


## <a name="requirements"></a><span data-ttu-id="98c64-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98c64-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="98c64-114">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="98c64-114">**Header**</span></span> | <span data-ttu-id="98c64-115">directml. h</span><span class="sxs-lookup"><span data-stu-id="98c64-115">directml.h</span></span> |