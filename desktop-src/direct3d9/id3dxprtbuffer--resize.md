---
description: Modifie le nombre d’échantillons contenus dans la mémoire tampon.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'ID3DXPRTBuffer :: Resize, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c54044ffc9e166131faa16c9b438b497c658ef25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522367"
---
# <a name="id3dxprtbufferresize-method"></a><span data-ttu-id="e9ede-103">ID3DXPRTBuffer :: Resize, méthode</span><span class="sxs-lookup"><span data-stu-id="e9ede-103">ID3DXPRTBuffer::Resize method</span></span>

<span data-ttu-id="e9ede-104">Modifie le nombre d’échantillons contenus dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e9ede-104">Changes the number of samples contained in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ede-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9ede-105">Syntax</span></span>


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a><span data-ttu-id="e9ede-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9ede-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ede-107">*Actualité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9ede-107">*NewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ede-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9ede-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9ede-109">Nombre d’échantillons à contenir dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e9ede-109">Number of samples to be contained in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ede-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9ede-110">Return value</span></span>

<span data-ttu-id="e9ede-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9ede-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9ede-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9ede-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9ede-113">Si la méthode échoue, la valeur suivante est retournée, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e9ede-113">If the method fails, the following value will be returned, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ede-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9ede-114">Requirements</span></span>



| <span data-ttu-id="e9ede-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9ede-115">Requirement</span></span> | <span data-ttu-id="e9ede-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9ede-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ede-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9ede-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e9ede-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ede-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9ede-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9ede-119">Library</span></span><br/> | <dl> <span data-ttu-id="e9ede-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9ede-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9ede-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9ede-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ede-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="e9ede-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
