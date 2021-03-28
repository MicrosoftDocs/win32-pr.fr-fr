---
title: Méthode ID3DX11EffectPass GetGeometryShaderDesc (D3dx11effect. h)
description: Obtient une géométrie-Description du nuanceur.
ms.assetid: 03298ec3-6b85-40bf-8920-a82c7606d326
keywords:
- Méthode GetGeometryShaderDesc Direct3D 11
- Méthode GetGeometryShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetGeometryShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetGeometryShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c3b84ed9e8c245611c1442987b68a94e7b10ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992241"
---
# <a name="id3dx11effectpassgetgeometryshaderdesc-method"></a><span data-ttu-id="c849c-106">ID3DX11EffectPass :: GetGeometryShaderDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="c849c-106">ID3DX11EffectPass::GetGeometryShaderDesc method</span></span>

<span data-ttu-id="c849c-107">Obtient une géométrie-Description du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c849c-107">Get a geometry-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c849c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c849c-108">Syntax</span></span>


```C++
HRESULT GetGeometryShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c849c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c849c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c849c-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="c849c-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="c849c-111">Type : **[ **D3DX11 \_ passe- \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="c849c-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="c849c-112">Pointeur vers une description Geometry-Shader (consultez [**D3DX11 \_ passe \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="c849c-112">A pointer to a geometry-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c849c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c849c-113">Return value</span></span>

<span data-ttu-id="c849c-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c849c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c849c-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="c849c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c849c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c849c-116">Remarks</span></span>

<span data-ttu-id="c849c-117">Une passe d’effet peut contenir des affectations d’état de rendu et des assignations d’objets Shader.</span><span class="sxs-lookup"><span data-stu-id="c849c-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="c849c-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="c849c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c849c-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="c849c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c849c-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c849c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c849c-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c849c-121">Requirements</span></span>



| <span data-ttu-id="c849c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c849c-122">Requirement</span></span> | <span data-ttu-id="c849c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c849c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c849c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c849c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c849c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c849c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c849c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c849c-126">Library</span></span><br/> | <dl> <span data-ttu-id="c849c-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="c849c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c849c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c849c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c849c-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="c849c-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





