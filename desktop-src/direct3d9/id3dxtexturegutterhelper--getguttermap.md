---
description: Reçoit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'ID3DXTextureGutterHelper :: GetGutterMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539456"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a><span data-ttu-id="042f2-103">ID3DXTextureGutterHelper :: GetGutterMap, méthode</span><span class="sxs-lookup"><span data-stu-id="042f2-103">ID3DXTextureGutterHelper::GetGutterMap method</span></span>

<span data-ttu-id="042f2-104">Reçoit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="042f2-104">Receives a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="042f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="042f2-105">Syntax</span></span>


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="042f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="042f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042f2-107">*pGutterData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="042f2-107">*pGutterData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="042f2-108">Type : **[ **Byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="042f2-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="042f2-109">Pointeur désignant la classe Texel.</span><span class="sxs-lookup"><span data-stu-id="042f2-109">Pointer to the texel class.</span></span> <span data-ttu-id="042f2-110">Les classes Texel possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="042f2-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="042f2-111">Il n’existe pas de classe Texel 3.</span><span class="sxs-lookup"><span data-stu-id="042f2-111">There is no texel class 3.</span></span>



| <span data-ttu-id="042f2-112">Texel (classe)</span><span class="sxs-lookup"><span data-stu-id="042f2-112">Texel Class</span></span> | <span data-ttu-id="042f2-113">Emplacement de Texel</span><span class="sxs-lookup"><span data-stu-id="042f2-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="042f2-114">0</span><span class="sxs-lookup"><span data-stu-id="042f2-114">0</span></span>           | <span data-ttu-id="042f2-115">Point non valide ; Texel ne sera pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="042f2-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="042f2-116">1</span><span class="sxs-lookup"><span data-stu-id="042f2-116">1</span></span>           | <span data-ttu-id="042f2-117">Triangle intérieur.</span><span class="sxs-lookup"><span data-stu-id="042f2-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="042f2-118">2</span><span class="sxs-lookup"><span data-stu-id="042f2-118">2</span></span>           | <span data-ttu-id="042f2-119">Marge intérieure.</span><span class="sxs-lookup"><span data-stu-id="042f2-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="042f2-120">4</span><span class="sxs-lookup"><span data-stu-id="042f2-120">4</span></span>           | <span data-ttu-id="042f2-121">Marge intérieure ; Texel sera évalué comme un exemple complet dans les méthodes [**ID3DXTextureGutterHelper :: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper :: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper :: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="042f2-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042f2-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="042f2-122">Return value</span></span>

<span data-ttu-id="042f2-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="042f2-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="042f2-124">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="042f2-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="042f2-125">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="042f2-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="042f2-126">Notes</span><span class="sxs-lookup"><span data-stu-id="042f2-126">Remarks</span></span>

<span data-ttu-id="042f2-127">L’application doit allouer et gérer des pGutterData, avec la taille donnée par :</span><span class="sxs-lookup"><span data-stu-id="042f2-127">The application must allocate and manage pGutterData, with size given by:</span></span>


```
texture width * texture height * sizeof(BYTE)
```



<span data-ttu-id="042f2-128">La largeur et la hauteur de la texture sont retournées par [**ID3DXTextureGutterHelper :: GetWidth**](id3dxtexturegutterhelper--getwidth.md) et [**ID3DXTextureGutterHelper :: GetHeight**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="042f2-128">Texture width and height are returned by [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) and [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="042f2-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="042f2-129">Requirements</span></span>



| <span data-ttu-id="042f2-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="042f2-130">Requirement</span></span> | <span data-ttu-id="042f2-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="042f2-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="042f2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="042f2-132">Header</span></span><br/>  | <dl> <span data-ttu-id="042f2-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="042f2-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="042f2-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="042f2-134">Library</span></span><br/> | <dl> <span data-ttu-id="042f2-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="042f2-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="042f2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="042f2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="042f2-137">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="042f2-137">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
