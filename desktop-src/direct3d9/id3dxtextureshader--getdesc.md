---
description: 'ID3DXTextureShader :: GetDesc, méthode-obtient une description de la table constante.'
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'ID3DXTextureShader :: GetDesc, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ea94f0e22d838f09dae9b423f85aa1d55d2365b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117637"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="b0303-103">ID3DXTextureShader :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="b0303-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="b0303-104">Obtient une description de la table constante.</span><span class="sxs-lookup"><span data-stu-id="b0303-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0303-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0303-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="b0303-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0303-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0303-107">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0303-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0303-108">Type : **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0303-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="b0303-109">Attributs de la table constante.</span><span class="sxs-lookup"><span data-stu-id="b0303-109">The attributes of the constant table.</span></span> <span data-ttu-id="b0303-110">Consultez [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b0303-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0303-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0303-111">Return value</span></span>

<span data-ttu-id="b0303-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0303-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0303-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0303-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0303-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="b0303-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0303-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0303-115">Requirements</span></span>



| <span data-ttu-id="b0303-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0303-116">Requirement</span></span> | <span data-ttu-id="b0303-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0303-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0303-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0303-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b0303-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0303-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b0303-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0303-120">Library</span></span><br/> | <dl> <span data-ttu-id="b0303-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0303-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b0303-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0303-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0303-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b0303-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




