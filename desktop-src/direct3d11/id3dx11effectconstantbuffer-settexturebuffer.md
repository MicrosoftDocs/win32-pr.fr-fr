---
title: Méthode ID3DX11EffectConstantBuffer SetTextureBuffer (D3dx11effect. h)
description: Définissez une texture-buffer.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Méthode SetTextureBuffer Direct3D 11
- Méthode SetTextureBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, méthode SetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974483"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a><span data-ttu-id="a5182-106">ID3DX11EffectConstantBuffer :: SetTextureBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="a5182-106">ID3DX11EffectConstantBuffer::SetTextureBuffer method</span></span>

<span data-ttu-id="a5182-107">Définissez une texture-buffer.</span><span class="sxs-lookup"><span data-stu-id="a5182-107">Set a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5182-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5182-108">Syntax</span></span>


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a5182-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5182-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5182-110">*pTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="a5182-110">*pTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a5182-111">Type : **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="a5182-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="a5182-112">Pointeur vers une interface Shader-Resource-View pour accéder à une mémoire tampon de texture.</span><span class="sxs-lookup"><span data-stu-id="a5182-112">A pointer to a shader-resource-view interface for accessing a texture buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5182-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5182-113">Return value</span></span>

<span data-ttu-id="a5182-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5182-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5182-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="a5182-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5182-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a5182-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a5182-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="a5182-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a5182-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="a5182-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a5182-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a5182-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a5182-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a5182-120">Requirements</span></span>



| <span data-ttu-id="a5182-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5182-121">Requirement</span></span> | <span data-ttu-id="a5182-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5182-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5182-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5182-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a5182-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5182-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a5182-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5182-125">Library</span></span><br/> | <dl> <span data-ttu-id="a5182-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="a5182-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5182-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5182-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5182-128">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="a5182-128">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





