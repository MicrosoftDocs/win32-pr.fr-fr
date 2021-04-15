---
description: Définit un entier.
ms.assetid: 1090d4a6-b4f5-4e15-a49f-e2724f1c3f95
title: 'ID3DXBaseEffect :: setInt, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3c27d66544d4064c8d6c682db168b57b88d213cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322621"
---
# <a name="id3dxbaseeffectsetint-method"></a><span data-ttu-id="a14af-103">ID3DXBaseEffect :: setInt, méthode</span><span class="sxs-lookup"><span data-stu-id="a14af-103">ID3DXBaseEffect::SetInt method</span></span>

<span data-ttu-id="a14af-104">Définit un entier.</span><span class="sxs-lookup"><span data-stu-id="a14af-104">Sets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a14af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a14af-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hParameter,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="a14af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a14af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14af-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a14af-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14af-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a14af-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a14af-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="a14af-109">Unique identifier.</span></span> <span data-ttu-id="a14af-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a14af-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a14af-111">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a14af-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14af-112">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a14af-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a14af-113">Valeur de type entier.</span><span class="sxs-lookup"><span data-stu-id="a14af-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a14af-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a14af-114">Return value</span></span>

<span data-ttu-id="a14af-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a14af-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a14af-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a14af-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a14af-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a14af-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14af-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a14af-118">Requirements</span></span>



| <span data-ttu-id="a14af-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a14af-119">Requirement</span></span> | <span data-ttu-id="a14af-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a14af-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14af-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a14af-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a14af-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a14af-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a14af-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a14af-123">Library</span></span><br/> | <dl> <span data-ttu-id="a14af-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a14af-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a14af-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a14af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14af-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a14af-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a14af-127">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="a14af-127">**GetInt**</span></span>](id3dxbaseeffect--getint.md)
</dt> </dl>

 

 
