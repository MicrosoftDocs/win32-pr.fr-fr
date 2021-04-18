---
description: Obtient les attributs du correctif.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh :: GetPatchInfo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522602"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a><span data-ttu-id="723c7-103">ID3DXPatchMesh :: GetPatchInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="723c7-103">ID3DXPatchMesh::GetPatchInfo method</span></span>

<span data-ttu-id="723c7-104">Obtient les attributs du correctif.</span><span class="sxs-lookup"><span data-stu-id="723c7-104">Gets the attributes of the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="723c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="723c7-105">Syntax</span></span>


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a><span data-ttu-id="723c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="723c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="723c7-107">*PatchInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="723c7-107">*PatchInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="723c7-108">Type : **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="723c7-108">Type: **[**LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span></span>

<span data-ttu-id="723c7-109">Pointeur vers les structures contenant les attributs de correctif.</span><span class="sxs-lookup"><span data-stu-id="723c7-109">Pointer to the structures containing the patch attributes.</span></span> <span data-ttu-id="723c7-110">Pour plus d’informations sur les attributs de correctif, consultez [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="723c7-110">For more information about patch attributes, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="723c7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="723c7-111">Return value</span></span>

<span data-ttu-id="723c7-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="723c7-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="723c7-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="723c7-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="723c7-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="723c7-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="723c7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="723c7-115">Requirements</span></span>



| <span data-ttu-id="723c7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="723c7-116">Requirement</span></span> | <span data-ttu-id="723c7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="723c7-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="723c7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="723c7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="723c7-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="723c7-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="723c7-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="723c7-120">Library</span></span><br/> | <dl> <span data-ttu-id="723c7-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="723c7-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="723c7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="723c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723c7-123">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="723c7-123">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




