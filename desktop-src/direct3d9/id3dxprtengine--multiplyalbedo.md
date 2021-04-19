---
description: Multiplie chaque vecteur de transfert luminance (PRT) précalculé par le Albedo par vertex.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine :: MultiplyAlbedo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524876"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a><span data-ttu-id="78cfc-103">ID3DXPRTEngine :: MultiplyAlbedo, méthode</span><span class="sxs-lookup"><span data-stu-id="78cfc-103">ID3DXPRTEngine::MultiplyAlbedo method</span></span>

<span data-ttu-id="78cfc-104">Multiplie chaque vecteur de transfert luminance (PRT) précalculé par le Albedo par vertex.</span><span class="sxs-lookup"><span data-stu-id="78cfc-104">Multiplies each precomputed radiance transfer (PRT) vector by the per-vertex albedo.</span></span>

## <a name="syntax"></a><span data-ttu-id="78cfc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78cfc-105">Syntax</span></span>


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="78cfc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78cfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78cfc-107">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="78cfc-107">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78cfc-108">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="78cfc-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="78cfc-109">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui contiendra les VECTEURs PRT multipliés par le Albedo par vertex.</span><span class="sxs-lookup"><span data-stu-id="78cfc-109">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will contain PRT vectors multiplied by the per-vertex albedo.</span></span> <span data-ttu-id="78cfc-110">Si cette mémoire tampon de sortie est un objet de texture, vous devez veiller à stocker le albedo de la texture à la même résolution que la mémoire tampon de simulation.</span><span class="sxs-lookup"><span data-stu-id="78cfc-110">If this output buffer is a texture object, then care must be taken to store the albedo of the texture at the same resolution as the simulation buffer.</span></span> <span data-ttu-id="78cfc-111">Vous pouvez définir la résolution appropriée sur le Albedo avec [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), en appliquant les zones de marge de texture, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="78cfc-111">You can set the proper resolution on the albedo with [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applying texture gutter regions if appropriate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78cfc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78cfc-112">Return value</span></span>

<span data-ttu-id="78cfc-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78cfc-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78cfc-114">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78cfc-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="78cfc-115">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="78cfc-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="78cfc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="78cfc-116">Remarks</span></span>

<span data-ttu-id="78cfc-117">Les méthodes ID3DXPRTEngine :: Computexxx calculent les mémoires tampons de sortie dans lesquelles le signal lumineux n’a pas été multiplié par Albedo.</span><span class="sxs-lookup"><span data-stu-id="78cfc-117">The ID3DXPRTEngine::Computexxx methods compute output buffers in which the light signal has not been multiplied by albedo.</span></span> <span data-ttu-id="78cfc-118">En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.</span><span class="sxs-lookup"><span data-stu-id="78cfc-118">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="78cfc-119">Pour inclure Albedo dans le modèle de lumière rendue, appelez cette méthode après l’une des méthodes Computexxx.</span><span class="sxs-lookup"><span data-stu-id="78cfc-119">To include albedo in the rendered-light model, call this method after one of the Computexxx methods.</span></span>

<span data-ttu-id="78cfc-120">[**ID3DXPRTEngine :: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) doit être appelé avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="78cfc-120">[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) should be called before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="78cfc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78cfc-121">Requirements</span></span>



| <span data-ttu-id="78cfc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78cfc-122">Requirement</span></span> | <span data-ttu-id="78cfc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="78cfc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78cfc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="78cfc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="78cfc-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="78cfc-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78cfc-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78cfc-126">Library</span></span><br/> | <dl> <span data-ttu-id="78cfc-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78cfc-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78cfc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78cfc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78cfc-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="78cfc-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="78cfc-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="78cfc-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




