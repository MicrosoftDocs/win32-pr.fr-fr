---
title: Méthode ID3DX11EffectShaderVariable GetPixelShader (D3dx11effect. h)
description: Obtenir un nuanceur de pixels.
ms.assetid: 4ce4b248-23b9-4135-a2b4-262e63247688
keywords:
- Méthode GetPixelShader Direct3D 11
- Méthode GetPixelShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetPixelShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPixelShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6588fd9afb7e58308f0fbc120705d4a22d9f2ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531024"
---
# <a name="id3dx11effectshadervariablegetpixelshader-method"></a><span data-ttu-id="d18b6-106">ID3DX11EffectShaderVariable :: GetPixelShader, méthode</span><span class="sxs-lookup"><span data-stu-id="d18b6-106">ID3DX11EffectShaderVariable::GetPixelShader method</span></span>

<span data-ttu-id="d18b6-107">Obtenir un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="d18b6-107">Get a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18b6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d18b6-108">Syntax</span></span>


```C++
HRESULT GetPixelShader(
   UINT              ShaderIndex,
   ID3D11PixelShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="d18b6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d18b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d18b6-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="d18b6-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="d18b6-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d18b6-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d18b6-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="d18b6-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="d18b6-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="d18b6-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="d18b6-114">Type : **[ **ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="d18b6-114">Type: **[**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span></span>

<span data-ttu-id="d18b6-115">Pointeur vers un pointeur [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) qui sera défini sur le nuanceur de pixels lors du retour.</span><span class="sxs-lookup"><span data-stu-id="d18b6-115">A pointer to an [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) pointer that will be set to the pixel shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d18b6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d18b6-116">Return value</span></span>

<span data-ttu-id="d18b6-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d18b6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d18b6-118">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="d18b6-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d18b6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d18b6-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d18b6-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="d18b6-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d18b6-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="d18b6-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d18b6-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d18b6-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d18b6-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d18b6-123">Requirements</span></span>



| <span data-ttu-id="d18b6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d18b6-124">Requirement</span></span> | <span data-ttu-id="d18b6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d18b6-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18b6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d18b6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d18b6-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d18b6-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d18b6-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d18b6-128">Library</span></span><br/> | <dl> <span data-ttu-id="d18b6-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="d18b6-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18b6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d18b6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18b6-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="d18b6-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

