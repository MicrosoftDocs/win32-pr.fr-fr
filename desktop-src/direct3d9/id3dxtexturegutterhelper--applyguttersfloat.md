---
description: Applique des reliures à une mémoire tampon de texture FLOTTante.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'ID3DXTextureGutterHelper :: ApplyGuttersFloat, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106540927"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a><span data-ttu-id="9808a-103">ID3DXTextureGutterHelper :: ApplyGuttersFloat, méthode</span><span class="sxs-lookup"><span data-stu-id="9808a-103">ID3DXTextureGutterHelper::ApplyGuttersFloat method</span></span>

<span data-ttu-id="9808a-104">Applique des reliures à une mémoire tampon de texture FLOTTante.</span><span class="sxs-lookup"><span data-stu-id="9808a-104">Applies gutters to a FLOAT texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9808a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9808a-105">Syntax</span></span>


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a><span data-ttu-id="9808a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9808a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9808a-107">*pDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9808a-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9808a-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9808a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9808a-109">Pointeur vers une mémoire tampon de données de texture de type FLOAT.</span><span class="sxs-lookup"><span data-stu-id="9808a-109">Pointer to a buffer of FLOAT texture data.</span></span>

</dd> <dt>

<span data-ttu-id="9808a-110">*NumCoeffs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9808a-110">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9808a-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9808a-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9808a-112">Nombre de scalaires par canal de couleurs utilisé en mémoire pour stocker des exemples.</span><span class="sxs-lookup"><span data-stu-id="9808a-112">Number of scalars per color channel used in memory to store samples.</span></span> <span data-ttu-id="9808a-113">Chaque Texel contient des valeurs FLOAT NumCoeffs.</span><span class="sxs-lookup"><span data-stu-id="9808a-113">Each texel contains NumCoeffs FLOAT values.</span></span>

</dd> <dt>

<span data-ttu-id="9808a-114">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9808a-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9808a-115">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9808a-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9808a-116">Largeur de la texture, en pixels, obtenue à partir de [**ID3DXTextureGutterHelper :: GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span><span class="sxs-lookup"><span data-stu-id="9808a-116">Width of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span></span>

</dd> <dt>

<span data-ttu-id="9808a-117">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9808a-117">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9808a-118">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9808a-118">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9808a-119">Hauteur de la texture, en pixels, obtenue à partir de [**ID3DXTextureGutterHelper :: GetHeight**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="9808a-119">Height of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9808a-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9808a-120">Return value</span></span>

<span data-ttu-id="9808a-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9808a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9808a-122">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9808a-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9808a-123">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="9808a-123">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="9808a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9808a-124">Remarks</span></span>

<span data-ttu-id="9808a-125">Les [**texels de classe 2**](id3dxtexturegutterhelper.md) sont générés par le rééchantillonnage des texels de classe 1 et 4.</span><span class="sxs-lookup"><span data-stu-id="9808a-125">[**Class 2 texels**](id3dxtexturegutterhelper.md) are generated by resampling class 1 and 4 texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="9808a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9808a-126">Requirements</span></span>



| <span data-ttu-id="9808a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9808a-127">Requirement</span></span> | <span data-ttu-id="9808a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9808a-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9808a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9808a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9808a-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9808a-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9808a-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9808a-131">Library</span></span><br/> | <dl> <span data-ttu-id="9808a-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9808a-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9808a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9808a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9808a-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="9808a-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
