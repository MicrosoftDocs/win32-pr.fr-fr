---
description: Obtient la déclaration de vertex.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'ID3DXSkinInfo :: GetDeclaration, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322602"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="b74a9-103">ID3DXSkinInfo :: GetDeclaration, méthode</span><span class="sxs-lookup"><span data-stu-id="b74a9-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="b74a9-104">Obtient la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="b74a9-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b74a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b74a9-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="b74a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b74a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b74a9-107">*Déclaration* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="b74a9-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b74a9-108">Type : **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="b74a9-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="b74a9-109">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) décrivant le format de vertex des vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="b74a9-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="b74a9-110">La limite supérieure de ce tableau déclarateur est [**la \_ \_ \_ taille maximale**](./max-fvf-decl-size.md)de la déclaration de la Commission de la Commission.</span><span class="sxs-lookup"><span data-stu-id="b74a9-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="b74a9-111">Le tableau d’éléments de vertex se termine par la macro [**\_ end D3DDECL**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="b74a9-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b74a9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b74a9-112">Return value</span></span>

<span data-ttu-id="b74a9-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b74a9-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b74a9-114">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b74a9-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b74a9-115">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b74a9-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b74a9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b74a9-116">Remarks</span></span>

<span data-ttu-id="b74a9-117">Le tableau d’éléments comprend la [**macro \_ end D3DDECL**](d3ddecl-end.md) , qui termine la déclaration.</span><span class="sxs-lookup"><span data-stu-id="b74a9-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74a9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b74a9-118">Requirements</span></span>



| <span data-ttu-id="b74a9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b74a9-119">Requirement</span></span> | <span data-ttu-id="b74a9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b74a9-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b74a9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b74a9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b74a9-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b74a9-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b74a9-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b74a9-123">Library</span></span><br/> | <dl> <span data-ttu-id="b74a9-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b74a9-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b74a9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b74a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b74a9-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="b74a9-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="b74a9-127">**ID3DXSkinInfo::SetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="b74a9-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
