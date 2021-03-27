---
title: Méthode ID3DX11EffectPass GetVertexShaderDesc (D3dx11effect. h)
description: Obtenir une description du nuanceur de sommets.
ms.assetid: 7e02a438-2ff4-4e32-bc16-d112aafa57cb
keywords:
- Méthode GetVertexShaderDesc Direct3D 11
- Méthode GetVertexShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetVertexShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetVertexShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8c69bab360fa3d12ccfc1a701926183dad7bbe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953960"
---
# <a name="id3dx11effectpassgetvertexshaderdesc-method"></a><span data-ttu-id="22128-106">ID3DX11EffectPass :: GetVertexShaderDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="22128-106">ID3DX11EffectPass::GetVertexShaderDesc method</span></span>

<span data-ttu-id="22128-107">Obtenir une description du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="22128-107">Get a vertex-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="22128-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22128-108">Syntax</span></span>


```C++
HRESULT GetVertexShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="22128-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22128-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22128-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="22128-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="22128-111">Type : **[ **D3DX11 \_ passe- \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="22128-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="22128-112">Pointeur vers une description du nuanceur de sommets (consultez [**D3DX11 \_ passe \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="22128-112">A pointer to a vertex-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22128-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22128-113">Return value</span></span>

<span data-ttu-id="22128-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22128-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22128-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="22128-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22128-116">Notes</span><span class="sxs-lookup"><span data-stu-id="22128-116">Remarks</span></span>

<span data-ttu-id="22128-117">Une passe d’effet peut contenir des affectations d’état de rendu et des assignations d’objets Shader.</span><span class="sxs-lookup"><span data-stu-id="22128-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="22128-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="22128-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="22128-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="22128-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="22128-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="22128-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22128-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22128-121">Requirements</span></span>



| <span data-ttu-id="22128-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22128-122">Requirement</span></span> | <span data-ttu-id="22128-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="22128-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22128-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="22128-124">Header</span></span><br/>  | <dl> <span data-ttu-id="22128-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="22128-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="22128-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22128-126">Library</span></span><br/> | <dl> <span data-ttu-id="22128-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="22128-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22128-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22128-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22128-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="22128-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





