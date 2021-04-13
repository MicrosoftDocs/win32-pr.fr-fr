---
description: Compilez un effet.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'ID3DXEffectCompiler :: CompileEffect, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322717"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a><span data-ttu-id="209a1-103">ID3DXEffectCompiler :: CompileEffect, méthode</span><span class="sxs-lookup"><span data-stu-id="209a1-103">ID3DXEffectCompiler::CompileEffect method</span></span>

<span data-ttu-id="209a1-104">Compilez un effet.</span><span class="sxs-lookup"><span data-stu-id="209a1-104">Compile an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="209a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="209a1-105">Syntax</span></span>


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="209a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="209a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="209a1-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="209a1-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="209a1-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="209a1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="209a1-109">Options de compilation identifiées par différents indicateurs.</span><span class="sxs-lookup"><span data-stu-id="209a1-109">Compile options identified by various flags.</span></span> <span data-ttu-id="209a1-110">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="209a1-110">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="209a1-111">Pour plus d’informations, consultez [indicateurs D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="209a1-111">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="209a1-112">*ppEffect* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="209a1-112">*ppEffect* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="209a1-113">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="209a1-113">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="209a1-114">Mémoire tampon contenant l’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="209a1-114">Buffer containing the compiled effect.</span></span> <span data-ttu-id="209a1-115">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="209a1-115">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="209a1-116">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="209a1-116">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="209a1-117">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="209a1-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="209a1-118">Mémoire tampon contenant au moins le premier message d’erreur de compilation qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="209a1-118">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="209a1-119">Cela comprend les erreurs d’effet du compilateur et les erreurs de compilation du langage de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="209a1-119">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="209a1-120">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="209a1-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="209a1-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="209a1-121">Return value</span></span>

<span data-ttu-id="209a1-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="209a1-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="209a1-123">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="209a1-123">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="209a1-124">Si les arguments ne sont pas valides, la méthode retourne D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="209a1-124">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="209a1-125">Si la méthode échoue, la valeur de retour est E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="209a1-125">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="209a1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="209a1-126">Requirements</span></span>



| <span data-ttu-id="209a1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="209a1-127">Requirement</span></span> | <span data-ttu-id="209a1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="209a1-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="209a1-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="209a1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="209a1-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="209a1-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="209a1-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="209a1-131">Library</span></span><br/> | <dl> <span data-ttu-id="209a1-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="209a1-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="209a1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="209a1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209a1-134">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="209a1-134">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> </dl>

 

 
