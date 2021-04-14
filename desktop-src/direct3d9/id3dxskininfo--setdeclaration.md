---
description: Définit la déclaration de vertex.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'ID3DXSkinInfo :: SetDeclaration, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322597"
---
# <a name="id3dxskininfosetdeclaration-method"></a><span data-ttu-id="96413-103">ID3DXSkinInfo :: SetDeclaration, méthode</span><span class="sxs-lookup"><span data-stu-id="96413-103">ID3DXSkinInfo::SetDeclaration method</span></span>

<span data-ttu-id="96413-104">Définit la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="96413-104">Sets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="96413-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96413-105">Syntax</span></span>


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="96413-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96413-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96413-107">*pDeclaration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96413-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96413-108">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="96413-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="96413-109">Pointeur vers un tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="96413-109">Pointer to an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96413-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96413-110">Return value</span></span>

<span data-ttu-id="96413-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96413-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96413-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96413-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="96413-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="96413-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="96413-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96413-114">Requirements</span></span>



| <span data-ttu-id="96413-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96413-115">Requirement</span></span> | <span data-ttu-id="96413-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="96413-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96413-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="96413-117">Header</span></span><br/>  | <dl> <span data-ttu-id="96413-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="96413-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="96413-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96413-119">Library</span></span><br/> | <dl> <span data-ttu-id="96413-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96413-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96413-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96413-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96413-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="96413-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="96413-123">**ID3DXSkinInfo::GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="96413-123">**ID3DXSkinInfo::GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




