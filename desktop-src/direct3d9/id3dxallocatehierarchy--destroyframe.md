---
description: Demande la désallocation d’un objet Frame.
ms.assetid: b2793744-1bba-4a2b-938c-44ed316358fd
title: ID3DXAllocateHierarchy ::D méthode estroyFrame (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4a394501b9967d3f7cb6d3f6b2f30db168438278
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394243"
---
# <a name="id3dxallocatehierarchydestroyframe-method"></a><span data-ttu-id="20a66-103">ID3DXAllocateHierarchy ::D méthode estroyFrame</span><span class="sxs-lookup"><span data-stu-id="20a66-103">ID3DXAllocateHierarchy::DestroyFrame method</span></span>

<span data-ttu-id="20a66-104">Demande la désallocation d’un objet Frame.</span><span class="sxs-lookup"><span data-stu-id="20a66-104">Requests deallocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20a66-105">Syntax</span></span>


```C++
HRESULT DestroyFrame(
  [in] LPD3DXFRAME pFrameToFree
);
```



## <a name="parameters"></a><span data-ttu-id="20a66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20a66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a66-107">*pFrameToFree* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20a66-107">*pFrameToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20a66-108">Type : **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="20a66-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="20a66-109">Pointeur vers le frame à désallouer.</span><span class="sxs-lookup"><span data-stu-id="20a66-109">Pointer to the frame to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a66-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20a66-110">Return value</span></span>

<span data-ttu-id="20a66-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20a66-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20a66-112">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="20a66-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="20a66-113">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20a66-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="20a66-114">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="20a66-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="20a66-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a66-115">Requirements</span></span>



| <span data-ttu-id="20a66-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20a66-116">Requirement</span></span> | <span data-ttu-id="20a66-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="20a66-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20a66-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="20a66-118">Header</span></span><br/>  | <dl> <span data-ttu-id="20a66-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="20a66-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="20a66-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20a66-120">Library</span></span><br/> | <dl> <span data-ttu-id="20a66-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20a66-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20a66-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a66-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a66-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="20a66-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




