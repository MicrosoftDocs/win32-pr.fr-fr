---
title: Méthode ID3DX11EffectShaderResourceVariable GetResourceArray (D3dx11effect. h)
description: Obtient un tableau de ressources de nuanceur.
ms.assetid: 7540183d-dabb-46c2-8df1-6d4734b77f25
keywords:
- Méthode GetResourceArray Direct3D 11
- Méthode GetResourceArray Direct3D 11, interface ID3DX11EffectShaderResourceVariable
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11, méthode GetResourceArray
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0091d81b7e157aecb8315e1def380800c8155c60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954020"
---
# <a name="id3dx11effectshaderresourcevariablegetresourcearray-method"></a><span data-ttu-id="5d71a-106">ID3DX11EffectShaderResourceVariable :: GetResourceArray, méthode</span><span class="sxs-lookup"><span data-stu-id="5d71a-106">ID3DX11EffectShaderResourceVariable::GetResourceArray method</span></span>

<span data-ttu-id="5d71a-107">Obtient un tableau de ressources de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="5d71a-107">Get an array of shader resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d71a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d71a-108">Syntax</span></span>


```C++
HRESULT GetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a><span data-ttu-id="5d71a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d71a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d71a-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="5d71a-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="5d71a-111">Type : **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d71a-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="5d71a-112">Adresse d’un tableau d’interfaces de nuanceur-ressource-vue.</span><span class="sxs-lookup"><span data-stu-id="5d71a-112">The address of an array of shader-resource-view interfaces.</span></span> <span data-ttu-id="5d71a-113">Consultez [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="5d71a-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="5d71a-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="5d71a-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="5d71a-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5d71a-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5d71a-116">Index de tableau de base zéro permettant d’accéder à la première interface.</span><span class="sxs-lookup"><span data-stu-id="5d71a-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="5d71a-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="5d71a-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="5d71a-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5d71a-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5d71a-119">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="5d71a-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d71a-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d71a-120">Return value</span></span>

<span data-ttu-id="5d71a-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d71a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d71a-122">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="5d71a-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d71a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5d71a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d71a-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="5d71a-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5d71a-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="5d71a-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5d71a-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5d71a-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d71a-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5d71a-127">Requirements</span></span>



| <span data-ttu-id="5d71a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d71a-128">Requirement</span></span> | <span data-ttu-id="5d71a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d71a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d71a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d71a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5d71a-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d71a-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5d71a-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d71a-132">Library</span></span><br/> | <dl> <span data-ttu-id="5d71a-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="5d71a-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d71a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d71a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d71a-135">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="5d71a-135">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

