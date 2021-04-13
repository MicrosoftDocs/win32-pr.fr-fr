---
description: Récupère les coordonnées de texture (u, v) de chaque Texel.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'ID3DXTextureGutterHelper :: GetTexelMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322977"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a><span data-ttu-id="d989c-103">ID3DXTextureGutterHelper :: GetTexelMap, méthode</span><span class="sxs-lookup"><span data-stu-id="d989c-103">ID3DXTextureGutterHelper::GetTexelMap method</span></span>

<span data-ttu-id="d989c-104">Récupère les coordonnées de texture (u, v) de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="d989c-104">Retrieves the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="d989c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d989c-105">Syntax</span></span>


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="d989c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d989c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d989c-107">*pTexelData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d989c-107">*pTexelData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d989c-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d989c-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d989c-109">Pointeur vers l’emplacement, en pixels (u, v), coordonnées de texture où chaque Texel se trouve.</span><span class="sxs-lookup"><span data-stu-id="d989c-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d989c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d989c-110">Return value</span></span>

<span data-ttu-id="d989c-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d989c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d989c-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d989c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d989c-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="d989c-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="d989c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d989c-114">Remarks</span></span>

<span data-ttu-id="d989c-115">Pour les [**texels de classe 2 et 4**](id3dxtexturegutterhelper.md), les coordonnées de texture retournées (u, v) correspondent au point le plus proche sur le triangle le plus proche.</span><span class="sxs-lookup"><span data-stu-id="d989c-115">For [**class 2 and 4 texels**](id3dxtexturegutterhelper.md), the returned (u, v) texture coordinates correspond to the closest point on the closest triangle.</span></span>

<span data-ttu-id="d989c-116">L’application doit allouer et gérer pTexelData.</span><span class="sxs-lookup"><span data-stu-id="d989c-116">The application must allocate and manage pTexelData.</span></span>

## <a name="requirements"></a><span data-ttu-id="d989c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d989c-117">Requirements</span></span>



| <span data-ttu-id="d989c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d989c-118">Requirement</span></span> | <span data-ttu-id="d989c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d989c-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d989c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d989c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d989c-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d989c-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d989c-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d989c-122">Library</span></span><br/> | <dl> <span data-ttu-id="d989c-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d989c-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d989c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d989c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d989c-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="d989c-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




