---
description: Définit l’index du type de maillage auquel appartient chaque Texel.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'ID3DXTextureGutterHelper :: SetFaceMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211905"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a><span data-ttu-id="e916b-103">ID3DXTextureGutterHelper :: SetFaceMap, méthode</span><span class="sxs-lookup"><span data-stu-id="e916b-103">ID3DXTextureGutterHelper::SetFaceMap method</span></span>

<span data-ttu-id="e916b-104">Définit l’index du type de maillage auquel appartient chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="e916b-104">Sets the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e916b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e916b-105">Syntax</span></span>


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="e916b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e916b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e916b-107">*pFaceData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e916b-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e916b-108">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e916b-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e916b-109">Pointeur vers l’index du type de maillage auquel appartient chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="e916b-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e916b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e916b-110">Return value</span></span>

<span data-ttu-id="e916b-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e916b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e916b-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e916b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e916b-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="e916b-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="e916b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e916b-114">Remarks</span></span>

<span data-ttu-id="e916b-115">L’entrée de données de la maille de cette méthode est valide uniquement pour les texels valides (non de classe 0).</span><span class="sxs-lookup"><span data-stu-id="e916b-115">The mesh face data input to this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="e916b-116">[**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides.</span><span class="sxs-lookup"><span data-stu-id="e916b-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="e916b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e916b-117">Requirements</span></span>



| <span data-ttu-id="e916b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e916b-118">Requirement</span></span> | <span data-ttu-id="e916b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e916b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e916b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e916b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e916b-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e916b-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e916b-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e916b-122">Library</span></span><br/> | <dl> <span data-ttu-id="e916b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e916b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e916b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e916b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e916b-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="e916b-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
