---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compile un graphique d’opérateurs DirectML dans un objet qui peut être distribué au GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803750"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="d2766-103">IDMLDevice1 :: CompileGraph, méthode (directml. h)</span><span class="sxs-lookup"><span data-stu-id="d2766-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="d2766-104">Compile un graphique d’opérateurs DirectML dans un objet qui peut être distribué au GPU.</span><span class="sxs-lookup"><span data-stu-id="d2766-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="d2766-105">Un opérateur compilé représente le formulaire efficace et cuit d’un opérateur apte à être exécuté sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="d2766-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="d2766-106">Un opérateur compilé conserve l’État (par exemple, les nuanceurs et autres objets) requis pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2766-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="d2766-107">Comme un opérateur compilé implémente l’interface [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) , vous êtes en mesure d’en supprimer un de la mémoire du GPU si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="d2766-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="d2766-108">Pour plus d’informations, consultez [IDMLDevice1 :: expulsion](/windows/win32/api/directml/nf-directml-idmldevice-evict) et [IDMLDevice1 :: MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .</span><span class="sxs-lookup"><span data-stu-id="d2766-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="d2766-109">L’opérateur compilé n’utilise pas ni ne référence les objets [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) fournis dans la description du graphique après le retour de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d2766-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2766-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d2766-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d2766-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="d2766-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2766-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2766-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="d2766-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2766-113">Parameters</span></span>

`desc`

<span data-ttu-id="d2766-114">Type : **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2766-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="d2766-115">Description du graphique à compiler.</span><span class="sxs-lookup"><span data-stu-id="d2766-115">A description of the graph to compile.</span></span> <span data-ttu-id="d2766-116">Consultez [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="d2766-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="d2766-117">Type : [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="d2766-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="d2766-118">Indicateurs permettant de contrôler l’exécution de cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="d2766-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="d2766-119">Type : <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="d2766-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="d2766-120">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans <i>PPV</i>.</span><span class="sxs-lookup"><span data-stu-id="d2766-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="d2766-121">Il doit s’agir du GUID de [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span><span class="sxs-lookup"><span data-stu-id="d2766-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="d2766-122">Type : <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="d2766-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="d2766-123">Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’opérateur compilé.</span><span class="sxs-lookup"><span data-stu-id="d2766-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="d2766-124">Il s’agit de l’adresse d’un pointeur vers un [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), représentant l’opérateur compilé créé.</span><span class="sxs-lookup"><span data-stu-id="d2766-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="d2766-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2766-125">Return value</span></span>

<span data-ttu-id="d2766-126">Type : [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d2766-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d2766-127">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="d2766-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d2766-128">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2766-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2766-129">Notes </span><span class="sxs-lookup"><span data-stu-id="d2766-129">Remarks</span></span>

<span data-ttu-id="d2766-130">L’API Graph de l’opérateur DirectML fournit une méthode abstraite pour utiliser efficacement DirectML sur différents matériels.</span><span class="sxs-lookup"><span data-stu-id="d2766-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="d2766-131">DirectML applique des optimisations de niveau tenseur, telles que le choix de la disposition de tenseur la plus efficace en fonction de l’adaptateur utilisé.</span><span class="sxs-lookup"><span data-stu-id="d2766-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="d2766-132">Elle applique également des optimisations telles que la suppression des opérateurs de jointure ou de fractionnement.</span><span class="sxs-lookup"><span data-stu-id="d2766-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="d2766-133">Nous vous recommandons d’appliquer des optimisations de haut niveau avant de générer un graphique DirectML.</span><span class="sxs-lookup"><span data-stu-id="d2766-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="d2766-134">Par exemple, le refus d’opérateurs de convolution avec BatchNorm, le repli de constante et l’élimination commune de sous-expression.</span><span class="sxs-lookup"><span data-stu-id="d2766-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="d2766-135">Les optimisations au sein de l’optimiseur de graphique de DirectML sont destinées à compléter les optimisations indépendantes des appareils, qui sont généralement gérées de façon générique par Machine Learning frameworks.</span><span class="sxs-lookup"><span data-stu-id="d2766-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2766-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d2766-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d2766-137">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="d2766-137">**Target Platform**</span></span> | <span data-ttu-id="d2766-138">Windows</span><span class="sxs-lookup"><span data-stu-id="d2766-138">Windows</span></span> |
| <span data-ttu-id="d2766-139">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="d2766-139">**Header**</span></span> | <span data-ttu-id="d2766-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="d2766-140">directml.h</span></span> |
| <span data-ttu-id="d2766-141">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="d2766-141">**Library**</span></span> | <span data-ttu-id="d2766-142">DirectML. lib</span><span class="sxs-lookup"><span data-stu-id="d2766-142">DirectML.lib</span></span> |
| <span data-ttu-id="d2766-143">**DLL**</span><span class="sxs-lookup"><span data-stu-id="d2766-143">**DLL**</span></span> | <span data-ttu-id="d2766-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="d2766-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="d2766-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2766-145">See also</span></span>

[<span data-ttu-id="d2766-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="d2766-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)