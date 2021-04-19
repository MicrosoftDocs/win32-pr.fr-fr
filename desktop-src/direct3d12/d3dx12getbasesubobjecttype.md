---
title: D3DX12GetBaseSubobjectType, fonction (D3dx12. h)
description: Retourne le type de sous-objet qui correspond à la classe de base du type de sous-objet passé.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType fonction)
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532421"
---
# <a name="d3dx12getbasesubobjecttype-function"></a><span data-ttu-id="c3edb-104">D3DX12GetBaseSubobjectType fonction)</span><span class="sxs-lookup"><span data-stu-id="c3edb-104">D3DX12GetBaseSubobjectType function</span></span>

<span data-ttu-id="c3edb-105">Retourne le type de sous-objet qui correspond à la classe de base du type de sous-objet passé.</span><span class="sxs-lookup"><span data-stu-id="c3edb-105">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3edb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3edb-106">Syntax</span></span>


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a><span data-ttu-id="c3edb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3edb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3edb-108">*SubobjectType*</span><span class="sxs-lookup"><span data-stu-id="c3edb-108">*SubobjectType*</span></span> 
</dt> <dd>

<span data-ttu-id="c3edb-109">Type : **\_ type de \_ \_ \_ sous-objet état du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="c3edb-109">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="c3edb-110">Valeur d’énumération qui spécifie le type de sous-objet qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="c3edb-110">An enumeration value that specifies the subobject type that you're interested in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3edb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3edb-111">Return value</span></span>

<span data-ttu-id="c3edb-112">Type : **\_ type de \_ \_ \_ sous-objet état du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="c3edb-112">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="c3edb-113">Si *SubobjectType* correspond à un type de données de sous-objet dérivé d’un autre type de données de sous-objet, le type de sous-objet du type de données de sous-objet de base est retourné ; dans le cas contraire, le type de sous-objet passé est retourné.</span><span class="sxs-lookup"><span data-stu-id="c3edb-113">If *SubobjectType* corresponds to a subobject data type that is derived from another subobject data type, the subobject type of the base subobject data type is returned; otherwise, the passed-in subobject type is returned.</span></span> <span data-ttu-id="c3edb-114">Par exemple, si la profondeur de type de sous-objet de l' **État du \_ pipeline D3D12 \_ \_ \_ \_ \_ STENCIL1** est passée, le stencil de profondeur du type de sous-objet de l' **\_ État du pipeline \_ \_ \_ \_ \_ D3D12** est retourné.</span><span class="sxs-lookup"><span data-stu-id="c3edb-114">For example, if **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** is passed in, then **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3edb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c3edb-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c3edb-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c3edb-116">Requirements</span></span>



| <span data-ttu-id="c3edb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3edb-117">Requirement</span></span> | <span data-ttu-id="c3edb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3edb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3edb-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3edb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c3edb-120"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3edb-120"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c3edb-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3edb-121">Library</span></span><br/> | <dl> <span data-ttu-id="c3edb-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3edb-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c3edb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c3edb-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3edb-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3edb-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3edb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3edb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3edb-126">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="c3edb-126">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





