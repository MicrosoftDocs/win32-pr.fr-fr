---
description: Demande la désallocation d’un objet conteneur de maillage.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: ID3DXAllocateHierarchy ::D méthode estroyMeshContainer (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531071"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a><span data-ttu-id="7e0c7-103">ID3DXAllocateHierarchy ::D méthode estroyMeshContainer</span><span class="sxs-lookup"><span data-stu-id="7e0c7-103">ID3DXAllocateHierarchy::DestroyMeshContainer method</span></span>

<span data-ttu-id="7e0c7-104">Demande la désallocation d’un objet conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-104">Requests deallocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e0c7-105">Syntax</span></span>


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a><span data-ttu-id="7e0c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e0c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e0c7-107">*pMeshContainerToFree* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e0c7-107">*pMeshContainerToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0c7-108">Type : **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="7e0c7-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="7e0c7-109">Pointeur vers l’objet conteneur de maillage à désallouer.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-109">Pointer to the mesh container object to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e0c7-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e0c7-110">Return value</span></span>

<span data-ttu-id="7e0c7-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e0c7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e0c7-112">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7e0c7-113">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7e0c7-114">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0c7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e0c7-115">Requirements</span></span>



| <span data-ttu-id="7e0c7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e0c7-116">Requirement</span></span> | <span data-ttu-id="7e0c7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e0c7-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0c7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e0c7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7e0c7-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e0c7-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7e0c7-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7e0c7-120">Library</span></span><br/> | <dl> <span data-ttu-id="7e0c7-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e0c7-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e0c7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e0c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0c7-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="7e0c7-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




