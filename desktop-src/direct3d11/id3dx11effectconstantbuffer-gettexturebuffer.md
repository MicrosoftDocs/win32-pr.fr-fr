---
title: Méthode ID3DX11EffectConstantBuffer GetTextureBuffer (D3dx11effect. h)
description: Obtenir une mémoire tampon de texture.
ms.assetid: 8d09e67c-358e-49ee-8ca4-e1f548b52c3a
keywords:
- Méthode GetTextureBuffer Direct3D 11
- Méthode GetTextureBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, méthode GetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03000338c725e71096e57715a49a70b4347b358
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982479"
---
# <a name="id3dx11effectconstantbuffergettexturebuffer-method"></a><span data-ttu-id="1d0eb-106">ID3DX11EffectConstantBuffer :: GetTextureBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="1d0eb-106">ID3DX11EffectConstantBuffer::GetTextureBuffer method</span></span>

<span data-ttu-id="1d0eb-107">Obtenir une mémoire tampon de texture.</span><span class="sxs-lookup"><span data-stu-id="1d0eb-107">Get a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0eb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d0eb-108">Syntax</span></span>


```C++
HRESULT GetTextureBuffer(
   ID3D11ShaderResourceView **ppTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="1d0eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d0eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0eb-110">*ppTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="1d0eb-110">*ppTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="1d0eb-111">Type : **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="1d0eb-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="1d0eb-112">Adresse d’un pointeur vers une interface de nuanceur-ressource-affichage pour accéder à une mémoire tampon de texture.</span><span class="sxs-lookup"><span data-stu-id="1d0eb-112">The address of a pointer to a shader-resource-view interface for accessing a texture buffer.</span></span> <span data-ttu-id="1d0eb-113">Consultez [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="1d0eb-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0eb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d0eb-114">Return value</span></span>

<span data-ttu-id="1d0eb-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d0eb-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d0eb-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="1d0eb-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0eb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1d0eb-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d0eb-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="1d0eb-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1d0eb-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="1d0eb-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1d0eb-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1d0eb-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d0eb-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1d0eb-121">Requirements</span></span>



| <span data-ttu-id="1d0eb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d0eb-122">Requirement</span></span> | <span data-ttu-id="1d0eb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d0eb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0eb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d0eb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1d0eb-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d0eb-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1d0eb-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1d0eb-126">Library</span></span><br/> | <dl> <span data-ttu-id="1d0eb-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="1d0eb-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d0eb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d0eb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0eb-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="1d0eb-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





