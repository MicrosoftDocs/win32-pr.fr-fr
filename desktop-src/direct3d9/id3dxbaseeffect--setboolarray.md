---
description: 'ID3DXBaseEffect :: SetBoolArray, méthode-définit un tableau de valeurs booléennes.'
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'ID3DXBaseEffect :: SetBoolArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cad6846914d348dd49d6362d70271c5af078e35d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093827"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="54472-103">ID3DXBaseEffect :: SetBoolArray, méthode</span><span class="sxs-lookup"><span data-stu-id="54472-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="54472-104">Définit un tableau de valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="54472-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="54472-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54472-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="54472-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54472-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54472-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54472-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="54472-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="54472-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="54472-109">Unique identifier.</span></span> <span data-ttu-id="54472-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="54472-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="54472-111">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54472-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54472-112">Type : **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="54472-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54472-113">Tableau de valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="54472-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="54472-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54472-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54472-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54472-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54472-116">Nombre de valeurs booléennes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="54472-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54472-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54472-117">Return value</span></span>

<span data-ttu-id="54472-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54472-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54472-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54472-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54472-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="54472-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="54472-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54472-121">Requirements</span></span>



| <span data-ttu-id="54472-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54472-122">Requirement</span></span> | <span data-ttu-id="54472-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="54472-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54472-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="54472-124">Header</span></span><br/>  | <dl> <span data-ttu-id="54472-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="54472-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="54472-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54472-126">Library</span></span><br/> | <dl> <span data-ttu-id="54472-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54472-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="54472-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54472-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54472-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="54472-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="54472-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="54472-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
