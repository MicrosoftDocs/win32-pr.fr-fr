---
title: Méthode ID3DX11EffectPass GetComputeShaderDesc (D3dx11effect. h)
description: Obtenir une description du nuanceur de calcul.
ms.assetid: 9c3a702f-2016-4b1a-a832-d1bb968aec2d
keywords:
- Méthode GetComputeShaderDesc Direct3D 11
- Méthode GetComputeShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetComputeShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetComputeShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21cc13699553b0da60498209ddffd31a56607809
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953961"
---
# <a name="id3dx11effectpassgetcomputeshaderdesc-method"></a><span data-ttu-id="5ac1a-106">ID3DX11EffectPass :: GetComputeShaderDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="5ac1a-106">ID3DX11EffectPass::GetComputeShaderDesc method</span></span>

<span data-ttu-id="5ac1a-107">Obtenir une description du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="5ac1a-107">Get a compute-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac1a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ac1a-108">Syntax</span></span>


```C++
HRESULT GetComputeShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="5ac1a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ac1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac1a-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="5ac1a-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac1a-111">Type : **[ **D3DX11 \_ passe- \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ac1a-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="5ac1a-112">Pointeur désignant une description du nuanceur de calcul (consultez [**D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="5ac1a-112">A pointer to a compute-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac1a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ac1a-113">Return value</span></span>

<span data-ttu-id="5ac1a-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ac1a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ac1a-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="5ac1a-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac1a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5ac1a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ac1a-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="5ac1a-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5ac1a-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="5ac1a-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5ac1a-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5ac1a-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ac1a-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5ac1a-120">Requirements</span></span>



| <span data-ttu-id="5ac1a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ac1a-121">Requirement</span></span> | <span data-ttu-id="5ac1a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ac1a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac1a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ac1a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5ac1a-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac1a-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5ac1a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ac1a-125">Library</span></span><br/> | <dl> <span data-ttu-id="5ac1a-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac1a-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac1a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ac1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac1a-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="5ac1a-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





