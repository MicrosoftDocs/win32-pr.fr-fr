---
description: Rééchantillonne une mémoire tampon d’entrée ID3DXPRTBuffer et l’enregistre dans une mémoire tampon de sortie. Cette méthode peut être utilisée pour convertir une mémoire tampon de vertex en une mémoire tampon de texture et vice versa. Il peut également être utilisé pour convertir des mémoires tampons à canal unique en mémoires tampons de 3 canaux et vice versa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'ID3DXPRTEngine :: ResampleBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762290"
---
# <a name="id3dxprtengineresamplebuffer-method"></a><span data-ttu-id="bb494-105">ID3DXPRTEngine :: ResampleBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="bb494-105">ID3DXPRTEngine::ResampleBuffer method</span></span>

<span data-ttu-id="bb494-106">Rééchantillonne une mémoire tampon d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) et l’enregistre dans une mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="bb494-106">Resamples an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer and saves it to an output buffer.</span></span> <span data-ttu-id="bb494-107">Cette méthode peut être utilisée pour convertir une mémoire tampon de vertex en une mémoire tampon de texture et vice versa.</span><span class="sxs-lookup"><span data-stu-id="bb494-107">This method can be used to convert a vertex buffer to a texture buffer and vice-versa.</span></span> <span data-ttu-id="bb494-108">Il peut également être utilisé pour convertir des mémoires tampons à canal unique en mémoires tampons de 3 canaux et vice versa.</span><span class="sxs-lookup"><span data-stu-id="bb494-108">It can also be used to convert single-channel buffers to 3-channel buffers and vice-versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb494-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb494-109">Syntax</span></span>


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a><span data-ttu-id="bb494-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb494-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb494-111">*pBufferIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb494-111">*pBufferIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb494-112">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bb494-112">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bb494-113">Pointeur vers la mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bb494-113">Pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bb494-114">*pBufferOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bb494-114">*pBufferOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb494-115">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bb494-115">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bb494-116">Pointeur vers la mémoire tampon de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="bb494-116">Pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb494-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb494-117">Return value</span></span>

<span data-ttu-id="bb494-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb494-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb494-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb494-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bb494-120">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bb494-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb494-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb494-121">Requirements</span></span>



| <span data-ttu-id="bb494-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb494-122">Requirement</span></span> | <span data-ttu-id="bb494-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb494-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb494-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb494-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bb494-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb494-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bb494-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb494-126">Library</span></span><br/> | <dl> <span data-ttu-id="bb494-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb494-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb494-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb494-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb494-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="bb494-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 




