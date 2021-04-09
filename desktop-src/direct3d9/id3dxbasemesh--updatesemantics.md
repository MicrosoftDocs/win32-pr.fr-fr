---
description: Cette méthode permet à l’utilisateur de modifier la déclaration de maillage sans modifier la disposition des données de la mémoire tampon de vertex. L’appel est valide uniquement si l’ancien et le nouveau format de déclaration ont la même taille de vertex.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh :: UpdateSemantics, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043117"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a><span data-ttu-id="ae873-104">ID3DXBaseMesh :: UpdateSemantics, méthode</span><span class="sxs-lookup"><span data-stu-id="ae873-104">ID3DXBaseMesh::UpdateSemantics method</span></span>

<span data-ttu-id="ae873-105">Cette méthode permet à l’utilisateur de modifier la déclaration de maillage sans modifier la disposition des données de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="ae873-105">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="ae873-106">L’appel est valide uniquement si l’ancien et le nouveau format de déclaration ont la même taille de vertex.</span><span class="sxs-lookup"><span data-stu-id="ae873-106">The call is valid only if the old and new declaration formats have the same vertex size.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae873-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae873-107">Syntax</span></span>


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="ae873-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae873-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae873-109">*Déclaration* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="ae873-109">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae873-110">Type : **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="ae873-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="ae873-111">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le format de vertex des vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="ae873-111">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="ae873-112">La limite supérieure de ce tableau déclarateur est [**la \_ \_ \_ taille maximale**](./max-fvf-decl-size.md)de la déclaration de la Commission de la Commission.</span><span class="sxs-lookup"><span data-stu-id="ae873-112">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae873-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae873-113">Return value</span></span>

<span data-ttu-id="ae873-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae873-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae873-115">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae873-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae873-116">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ae873-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae873-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ae873-117">Remarks</span></span>

<span data-ttu-id="ae873-118">[**ID3DXBaseMesh :: CloneMesh**](id3dxbasemesh--clonemesh.md) est utilisé pour reformater et modifier la disposition des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="ae873-118">[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="ae873-119">Par exemple, utilisez-le pour ajouter de l’espace pour les normales, les coordonnées de texture, les couleurs, les pondérations, etc. qui n’étaient pas déjà présentes.</span><span class="sxs-lookup"><span data-stu-id="ae873-119">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="ae873-120">**ID3DXBaseMesh :: UpdateSemantics** est une méthode permettant de mettre à jour la déclaration de vertex avec des informations sémantiques différentes, sans modifier la disposition de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="ae873-120">**ID3DXBaseMesh::UpdateSemantics** is a method for updating the vertex declaration with different semantic information, without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="ae873-121">Par exemple, utilisez-le pour réétiqueter une coordonnée de texture 3D en tant que biperpendiculaire ou tangente, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="ae873-121">For example, use it to relabel a 3D texture coordinate as a binormal or tangent, or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae873-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae873-122">Requirements</span></span>



| <span data-ttu-id="ae873-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae873-123">Requirement</span></span> | <span data-ttu-id="ae873-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae873-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae873-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae873-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ae873-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae873-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ae873-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae873-127">Library</span></span><br/> | <dl> <span data-ttu-id="ae873-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae873-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae873-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae873-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae873-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="ae873-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="ae873-131">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="ae873-131">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="ae873-132">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="ae873-132">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
