---
description: Définit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'ID3DXTextureGutterHelper :: SetGutterMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523224"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a><span data-ttu-id="c0882-103">ID3DXTextureGutterHelper :: SetGutterMap, méthode</span><span class="sxs-lookup"><span data-stu-id="c0882-103">ID3DXTextureGutterHelper::SetGutterMap method</span></span>

<span data-ttu-id="c0882-104">Définit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="c0882-104">Sets a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0882-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0882-105">Syntax</span></span>


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="c0882-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0882-107">*pGutterData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0882-107">*pGutterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0882-108">Type : **[ **Byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0882-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c0882-109">Pointeur désignant la classe Texel.</span><span class="sxs-lookup"><span data-stu-id="c0882-109">Pointer to the texel class.</span></span> <span data-ttu-id="c0882-110">Les classes Texel possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0882-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="c0882-111">Il n’existe pas de classe Texel 3.</span><span class="sxs-lookup"><span data-stu-id="c0882-111">There is no texel class 3.</span></span>



| <span data-ttu-id="c0882-112">Texel (classe)</span><span class="sxs-lookup"><span data-stu-id="c0882-112">Texel Class</span></span> | <span data-ttu-id="c0882-113">Emplacement de Texel</span><span class="sxs-lookup"><span data-stu-id="c0882-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0882-114">0</span><span class="sxs-lookup"><span data-stu-id="c0882-114">0</span></span>           | <span data-ttu-id="c0882-115">Point non valide ; Texel ne sera pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c0882-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c0882-116">1</span><span class="sxs-lookup"><span data-stu-id="c0882-116">1</span></span>           | <span data-ttu-id="c0882-117">Triangle intérieur.</span><span class="sxs-lookup"><span data-stu-id="c0882-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c0882-118">2</span><span class="sxs-lookup"><span data-stu-id="c0882-118">2</span></span>           | <span data-ttu-id="c0882-119">Marge intérieure.</span><span class="sxs-lookup"><span data-stu-id="c0882-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c0882-120">4</span><span class="sxs-lookup"><span data-stu-id="c0882-120">4</span></span>           | <span data-ttu-id="c0882-121">Marge intérieure ; Texel sera évalué comme un exemple complet dans les méthodes [**ID3DXTextureGutterHelper :: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper :: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper :: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="c0882-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0882-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0882-122">Return value</span></span>

<span data-ttu-id="c0882-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0882-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0882-124">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0882-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c0882-125">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="c0882-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="c0882-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0882-126">Requirements</span></span>



| <span data-ttu-id="c0882-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0882-127">Requirement</span></span> | <span data-ttu-id="c0882-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0882-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0882-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0882-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c0882-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0882-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c0882-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0882-131">Library</span></span><br/> | <dl> <span data-ttu-id="c0882-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0882-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c0882-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0882-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0882-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="c0882-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
