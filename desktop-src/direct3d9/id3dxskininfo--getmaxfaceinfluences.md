---
description: Obtient le nombre maximal d’influences dans un maillage de triangle avec la mémoire tampon d’index spécifiée.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'ID3DXSkinInfo :: GetMaxFaceInfluences, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394047"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a><span data-ttu-id="6a9b8-103">ID3DXSkinInfo :: GetMaxFaceInfluences, méthode</span><span class="sxs-lookup"><span data-stu-id="6a9b8-103">ID3DXSkinInfo::GetMaxFaceInfluences method</span></span>

<span data-ttu-id="6a9b8-104">Obtient le nombre maximal d’influences dans un maillage de triangle avec la mémoire tampon d’index spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6a9b8-104">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a9b8-105">Syntax</span></span>


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="6a9b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a9b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9b8-107">*PIB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a9b8-107">*pIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9b8-108">Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="6a9b8-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span></span>

<span data-ttu-id="6a9b8-109">Pointeur vers la mémoire tampon d’index qui contient les données d’index de maillage.</span><span class="sxs-lookup"><span data-stu-id="6a9b8-109">Pointer to the index buffer that contains the mesh index data.</span></span>

</dd> <dt>

<span data-ttu-id="6a9b8-110">*NumFaces* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a9b8-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9b8-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a9b8-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a9b8-112">Nombre de visages dans la maille.</span><span class="sxs-lookup"><span data-stu-id="6a9b8-112">Number of faces in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6a9b8-113">*maxFaceInfluences* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a9b8-113">*maxFaceInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9b8-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a9b8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6a9b8-115">Pointeur vers les influences de la face maximale.</span><span class="sxs-lookup"><span data-stu-id="6a9b8-115">Pointer to the maximum face influences.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a9b8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a9b8-116">Return value</span></span>

<span data-ttu-id="6a9b8-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a9b8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a9b8-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a9b8-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a9b8-119">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6a9b8-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a9b8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a9b8-120">Requirements</span></span>



| <span data-ttu-id="6a9b8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a9b8-121">Requirement</span></span> | <span data-ttu-id="6a9b8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a9b8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9b8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a9b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6a9b8-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a9b8-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6a9b8-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a9b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="6a9b8-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a9b8-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a9b8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a9b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9b8-128">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="6a9b8-128">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
