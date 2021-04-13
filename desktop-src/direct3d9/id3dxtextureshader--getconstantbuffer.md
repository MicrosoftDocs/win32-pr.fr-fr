---
description: Obtient un pointeur vers la table constante.
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'ID3DXTextureShader :: GetConstantBuffer, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322777"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a><span data-ttu-id="12416-103">ID3DXTextureShader :: GetConstantBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="12416-103">ID3DXTextureShader::GetConstantBuffer method</span></span>

<span data-ttu-id="12416-104">Obtient un pointeur vers la table constante.</span><span class="sxs-lookup"><span data-stu-id="12416-104">Get a pointer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="12416-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12416-105">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="12416-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12416-107">*ppConstantBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="12416-107">*ppConstantBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12416-108">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="12416-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="12416-109">Pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient les constantes.</span><span class="sxs-lookup"><span data-stu-id="12416-109">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains the constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12416-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12416-110">Return value</span></span>

<span data-ttu-id="12416-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12416-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12416-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12416-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="12416-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="12416-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="12416-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12416-114">Requirements</span></span>



| <span data-ttu-id="12416-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12416-115">Requirement</span></span> | <span data-ttu-id="12416-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="12416-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12416-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="12416-117">Header</span></span><br/>  | <dl> <span data-ttu-id="12416-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="12416-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="12416-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12416-119">Library</span></span><br/> | <dl> <span data-ttu-id="12416-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12416-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="12416-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12416-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12416-122">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="12416-122">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




