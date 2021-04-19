---
description: Récupère l’index du type de maillage auquel appartient chaque Texel.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'ID3DXTextureGutterHelper :: GetFaceMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535824"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a><span data-ttu-id="5f2cb-103">ID3DXTextureGutterHelper :: GetFaceMap, méthode</span><span class="sxs-lookup"><span data-stu-id="5f2cb-103">ID3DXTextureGutterHelper::GetFaceMap method</span></span>

<span data-ttu-id="5f2cb-104">Récupère l’index du type de maillage auquel appartient chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="5f2cb-104">Retrieves the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f2cb-105">Syntax</span></span>


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="5f2cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f2cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f2cb-107">*pFaceData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f2cb-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2cb-108">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f2cb-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5f2cb-109">Pointeur vers l’index du type de maillage auquel appartient chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="5f2cb-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f2cb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f2cb-110">Return value</span></span>

<span data-ttu-id="5f2cb-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f2cb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f2cb-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5f2cb-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5f2cb-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="5f2cb-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="5f2cb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5f2cb-114">Remarks</span></span>

<span data-ttu-id="5f2cb-115">Les données de la maille retournées par cette méthode sont valides uniquement pour les texels valides (non de classe 0).</span><span class="sxs-lookup"><span data-stu-id="5f2cb-115">The mesh face data returned by this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="5f2cb-116">[**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides (non de classe 0).</span><span class="sxs-lookup"><span data-stu-id="5f2cb-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid (non-class 0) texels.</span></span>

<span data-ttu-id="5f2cb-117">Pour les [**texels de classe 2**](id3dxtexturegutterhelper.md), cette méthode récupère la face la plus proche.</span><span class="sxs-lookup"><span data-stu-id="5f2cb-117">For [**class 2 texels**](id3dxtexturegutterhelper.md), this method retrieves the closest face.</span></span>

<span data-ttu-id="5f2cb-118">L’application doit allouer et gérer pFaceData.</span><span class="sxs-lookup"><span data-stu-id="5f2cb-118">The application must allocate and manage pFaceData.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2cb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f2cb-119">Requirements</span></span>



| <span data-ttu-id="5f2cb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f2cb-120">Requirement</span></span> | <span data-ttu-id="5f2cb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f2cb-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2cb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f2cb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5f2cb-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f2cb-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5f2cb-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f2cb-124">Library</span></span><br/> | <dl> <span data-ttu-id="5f2cb-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f2cb-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f2cb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f2cb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2cb-127">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="5f2cb-127">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
