---
title: Méthode ID3DX11EffectShaderVariable GetShaderDesc (D3dx11effect. h)
description: Obtenir une description du nuanceur.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Méthode GetShaderDesc Direct3D 11
- Méthode GetShaderDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c76730d1ad5f3de35e273034d3a17beb71fb7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974663"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a><span data-ttu-id="ea9c3-106">ID3DX11EffectShaderVariable :: GetShaderDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="ea9c3-106">ID3DX11EffectShaderVariable::GetShaderDesc method</span></span>

<span data-ttu-id="ea9c3-107">Obtenir une description du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ea9c3-107">Get a shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea9c3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea9c3-108">Syntax</span></span>


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ea9c3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea9c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9c3-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="ea9c3-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9c3-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ea9c3-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ea9c3-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="ea9c3-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="ea9c3-113">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="ea9c3-113">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9c3-114">Type : **[ **D3DX11 \_ Effect \_ Shader \_ desc**](d3dx11-effect-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea9c3-114">Type: **[**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)\***</span></span>

<span data-ttu-id="ea9c3-115">Pointeur vers une description de nuanceur (voir [**D3DX11 \_ Effect \_ Shader \_ desc**](d3dx11-effect-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="ea9c3-115">A pointer to a shader description (see [**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9c3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea9c3-116">Return value</span></span>

<span data-ttu-id="ea9c3-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea9c3-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea9c3-118">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="ea9c3-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9c3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ea9c3-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea9c3-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="ea9c3-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ea9c3-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="ea9c3-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ea9c3-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ea9c3-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea9c3-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea9c3-123">Requirements</span></span>



| <span data-ttu-id="ea9c3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea9c3-124">Requirement</span></span> | <span data-ttu-id="ea9c3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea9c3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9c3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea9c3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ea9c3-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea9c3-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ea9c3-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea9c3-128">Library</span></span><br/> | <dl> <span data-ttu-id="ea9c3-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="ea9c3-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9c3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea9c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9c3-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="ea9c3-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

