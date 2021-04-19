---
title: CommandListCast, fonction (D3dx12. h)
description: Ce modèle de fonction convertit un pointeur constant en une liste de commandes en pointeur const vers un ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- CommandListCast fonction)
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539913"
---
# <a name="commandlistcast-function"></a><span data-ttu-id="eee25-104">CommandListCast fonction)</span><span class="sxs-lookup"><span data-stu-id="eee25-104">CommandListCast function</span></span>

<span data-ttu-id="eee25-105">Ce modèle de fonction convertit un pointeur constant en une liste de commandes en pointeur const vers un ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="eee25-105">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span>

<span data-ttu-id="eee25-106">Ce cast est utile pour passer des pointeurs de liste de commandes fortement typés dans [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="eee25-106">This cast is useful for passing strongly-typed command list pointers into [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>

## <a name="syntax"></a><span data-ttu-id="eee25-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eee25-107">Syntax</span></span>


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a><span data-ttu-id="eee25-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eee25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eee25-109">*p*</span><span class="sxs-lookup"><span data-stu-id="eee25-109">*pp*</span></span> 
</dt> <dd>

<span data-ttu-id="eee25-110">Type : **t \_ CommandListType \* \* const**</span><span class="sxs-lookup"><span data-stu-id="eee25-110">Type: **t\_CommandListType \* const \***</span></span>

<span data-ttu-id="eee25-111">Liste de commandes fortement typée à convertir.</span><span class="sxs-lookup"><span data-stu-id="eee25-111">The strongly-typed command list to cast.</span></span>

<span data-ttu-id="eee25-112">L’argument de modèle **t \_ CommandListType** spécifie un objet de liste de commandes fortement typé.</span><span class="sxs-lookup"><span data-stu-id="eee25-112">The template argument **t\_CommandListType** specifies any strongly-typed command list object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eee25-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eee25-113">Return value</span></span>

<span data-ttu-id="eee25-114">Type : **ID3D12CommandList \* const \***</span><span class="sxs-lookup"><span data-stu-id="eee25-114">Type: **ID3D12CommandList \* const \***</span></span>

<span data-ttu-id="eee25-115">Liste de commandes fortement typées, réinterprétée comme un [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="eee25-115">The strongly-typed command list, reinterpreted as an [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>

## <a name="remarks"></a><span data-ttu-id="eee25-116">Notes</span><span class="sxs-lookup"><span data-stu-id="eee25-116">Remarks</span></span>

<span data-ttu-id="eee25-117">CommandListCast effectue un **\_ cast de réinterprétation**.</span><span class="sxs-lookup"><span data-stu-id="eee25-117">CommandListCast performs a **reinterpret\_cast**.</span></span> <span data-ttu-id="eee25-118">Le cast est valide tant que le caractère const de la liste de commandes est respecté.</span><span class="sxs-lookup"><span data-stu-id="eee25-118">The cast is valid as long as the const-ness of the command list is respected.</span></span>

<span data-ttu-id="eee25-119">La fonction CommandListCast est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="eee25-119">The CommandListCast function is defined as the following:</span></span>


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a><span data-ttu-id="eee25-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eee25-120">Requirements</span></span>



| <span data-ttu-id="eee25-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eee25-121">Requirement</span></span> | <span data-ttu-id="eee25-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="eee25-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eee25-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="eee25-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eee25-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee25-124"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="eee25-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eee25-125">Library</span></span><br/> | <dl> <span data-ttu-id="eee25-126"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eee25-126"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="eee25-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eee25-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="eee25-128"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eee25-128"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee25-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eee25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee25-130">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="eee25-130">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





