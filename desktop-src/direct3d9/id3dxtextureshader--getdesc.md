---
description: Obtient une description de la table constante.
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
ms.openlocfilehash: 97302b7e0f8c9f05e6229e20c2c9c158173ed944
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211788"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="81ce9-103">ID3DXTextureShader :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="81ce9-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="81ce9-104">Obtient une description de la table constante.</span><span class="sxs-lookup"><span data-stu-id="81ce9-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ce9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81ce9-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="81ce9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81ce9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ce9-107">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81ce9-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ce9-108">Type : **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="81ce9-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="81ce9-109">Attributs de la table constante.</span><span class="sxs-lookup"><span data-stu-id="81ce9-109">The attributes of the constant table.</span></span> <span data-ttu-id="81ce9-110">Consultez [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="81ce9-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ce9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81ce9-111">Return value</span></span>

<span data-ttu-id="81ce9-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81ce9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81ce9-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81ce9-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="81ce9-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="81ce9-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ce9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81ce9-115">Requirements</span></span>



| <span data-ttu-id="81ce9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81ce9-116">Requirement</span></span> | <span data-ttu-id="81ce9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="81ce9-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ce9-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="81ce9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="81ce9-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="81ce9-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="81ce9-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81ce9-120">Library</span></span><br/> | <dl> <span data-ttu-id="81ce9-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81ce9-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="81ce9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81ce9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ce9-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="81ce9-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




