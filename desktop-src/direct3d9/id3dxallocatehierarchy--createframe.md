---
description: Demande l’allocation d’un objet Frame.
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: 'ID3DXAllocateHierarchy :: CreateFrame, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6a3a13dd4d3b3dfaffb26632ff6ad5cc8666f86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539905"
---
# <a name="id3dxallocatehierarchycreateframe-method"></a><span data-ttu-id="7fb25-103">ID3DXAllocateHierarchy :: CreateFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="7fb25-103">ID3DXAllocateHierarchy::CreateFrame method</span></span>

<span data-ttu-id="7fb25-104">Demande l’allocation d’un objet Frame.</span><span class="sxs-lookup"><span data-stu-id="7fb25-104">Requests allocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb25-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fb25-105">Syntax</span></span>


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7fb25-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fb25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fb25-107">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fb25-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb25-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb25-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7fb25-109">Nom du frame à créer.</span><span class="sxs-lookup"><span data-stu-id="7fb25-109">Name of the frame to be created.</span></span>

</dd> <dt>

<span data-ttu-id="7fb25-110">*ppNewFrame* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7fb25-110">*ppNewFrame* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb25-111">Type : **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fb25-111">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="7fb25-112">Retourne l’objet de frame créé.</span><span class="sxs-lookup"><span data-stu-id="7fb25-112">Returns the created frame object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fb25-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fb25-113">Return value</span></span>

<span data-ttu-id="7fb25-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7fb25-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7fb25-115">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="7fb25-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7fb25-116">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7fb25-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7fb25-117">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7fb25-117">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fb25-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fb25-118">Requirements</span></span>



| <span data-ttu-id="7fb25-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fb25-119">Requirement</span></span> | <span data-ttu-id="7fb25-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fb25-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb25-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fb25-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7fb25-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fb25-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7fb25-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7fb25-123">Library</span></span><br/> | <dl> <span data-ttu-id="7fb25-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fb25-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7fb25-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fb25-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb25-126">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="7fb25-126">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
