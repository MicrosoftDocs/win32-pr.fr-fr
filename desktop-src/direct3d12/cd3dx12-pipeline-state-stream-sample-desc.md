---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description d’exemple comme un objet unique approprié pour une description de flux.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538548"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a><span data-ttu-id="39f43-104">\_Exemple de \_ \_ \_ \_ structure DESC de flux d’état de pipeline CD3DX12</span><span class="sxs-lookup"><span data-stu-id="39f43-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC structure</span></span>

<span data-ttu-id="39f43-105">Structure d’assistance utilisée pour décrire une description d’exemple comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="39f43-105">A helper structure used to describe a sample description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f43-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39f43-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="39f43-107">Membres</span><span class="sxs-lookup"><span data-stu-id="39f43-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="39f43-108">**\_Exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="39f43-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="39f43-109">Crée une nouvelle instance non initialisée d’un \_ exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="39f43-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="39f43-110">**\_ \_ Exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ desc ( \_ exemple dxgi \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="39f43-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC(DXGI\_SAMPLE\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="39f43-111">Crée une nouvelle instance d’un \_ exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc, initialisé avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure d' [**\_ exemple \_ desc de dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="39f43-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_DESC** and subobject data copied from *i*, a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="39f43-112">**Operator = ( \_ exemple dxgi \_ desc const& i)**</span><span class="sxs-lookup"><span data-stu-id="39f43-112">**operator=(DXGI\_SAMPLE\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="39f43-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="39f43-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="39f43-114">**exemple DXGI \_ \_ desc () const, opérateur**</span><span class="sxs-lookup"><span data-stu-id="39f43-114">**operator DXGI\_SAMPLE\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="39f43-115">Conversion implicite en une structure d' [**\_ exemple \_ desc dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="39f43-115">Implicit conversion to a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39f43-116">Notes</span><span class="sxs-lookup"><span data-stu-id="39f43-116">Remarks</span></span>

<span data-ttu-id="39f43-117">\_ \_ \_ \_ L’exemple de flux d’état de pipeline CD3DX12 \_ desc est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="39f43-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="39f43-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39f43-118">Requirements</span></span>



| <span data-ttu-id="39f43-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39f43-119">Requirement</span></span> | <span data-ttu-id="39f43-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="39f43-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39f43-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="39f43-121">Header</span></span><br/> | <dl> <span data-ttu-id="39f43-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="39f43-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f43-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39f43-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f43-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="39f43-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="39f43-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="39f43-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="39f43-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="39f43-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

