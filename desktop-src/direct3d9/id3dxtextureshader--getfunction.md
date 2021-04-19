---
description: Obtient un pointeur vers le flux de fonction DWORD.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'ID3DXTextureShader :: GetFunction, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523852"
---
# <a name="id3dxtextureshadergetfunction-method"></a><span data-ttu-id="cdb6b-103">ID3DXTextureShader :: GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="cdb6b-103">ID3DXTextureShader::GetFunction method</span></span>

<span data-ttu-id="cdb6b-104">Obtient un pointeur vers le flux de fonction DWORD.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-104">Gets a pointer to the function DWORD stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdb6b-105">Syntax</span></span>


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a><span data-ttu-id="cdb6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdb6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb6b-107">*ppFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdb6b-107">*ppFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb6b-108">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdb6b-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cdb6b-109">Pointeur vers le flux de fonction DWORD.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-109">A pointer to the function DWORD stream.</span></span> <span data-ttu-id="cdb6b-110">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cdb6b-110">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdb6b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdb6b-111">Return value</span></span>

<span data-ttu-id="cdb6b-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdb6b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdb6b-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cdb6b-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb6b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdb6b-115">Requirements</span></span>



| <span data-ttu-id="cdb6b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdb6b-116">Requirement</span></span> | <span data-ttu-id="cdb6b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdb6b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb6b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdb6b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cdb6b-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdb6b-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cdb6b-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cdb6b-120">Library</span></span><br/> | <dl> <span data-ttu-id="cdb6b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdb6b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cdb6b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdb6b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb6b-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="cdb6b-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




