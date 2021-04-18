---
title: Structure CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de tableau de \_ format D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Structure CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536448"
---
# <a name="cd3dx12_rt_format_array-structure"></a><span data-ttu-id="07d58-104">\_Structure de \_ tableau de format CD3DX12 RT \_</span><span class="sxs-lookup"><span data-stu-id="07d58-104">CD3DX12\_RT\_FORMAT\_ARRAY structure</span></span>

<span data-ttu-id="07d58-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ tableau de \_ format \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="07d58-105">A helper structure to enable easy initialization of a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d58-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07d58-106">Syntax</span></span>


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a><span data-ttu-id="07d58-107">Membres</span><span class="sxs-lookup"><span data-stu-id="07d58-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="07d58-108">**\_ \_ Tableau de format CD3DX12 RT \_ ()**</span><span class="sxs-lookup"><span data-stu-id="07d58-108">**CD3DX12\_RT\_FORMAT\_ARRAY()**</span></span>
</dt> <dd>

<span data-ttu-id="07d58-109">Crée une nouvelle instance non initialisée d’un \_ tableau de format CD3DX12 \_ RT \_ .</span><span class="sxs-lookup"><span data-stu-id="07d58-109">Creates a new, uninitialized, instance of a CD3DX12\_RT\_FORMAT\_ARRAY.</span></span>

</dd> <dt>

<span data-ttu-id="07d58-110">**\_ \_ tableau de format CD3DX12 RT explicite \_ (const D3D12 \_ RT \_ format \_ tableau& o)**</span><span class="sxs-lookup"><span data-stu-id="07d58-110">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const D3D12\_RT\_FORMAT\_ARRAY& o)**</span></span>
</dt> <dd>

<span data-ttu-id="07d58-111">Crée une nouvelle instance d’un \_ tableau de format CD3DX12 RT \_ \_ , initialisée avec les valeurs copiées à partir d’une structure de [**\_ \_ \_ tableau de format D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="07d58-111">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with values copied from a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="07d58-112">**\_ \_ tableau de format CD3DX12 RT explicite \_ (const dxgi \_ format \* pFormats, uint NumFormats)**</span><span class="sxs-lookup"><span data-stu-id="07d58-112">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const DXGI\_FORMAT\* pFormats, UINT NumFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="07d58-113">Crée une nouvelle instance d’un \_ tableau de format CD3DX12 RT \_ \_ , initialisée avec les valeurs passées dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="07d58-113">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with the values passed in the parameter list.</span></span> <span data-ttu-id="07d58-114">Le contenu du tableau spécifié par le paramètre *pFormats* est copié dans le tableau de membres **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="07d58-114">Contents of the array specified by the *pFormats* parameter are copied into the member array **RTFormats**.</span></span> <span data-ttu-id="07d58-115">Le tableau spécifié par *pFormats* est supposé avoir la même taille que **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="07d58-115">The array specified by *pFormats* is assumed to have the same size as **RTFormats**.</span></span>

</dd> <dt>

<span data-ttu-id="07d58-116">**const D3D12 \_ RT \_ FORMAT \_ tableau& () const**</span><span class="sxs-lookup"><span data-stu-id="07d58-116">**operator const D3D12\_RT\_FORMAT\_ARRAY&() const**</span></span>
</dt> <dd>

<span data-ttu-id="07d58-117">Conversion implicite en structure de [**\_ tableau de \_ format \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="07d58-117">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span> <span data-ttu-id="07d58-118">Étant donné \_ que \_ \_ le tableau de format D3D12 RT est le type sous-jacent de \_ stencil de profondeur CD3DX12 \_ \_ DESC1, l’objet est simplement retourné en tant que référence de tableau de format const D3D12 \_ RT \_ \_ à lui-même.</span><span class="sxs-lookup"><span data-stu-id="07d58-118">Because D3D12\_RT\_FORMAT\_ARRAY is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_RT\_FORMAT\_ARRAY reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07d58-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07d58-119">Requirements</span></span>



| <span data-ttu-id="07d58-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07d58-120">Requirement</span></span> | <span data-ttu-id="07d58-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="07d58-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07d58-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="07d58-122">Header</span></span><br/> | <dl> <span data-ttu-id="07d58-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d58-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d58-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07d58-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d58-125">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="07d58-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="07d58-126">**\_Tableau de \_ format D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="07d58-126">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





