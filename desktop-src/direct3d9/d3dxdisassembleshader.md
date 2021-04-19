---
description: Désassembler un nuanceur.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: D3DXDisassembleShader, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106530935"
---
# <a name="d3dxdisassembleshader-function"></a><span data-ttu-id="3b8c6-103">D3DXDisassembleShader fonction)</span><span class="sxs-lookup"><span data-stu-id="3b8c6-103">D3DXDisassembleShader function</span></span>

<span data-ttu-id="3b8c6-104">Désassembler un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-104">Disassemble a shader.</span></span>

> [!Note]  
> <span data-ttu-id="3b8c6-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="3b8c6-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3b8c6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b8c6-106">Syntax</span></span>


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="3b8c6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b8c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b8c6-108">*pShader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b8c6-108">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8c6-109">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3b8c6-109">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3b8c6-110">Pointeur vers une mémoire tampon qui contient les données du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-110">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="3b8c6-111">*EnableColorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b8c6-111">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8c6-112">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b8c6-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b8c6-113">Activez le code couleur pour faciliter la lecture du code machine.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-113">Enable color code to make it easier to read the disassembly.</span></span>

</dd> <dt>

<span data-ttu-id="3b8c6-114">*pComments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b8c6-114">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8c6-115">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b8c6-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b8c6-116">Chaîne de commentaires facultative se terminant par un caractère NULL.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-116">An optional NULL-terminated comment string.</span></span> <span data-ttu-id="3b8c6-117">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3b8c6-118">*ppDisassembly* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3b8c6-118">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8c6-119">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b8c6-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3b8c6-120">Retourne une mémoire tampon contenant le nuanceur désassemblé.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-120">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="3b8c6-121">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3b8c6-121">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b8c6-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b8c6-122">Return value</span></span>

<span data-ttu-id="3b8c6-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b8c6-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b8c6-124">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3b8c6-125">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3b8c6-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8c6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b8c6-126">Requirements</span></span>



| <span data-ttu-id="3b8c6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b8c6-127">Requirement</span></span> | <span data-ttu-id="3b8c6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b8c6-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8c6-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b8c6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3b8c6-130"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c6-130"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3b8c6-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b8c6-131">Library</span></span><br/> | <dl> <span data-ttu-id="3b8c6-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c6-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3b8c6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b8c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8c6-134">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3b8c6-134">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
