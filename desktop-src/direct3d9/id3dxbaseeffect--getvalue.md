---
description: Obtient la valeur d’une annotation ou d’un paramètre arbitraire, y compris des types simples, des structs, des tableaux, des chaînes, des nuanceurs et des textures. Cette méthode peut être utilisée à la place de presque tous les appels GetXXX dans ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'ID3DXBaseEffect :: GetValue, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538311"
---
# <a name="id3dxbaseeffectgetvalue-method"></a><span data-ttu-id="a48f0-104">ID3DXBaseEffect :: GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="a48f0-104">ID3DXBaseEffect::GetValue method</span></span>

<span data-ttu-id="a48f0-105">Obtient la valeur d’une annotation ou d’un paramètre arbitraire, y compris des types simples, des structs, des tableaux, des chaînes, des nuanceurs et des textures.</span><span class="sxs-lookup"><span data-stu-id="a48f0-105">Get the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span> <span data-ttu-id="a48f0-106">Cette méthode peut être utilisée à la place de presque tous les appels GetXXX dans [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="a48f0-106">This method can be used in place of nearly all the Getxxx calls in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a48f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a48f0-107">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="a48f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a48f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a48f0-109">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a48f0-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a48f0-110">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a48f0-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a48f0-111">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="a48f0-111">Unique identifier.</span></span> <span data-ttu-id="a48f0-112">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a48f0-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a48f0-113">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a48f0-113">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a48f0-114">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a48f0-114">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a48f0-115">Retourne une mémoire tampon contenant la valeur.</span><span class="sxs-lookup"><span data-stu-id="a48f0-115">Returns a buffer containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="a48f0-116">*Octets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a48f0-116">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a48f0-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a48f0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a48f0-118">\[en \] nombre d’octets dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a48f0-118">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="a48f0-119">Passez à \_ la passerelle par défaut D3DX si vous savez que votre mémoire tampon est suffisamment grande pour contenir le paramètre entier et que vous souhaitez ignorer la validation de la taille.</span><span class="sxs-lookup"><span data-stu-id="a48f0-119">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a48f0-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a48f0-120">Return value</span></span>

<span data-ttu-id="a48f0-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a48f0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a48f0-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a48f0-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a48f0-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a48f0-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a48f0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a48f0-124">Requirements</span></span>



| <span data-ttu-id="a48f0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a48f0-125">Requirement</span></span> | <span data-ttu-id="a48f0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a48f0-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48f0-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a48f0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a48f0-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a48f0-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a48f0-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a48f0-129">Library</span></span><br/> | <dl> <span data-ttu-id="a48f0-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a48f0-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a48f0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a48f0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48f0-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a48f0-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a48f0-133">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="a48f0-133">**SetValue**</span></span>](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
