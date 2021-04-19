---
description: Crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: D3DX10CreateSkinInfo, fonction (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a68da20c2e2e15e3b73d55ee1df70518bba46200
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532470"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="c3984-103">D3DX10CreateSkinInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="c3984-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="c3984-104">Crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.</span><span class="sxs-lookup"><span data-stu-id="c3984-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3984-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3984-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c3984-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3984-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3984-107">*ppSkinInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3984-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3984-108">Type : **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3984-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="c3984-109">Adresse d’un pointeur vers une [**interface ID3DX10SkinInfo**](id3dx10skininfo.md)représentant l’objet de maillage d’apparence créé.</span><span class="sxs-lookup"><span data-stu-id="c3984-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3984-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3984-110">Return value</span></span>

<span data-ttu-id="c3984-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3984-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3984-112">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3984-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3984-113">Si la fonction échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c3984-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3984-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c3984-114">Remarks</span></span>

<span data-ttu-id="c3984-115">Utilisez [**ID3DX10SkinInfo :: SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) pour remplir l’objet de maillage d’apparence vide retourné par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c3984-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3984-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3984-116">Requirements</span></span>



| <span data-ttu-id="c3984-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3984-117">Requirement</span></span> | <span data-ttu-id="c3984-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3984-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3984-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3984-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c3984-120"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3984-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c3984-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3984-121">Library</span></span><br/> | <dl> <span data-ttu-id="c3984-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3984-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3984-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3984-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3984-124">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="c3984-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="c3984-125">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="c3984-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




