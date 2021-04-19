---
description: Récupère une déclaration décrivant les vertex de la maille.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: 'ID3DXBaseMesh :: GetDeclaration, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f8736e822bfe4a959f35f60bb79783e79f2d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538486"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a><span data-ttu-id="7a01c-103">ID3DXBaseMesh :: GetDeclaration, méthode</span><span class="sxs-lookup"><span data-stu-id="7a01c-103">ID3DXBaseMesh::GetDeclaration method</span></span>

<span data-ttu-id="7a01c-104">Récupère une déclaration décrivant les vertex de la maille.</span><span class="sxs-lookup"><span data-stu-id="7a01c-104">Retrieves a declaration describing the vertices in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a01c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a01c-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="7a01c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a01c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a01c-107">*Déclaration* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="7a01c-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a01c-108">Type : **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="7a01c-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="7a01c-109">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) décrivant le format de vertex des vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="7a01c-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="7a01c-110">La limite supérieure de ce tableau déclarateur est [**la \_ \_ \_ taille maximale**](./max-fvf-decl-size.md)de la déclaration de la Commission de la Commission.</span><span class="sxs-lookup"><span data-stu-id="7a01c-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="7a01c-111">Le tableau d’éléments de vertex se termine par la macro [**\_ end D3DDECL**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="7a01c-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a01c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a01c-112">Return value</span></span>

<span data-ttu-id="7a01c-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a01c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a01c-114">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a01c-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7a01c-115">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7a01c-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a01c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7a01c-116">Remarks</span></span>

<span data-ttu-id="7a01c-117">Le tableau d’éléments comprend la [**macro \_ end D3DDECL**](d3ddecl-end.md) , qui termine la déclaration.</span><span class="sxs-lookup"><span data-stu-id="7a01c-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a01c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a01c-118">Requirements</span></span>



| <span data-ttu-id="7a01c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a01c-119">Requirement</span></span> | <span data-ttu-id="7a01c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a01c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a01c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a01c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7a01c-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a01c-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7a01c-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a01c-123">Library</span></span><br/> | <dl> <span data-ttu-id="7a01c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a01c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a01c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a01c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a01c-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="7a01c-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
