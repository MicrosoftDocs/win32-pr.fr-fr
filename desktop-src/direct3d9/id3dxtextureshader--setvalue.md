---
description: Définit la table de constantes avec les données dans la mémoire tampon.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'ID3DXTextureShader :: SetValue, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531328"
---
# <a name="id3dxtextureshadersetvalue-method"></a><span data-ttu-id="f9b89-103">ID3DXTextureShader :: SetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="f9b89-103">ID3DXTextureShader::SetValue method</span></span>

<span data-ttu-id="f9b89-104">Définit la table de constantes avec les données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f9b89-104">Sets the constant table with the data in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b89-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9b89-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="f9b89-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9b89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b89-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9b89-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b89-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f9b89-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f9b89-109">Identificateur unique d’une constante.</span><span class="sxs-lookup"><span data-stu-id="f9b89-109">Unique identifier to a constant.</span></span> <span data-ttu-id="f9b89-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="f9b89-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9b89-111">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9b89-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b89-112">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9b89-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9b89-113">Pointeur vers une mémoire tampon contenant les données constantes.</span><span class="sxs-lookup"><span data-stu-id="f9b89-113">A pointer to a buffer containing the constant data.</span></span>

</dd> <dt>

<span data-ttu-id="f9b89-114">*Octets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9b89-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b89-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9b89-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9b89-116">Taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="f9b89-116">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b89-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9b89-117">Return value</span></span>

<span data-ttu-id="f9b89-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9b89-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9b89-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9b89-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f9b89-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f9b89-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b89-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9b89-121">Requirements</span></span>



| <span data-ttu-id="f9b89-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9b89-122">Requirement</span></span> | <span data-ttu-id="f9b89-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9b89-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b89-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9b89-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f9b89-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9b89-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f9b89-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9b89-126">Library</span></span><br/> | <dl> <span data-ttu-id="f9b89-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9b89-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f9b89-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9b89-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b89-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="f9b89-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
