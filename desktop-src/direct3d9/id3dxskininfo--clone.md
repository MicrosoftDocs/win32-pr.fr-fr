---
description: Clone un objet d’informations d’apparence.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'ID3DXSkinInfo :: Clone, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211731"
---
# <a name="id3dxskininfoclone-method"></a><span data-ttu-id="3ebf5-103">ID3DXSkinInfo :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="3ebf5-103">ID3DXSkinInfo::Clone method</span></span>

<span data-ttu-id="3ebf5-104">Clone un objet d’informations d’apparence.</span><span class="sxs-lookup"><span data-stu-id="3ebf5-104">Clones a skin info object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebf5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ebf5-105">Syntax</span></span>


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3ebf5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ebf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ebf5-107">*ppSkinInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3ebf5-107">*ppSkinInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ebf5-108">Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ebf5-108">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="3ebf5-109">Adresse d’un pointeur vers un objet [**ID3DXSkinInfo**](id3dxskininfo.md) , qui contient l’objet cloné si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="3ebf5-109">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) object, which will contain the cloned object if the method is successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ebf5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ebf5-110">Return value</span></span>

<span data-ttu-id="3ebf5-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ebf5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ebf5-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ebf5-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3ebf5-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3ebf5-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ebf5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ebf5-114">Requirements</span></span>



| <span data-ttu-id="3ebf5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ebf5-115">Requirement</span></span> | <span data-ttu-id="3ebf5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ebf5-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebf5-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ebf5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3ebf5-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ebf5-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3ebf5-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3ebf5-119">Library</span></span><br/> | <dl> <span data-ttu-id="3ebf5-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ebf5-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ebf5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ebf5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebf5-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="3ebf5-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 




