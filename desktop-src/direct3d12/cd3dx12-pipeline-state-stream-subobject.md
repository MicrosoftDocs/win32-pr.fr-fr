---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12. h)
description: Structure d’assistance basée sur un modèle utilisée pour encapsuler le type de sous-objet et les paires de données de sous-objet en tant qu’objet unique approprié pour une description de flux.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539478"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a><span data-ttu-id="99cb4-104">CD3DX12 structure de sous- \_ objet du flux d’État du pipeline \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="99cb4-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT structure</span></span>

<span data-ttu-id="99cb4-105">Structure d’assistance basée sur un modèle utilisée pour encapsuler le type de sous-objet et les paires de données de sous-objet en tant qu’objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="99cb4-105">A templated helper structure used to encapsulate subobject type and subobject data pairs as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="99cb4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99cb4-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a><span data-ttu-id="99cb4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="99cb4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="99cb4-108">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="99cb4-109">Crée une nouvelle instance non initialisée d’un sous- \_ objet de flux d’état de pipeline CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="99cb4-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT.</span></span>

</dd> <dt>

<span data-ttu-id="99cb4-110">**CD3DX12 \_ \_Sous- \_ \_ objet de flux d’État du pipeline (** InnerStructType \* \* const &i) \* \*</span><span class="sxs-lookup"><span data-stu-id="99cb4-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT(** InnerStructType\*\* const &i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="99cb4-111">Crée une instance de \_ modèle de sous-objet de flux d’état de pipeline CD3DX12 \_ \_ \_ , initialisée avec un type de sous-objet de [**type de sous-objet d’état de pipeline D3D12 et des données de \_ \_ \_ \_ sous**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) -objet copiées à partir de *i*.</span><span class="sxs-lookup"><span data-stu-id="99cb4-111">Creates a new CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template instance, initialized with a subobject type of [**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) and subobject data copied from *i*.</span></span> <span data-ttu-id="99cb4-112">Le type de sous-objet et le type de données de sous-objet sont spécifiés en tant que paramètres de modèle, **type** et **InnerStructType**, respectivement.</span><span class="sxs-lookup"><span data-stu-id="99cb4-112">Both the subobject type and subobject data type are given as template parameters, **Type** and **InnerStructType**, respectively.</span></span> <span data-ttu-id="99cb4-113">Pour plus d’informations, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="99cb4-113">For more information, see Remarks below.</span></span>

</dd> <dt>

<span data-ttu-id="99cb4-114">**opérateur = (** InnerStructType \* \* const& i) \* \*</span><span class="sxs-lookup"><span data-stu-id="99cb4-114">**operator=(** InnerStructType\*\* const& i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="99cb4-115">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="99cb4-115">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="99cb4-116">**const, opérateur **InnerStructType**()**</span><span class="sxs-lookup"><span data-stu-id="99cb4-116">**operator **InnerStructType**() const**</span></span>
</dt> <dd>

<span data-ttu-id="99cb4-117">Conversion implicite vers le type de données de sous-objet donné par le paramètre de modèle **InnerStructType** .</span><span class="sxs-lookup"><span data-stu-id="99cb4-117">Implicit conversion to the subobject data type given by the **InnerStructType** template parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99cb4-118">Notes</span><span class="sxs-lookup"><span data-stu-id="99cb4-118">Remarks</span></span>

<span data-ttu-id="99cb4-119">\_ \_ \_ Le sous-objet de flux d’État du pipeline CD3DX12 \_ est un modèle défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="99cb4-119">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT is a template defined as follows:</span></span>


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



<span data-ttu-id="99cb4-120">Le paramètre de modèle **InnerStructType** spécifie le type de données de sous-objet ; autrement dit, les détails du sous-objet à encoder dans un flux.</span><span class="sxs-lookup"><span data-stu-id="99cb4-120">The template parameter **InnerStructType** specifies the subobject data type; that is, the subobject details to be encoded into a stream.</span></span> <span data-ttu-id="99cb4-121">Le **type** de paramètre de modèle spécifie le type de sous-objet. autrement dit, le type de la structure spécifiée par le paramètre de modèle **InnerStructType**.</span><span class="sxs-lookup"><span data-stu-id="99cb4-121">The template parameter **Type** specifies the subobject type; that is, the type of the structure specified by the template parameter **InnerStructType**.</span></span> <span data-ttu-id="99cb4-122">Le paramètre de modèle **defaultArg (** spécifie une valeur facultative à laquelle les données de sous-objet sont initialisées lorsqu’une instance de l’instanciation de modèle correspondante est construite par défaut ; par exemple, pour construire par défaut un [**flux d’état de pipeline CD3DX12, le \_ \_ \_ \_ \_ desc fusionné**](cd3dx12-pipeline-state-stream-blend-desc.md) est initialisé avec les valeurs par défaut d’état de fusion communes à l’aide de [**CD3DX12 \_ par défaut**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="99cb4-122">The template parameter **DefaultArg** specifies an optional value that the subobject data will be initialized to when an instance of the corresponding template instantiation is default-constructed; for example, to default-construct a [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) initialized with common blend-state defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

<span data-ttu-id="99cb4-123">Voici les instanciations de modèle définies :</span><span class="sxs-lookup"><span data-stu-id="99cb4-123">Here are the template instantiations that are defined:</span></span>

-   [<span data-ttu-id="99cb4-124">**\_Indicateurs du \_ flux d’État du PIPELINe CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-124">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>](cd3dx12-pipeline-state-stream-flags.md)
-   [<span data-ttu-id="99cb4-125">**\_Masque de \_ \_ nœud du flux d’État du pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-node-mask.md)
-   [<span data-ttu-id="99cb4-126">**\_ \_ \_ Signature racine du flux d’état \_ du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>](cd3dx12-pipeline-state-stream-root-signature.md)
-   [<span data-ttu-id="99cb4-127">**\_ \_ \_ \_ Disposition d’entrée de flux d’état de pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-127">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>](cd3dx12-pipeline-state-stream-input-layout.md)
-   [<span data-ttu-id="99cb4-128">**CD3DX12 de \_ flux d’état de pipeline \_ IB- \_ \_ \_ \_ valeur de coupe \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-128">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [<span data-ttu-id="99cb4-129">**\_ \_ \_ Topologie primitive du flux d’état \_ du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-129">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [<span data-ttu-id="99cb4-130">**\_Flux d’état de pipeline CD3DX12 \_ \_ \_ et**</span><span class="sxs-lookup"><span data-stu-id="99cb4-130">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>](cd3dx12-pipeline-state-stream-vs.md)
-   [<span data-ttu-id="99cb4-131">**\_Flux d’état de pipeline CD3DX12 \_ \_ \_ GS**</span><span class="sxs-lookup"><span data-stu-id="99cb4-131">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>](cd3dx12-pipeline-state-stream-gs.md)
-   [<span data-ttu-id="99cb4-132">**Sortie du flux de flux d' \_ État du pipeline CD3DX12 \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-132">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>](cd3dx12-pipeline-state-stream-stream-output.md)
-   [<span data-ttu-id="99cb4-133">**CD3DX12 de \_ flux d’État du pipeline \_ \_ \_ HS**</span><span class="sxs-lookup"><span data-stu-id="99cb4-133">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>](cd3dx12-pipeline-state-stream-hs.md)
-   [<span data-ttu-id="99cb4-134">**CD3DX12 \_ de \_ flux d’État du pipeline \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-134">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>](cd3dx12-pipeline-state-stream-ds.md)
-   [<span data-ttu-id="99cb4-135">**\_Flux d’État du pipeline CD3DX12 \_ \_ \_ PS**</span><span class="sxs-lookup"><span data-stu-id="99cb4-135">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>](cd3dx12-pipeline-state-stream-ps.md)
-   [<span data-ttu-id="99cb4-136">**\_Flux d’État du pipeline CD3DX12 \_ \_ \_ CS**</span><span class="sxs-lookup"><span data-stu-id="99cb4-136">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>](cd3dx12-pipeline-state-stream-cs.md)
-   [<span data-ttu-id="99cb4-137">**\_ \_ \_ \_ Mélange DESC du flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-137">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [<span data-ttu-id="99cb4-138">**\_Stencil de \_ \_ profondeur du flux d’État du pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-138">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [<span data-ttu-id="99cb4-139">**\_Profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="99cb4-139">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [<span data-ttu-id="99cb4-140">**\_Format du \_ \_ stencil de profondeur du flux d’État du \_ \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-140">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [<span data-ttu-id="99cb4-141">**\_Rastériseur de \_ flux d’état de PIPELINe CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-141">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [<span data-ttu-id="99cb4-142">**\_ \_ \_ \_ Formats cibles de rendu du flux d' \_ état \_ du pipeline CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="99cb4-142">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [<span data-ttu-id="99cb4-143">**\_Exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="99cb4-143">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [<span data-ttu-id="99cb4-144">**\_Exemple de \_ masque de \_ flux d’état de \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-144">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [<span data-ttu-id="99cb4-145">**\_Flux d' \_ État du pipeline CD3DX12 \_ \_ mis en cache \_**</span><span class="sxs-lookup"><span data-stu-id="99cb4-145">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>](cd3dx12-pipeline-state-stream-cached-pso.md)

<span data-ttu-id="99cb4-146">Le CD3DX12 de pipeline d’état de pipeline [**\_ \_ \_ \_ \_ desc**](cd3dx12-pipeline-state-stream-blend-desc.md), le [**\_ \_ \_ \_ \_ stencil de profondeur**](cd3dx12-pipeline-state-stream-depth-stencil.md)de flux d’état de pipeline CD3DX12, les structures de de flux d’état de [**\_ pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)et les structures de rastérisation de [**flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-rasterizer.md) sont définis pour initialiser leurs données de sous-objet avec les valeurs par défaut communes utilisant [**CD3DX12 \_ par défaut**](cd3dx12-default.md)</span><span class="sxs-lookup"><span data-stu-id="99cb4-146">The [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md), and [**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) structures are defined to initialize their subobject data with common defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99cb4-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99cb4-147">Requirements</span></span>



| <span data-ttu-id="99cb4-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99cb4-148">Requirement</span></span> | <span data-ttu-id="99cb4-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="99cb4-149">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99cb4-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="99cb4-150">Header</span></span><br/> | <dl> <span data-ttu-id="99cb4-151"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="99cb4-151"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99cb4-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99cb4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99cb4-153">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="99cb4-153">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="99cb4-154">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="99cb4-154">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

