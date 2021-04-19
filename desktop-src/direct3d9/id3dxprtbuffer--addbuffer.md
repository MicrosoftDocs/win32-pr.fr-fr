---
description: Ajoute une autre mémoire tampon au ID3DXPRTBuffer et stocke les résultats dans ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'ID3DXPRTBuffer :: AddBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527962"
---
# <a name="id3dxprtbufferaddbuffer-method"></a><span data-ttu-id="7fae6-103">ID3DXPRTBuffer :: AddBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="7fae6-103">ID3DXPRTBuffer::AddBuffer method</span></span>

<span data-ttu-id="7fae6-104">Ajoute une autre mémoire tampon au [**ID3DXPRTBuffer**](id3dxprtbuffer.md) et stocke les résultats dans **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="7fae6-104">Adds another buffer to the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and stores the results in **ID3DXPRTBuffer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fae6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fae6-105">Syntax</span></span>


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="7fae6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fae6-107">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fae6-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fae6-108">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7fae6-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7fae6-109">Pointeur vers une mémoire tampon qui contient les membres à ajouter aux membres respectifs de la mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7fae6-109">Pointer to a buffer that contains members to be added to the respective members of the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fae6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fae6-110">Return value</span></span>

<span data-ttu-id="7fae6-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7fae6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7fae6-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7fae6-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7fae6-113">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="7fae6-113">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fae6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7fae6-114">Remarks</span></span>

<span data-ttu-id="7fae6-115">pBuffer et [**ID3DXPRTBuffer**](id3dxprtbuffer.md) doivent avoir le même nombre d’échantillons, de coefficients et de canaux de couleur ; Sinon, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="7fae6-115">pBuffer and [**ID3DXPRTBuffer**](id3dxprtbuffer.md) must have the same number of samples, coefficients, and color channels; the method will fail otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fae6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fae6-116">Requirements</span></span>



| <span data-ttu-id="7fae6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fae6-117">Requirement</span></span> | <span data-ttu-id="7fae6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fae6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fae6-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fae6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7fae6-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fae6-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7fae6-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7fae6-121">Library</span></span><br/> | <dl> <span data-ttu-id="7fae6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fae6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7fae6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fae6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fae6-124">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="7fae6-124">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




