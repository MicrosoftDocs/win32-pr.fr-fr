---
description: Définit les coordonnées de texture (u, v) de chaque Texel.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'ID3DXTextureGutterHelper :: SetTexelMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532476"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a><span data-ttu-id="3f6b4-103">ID3DXTextureGutterHelper :: SetTexelMap, méthode</span><span class="sxs-lookup"><span data-stu-id="3f6b4-103">ID3DXTextureGutterHelper::SetTexelMap method</span></span>

<span data-ttu-id="3f6b4-104">Définit les coordonnées de texture (u, v) de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="3f6b4-104">Sets the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f6b4-105">Syntax</span></span>


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="3f6b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f6b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f6b4-107">*pTexelData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f6b4-107">*pTexelData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6b4-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f6b4-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3f6b4-109">Pointeur vers l’emplacement, en pixels (u, v), coordonnées de texture où chaque Texel se trouve.</span><span class="sxs-lookup"><span data-stu-id="3f6b4-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f6b4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f6b4-110">Return value</span></span>

<span data-ttu-id="3f6b4-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f6b4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f6b4-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f6b4-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3f6b4-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="3f6b4-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="3f6b4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f6b4-114">Requirements</span></span>



| <span data-ttu-id="3f6b4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f6b4-115">Requirement</span></span> | <span data-ttu-id="3f6b4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f6b4-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6b4-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f6b4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3f6b4-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f6b4-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3f6b4-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f6b4-119">Library</span></span><br/> | <dl> <span data-ttu-id="3f6b4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f6b4-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f6b4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f6b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f6b4-122">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="3f6b4-122">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




